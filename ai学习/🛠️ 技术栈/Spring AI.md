# Spring AI

## 一句话描述
Spring 官方推出的 AI 应用开发框架，与 Spring Boot 无缝集成。

## 核心概念
- **ChatClient**：统一的聊天客户端接口
- **Prompt Template**：提示词模板管理
- **Function Calling**：工具调用能力
- **Vector Store**：向量存储抽象

## 与我的架构关系
- [[1-接入网关]] 的实现基础
- [[9-LLM调用流程]] 的调用封装

## 代码示例

### ChatClient 基础调用
```java
ChatClient chatClient = ChatClient.builder(openAiChatModel).build();

ChatResponse response = chatClient.prompt()
    .user("Hello")
    .call()
    .chatResponse();
```

### 流式调用
```java
Flux<ChatResponse> stream = chatClient.prompt()
    .user("Write a poem")
    .stream();

stream.subscribe(response -> 
    System.out.println(response.getResult().getOutput().getContent())
);
```

### Function Calling
```java
ChatClient chatClient = ChatClient.builder(openAiChatModel)
    .defaultOptions(OpenAiChatOptions.builder()
        .functions(List.of(new WeatherFunction()))
        .build())
    .build();
```

## 常见坑点
- 响应式环境下需要使用 `Flux`/`Mono` 而非同步调用
- 模型参数需要根据具体模型进行适配
- Function Calling 需要定义清晰的 JSON Schema

## 参考资源
- 官方文档：https://docs.spring.io/spring-ai/reference/