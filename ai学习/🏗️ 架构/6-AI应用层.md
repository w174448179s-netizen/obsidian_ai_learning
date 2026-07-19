# 六、AI应用层 Application Layer

## 一句话职责
处理业务逻辑，管理对话和Agent执行。

## Chat Service

### 对话管理
- **ConversationId**：会话唯一标识
- **MessageId**：消息唯一标识
- 多轮对话历史管理
- 对话状态跟踪

### 对话生命周期
- 创建对话：生成ConversationId
- 追加消息：记录用户输入和模型响应
- 结束对话：清理资源
- 恢复对话：加载历史消息

## Agent Runtime

### Agent选择
- 根据意图选择合适的Agent
- Agent能力匹配
- Agent版本管理

### Agent执行
- 执行Agent任务
- 工具调用
- 结果收集

### Tool调用
- Function Calling
- JSON Schema定义
- 工具执行结果解析
- 重试机制

### 工作流编排
- 简单线性流程
- 分支流程
- 循环流程
- 并行流程

## Memory

### 短期记忆
- 当前上下文
- 对话历史
- 滑动窗口管理
- 摘要压缩

### 长期记忆
- 用户历史数据
- 用户画像
- 偏好设置
- 历史决策记录

## Agent主服务架构

```
AI-Agent-Service
├── 第一层：输入预处理层
│   ├── 文本清洗（空白符/全角/表情/格式标准化）
│   ├── 长度校验 + 预警/截断标记
│   ├── Prompt注入正则校验、高危敏感词AC校验
│   └── 输出：标准OpenAI格式JSON + X-Logic-Model-Id Header
├── 第二层：意图粗识别层
│   ├── 规则词表 + 轻量分类模型
│   └── 角色/配额读取（Redis + SSO JWT信息）
├── 第三层：会话记忆 ChatMemory
│   ├── 主线会话：绑定单一X-Logic-Model-Id
│   └── 备用异构会话：独立ChatSession，禁用RAG/SQL工具
├── 第四层：业务编排层
│   ├── RAG向量检索、SQL生成、插件工具调用
│   └── System Prompt模板
└── 第五层：模型调用层
    └── OpenAiChatModel（Spring AI）标准调用
```

## 代码片段

### Agent标准模型调用示例

```java
// 主线会话：纯标准OpenAI参数，无厂商私有参数
OpenAiChatOptions options = OpenAiChatOptions.builder()
        .model("qwen-openai")
        .temperature(0.7)
        .maxTokens(2000)
        .build();

ChatClient chatClient = ChatClient.builder(openAiChatModel)
        .defaultOptions(options)
        .build();

// 绑定主线modelId Header
HttpHeaders headers = new HttpHeaders();
headers.add("X-Logic-Model-Id", "qwen-openai");
```

## 设计考量

- 主线会话全程固定modelId，全程同协议模型
- RAG、SQL、多轮对话复用同一套上下文格式
- 异构备用会话独立管理，不影响主线

## 关联模块

- 上游：[[5-AI安全防护]]
- 下游：[[7-RAG检索增强生成]]、[[8-模型适配层]]
- 共享：[[11-Task任务管理]]