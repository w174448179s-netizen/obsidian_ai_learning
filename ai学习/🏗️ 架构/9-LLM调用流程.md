# 九、LLM调用流程

## 一句话职责
描述从用户输入到模型响应的完整调用链路。

## 完整调用流程

### 1. 用户输入
- 接收用户消息
- 消息格式校验
- 输入内容预处理

### 2. Prompt构建
- System Prompt 组装
- 用户消息格式化
- 上下文拼接
- 工具定义注入

### 3. Context拼接
- 从记忆管理加载历史对话
- 从RAG检索相关知识
- 控制上下文长度（不超过模型窗口）
- 重要信息优先

### 4. Token计算
- 计算输入Token数量
- 检查是否超过限制
- 预估输出Token数量
- 成本预估

### 5. 模型调用
- 选择合适的适配器
- 执行API调用
- 处理响应
- 错误重试

### 6. 流式输出SSE
- 将响应转为SSE格式
- 逐Token推送
- 客户端实时渲染
- 打字机效果

## 调用流程示意图

```
用户输入 → Prompt构建 → Context拼接 → Token计算
            → 模型调用 → 流式输出SSE → 客户端渲染
```

## 关键参数

### 推理参数
- **temperature**：控制随机性（0-2）
- **maxTokens**：最大输出Token数
- **topP**：核采样概率
- **frequencyPenalty**：频率惩罚
- **presencePenalty**：存在惩罚

### 格式参数
- **responseFormat**：响应格式（JSON、文本）
- **stream**：是否流式输出
- **model**：模型名称

## 代码片段

### 非流式调用

```java
CompletableFuture<ModelResponse> response = modelAdapter.chat(request);
response.thenAccept(resp -> {
    // 处理响应
});
```

### 流式调用

```java
Flux<String> stream = modelAdapter.streamChat(request);
stream.subscribe(
    chunk -> System.out.println(chunk),      // 处理每个token
    error -> log.error("Stream error", error), // 错误处理
    () -> log.info("Stream complete")        // 完成处理
);
```

## 设计考量

- 流式输出对用户体验提升明显，建议默认开启
- Context拼接需要考虑模型窗口限制
- Token计算需要精确，避免超额扣费
- 错误重试需要设置合理的重试次数和间隔

## 关联模块

- 上游：[[8-模型适配层]]
- 下游：[[10-SSE流式通信]]
- 共享：[[11-Task任务管理]]