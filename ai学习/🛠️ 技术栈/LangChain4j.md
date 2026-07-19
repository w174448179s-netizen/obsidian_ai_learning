# LangChain4j

## 一句话描述
LangChain 的 Java 移植版，适合复杂 AI 工作流编排。

## 核心概念
- **ChatLanguageModel**：聊天语言模型接口
- **Chain**：链式调用，组合多个组件
- **Agent**：智能体，具备规划和工具调用能力
- **Tool**：可调用的外部工具

## 与 Spring AI 的对比

| 特性 | LangChain4j | Spring AI |
|------|-------------|-----------|
| 灵活性 | 高，适合复杂工作流 | 中等，Spring生态集成更好 |
| 学习曲线 | 较陡 | 较低，Spring用户熟悉 |
| 社区生态 | 快速增长 | Spring官方背书 |

## 何时使用
- 需要多步推理的复杂 Agent
- 需要精细控制工作流的场景
- 需要自定义 Chain 编排

## 代码示例

### 基础 Chain
```java
ChatLanguageModel model = new OpenAiChatModel(apiKey);

PromptTemplate promptTemplate = PromptTemplate.from(
    "Question: {question}\nAnswer:"
);

Chain<String, String> chain = promptTemplate
    .apply(question -> Map.of("question", question))
    .andThen(model::generate)
    .andThen(Generation::text);

String answer = chain.execute("What is AI?");
```

### Agent 示例
```java
Agent agent = Agent.builder()
    .chatLanguageModel(model)
    .tools(List.of(new CalculatorTool(), new SearchTool()))
    .build();

String response = agent.execute("What is 25% of 400?");
```

## 参考资源
- 官方文档：https://docs.langchain4j.dev/