# 十、SSE流式通信

## 一句话职责
实现服务端向客户端的实时数据推送。

## SSE基础

### 协议特点
- **服务端持续推送**：一次请求，多次响应
- **单向通信**：服务端→客户端
- **长连接**：连接保持打开状态
- **自动重连**：客户端自动尝试重连

### 协议格式

```
event: message
data: {"content": "Hello"}

data: {"content": "World"}

```

- `event`：事件类型（可选）
- `data`：数据内容（必需）
- `retry`：重连间隔（可选）

## 为什么AI应用选SSE

### WebMVC vs WebFlux

#### WebMVC（Spring MVC + Tomcat Servlet）
- 同步阻塞 one-request-one-thread 模型
- 一个请求独占一个Tomcat工作线程
- LLM推理很慢（数秒），线程全程卡住等待
- 线程 = 并发上限，无法支撑海量长连接对话
- 例子：Tomcat默认线程池200个，几百个长对话请求就会占满

#### WebFlux（Reactor + Netty EventLoop）
- 非阻塞响应式模型
- 少量固定Netty事件循环线程（默认CPU核心数×2）
- IO等待时释放线程，不阻塞占用
- 一条SSE长连接 = 一条Netty Channel，不是独占OS线程
- Flux天然适配逐片流式推送

### 核心对比

| 特性 | WebMVC | WebFlux |
|------|--------|---------|
| 线程模型 | 阻塞线程池 | 事件循环 |
| 并发上限 | 线程池大小 | 内存容量 |
| SSE支持 | 差（阻塞线程） | 原生支持 |
| 流式输出 | 不适合 | 天然适配 |

## WebFlux核心语法

### 返回值规范
- **Mono\<T\>**：0/1个元素（普通查询、写入）
- **Flux\<T\>**：0/N个元素（列表、SSE流式输出）
- **Mono\<Void\>**：只执行动作，无返回（删除、更新）

### 核心算子
- **map()**：同步内存转换
- **flatMap()**：异步操作，返回Mono/Flux
- **flatMapMany()**：Mono转Flux（SSE必备）
- **onErrorResume()**：异常切换备用流
- **doOnCancel()**：长连接被客户端断开

### SSE端点定义

```java
@GetMapping(value = "/stream", produces = MediaType.TEXT_EVENT_STREAM_VALUE)
public Flux<ServerSentEvent<String>> stream(@RequestBody Mono<ChatRequest> reqMono) {
    return reqMono
        .flatMapMany(req -> llmClient.stream(req))
        .map(chunk -> ServerSentEvent.builder(chunk).build())
        .doOnCancel(() -> cancelLlmTask())
        .onErrorResume(e -> Flux.just(ServerSentEvent.builder("对话中断").build()));
}
```

## SSE管理

### Task任务管理
- 使用Task管理每个SSE连接
- Redis保存任务状态
- 断开检测
- Cancel机制

### 心跳保活
- 定时发送心跳消息
- 防止HTTP连接被中间件关闭
- 客户端检测连接状态

### 超时控制
- 请求超时配置
- 流式超时配置
- 超时自动断开

## 代码片段

### SSE流式对话模板

```java
reqMono
    .flatMapMany(req -> llmClient.stream(req))
    .map(chunk -> ServerSentEvent.builder(chunk).build())
    .doOnCancel(() -> cancelLlmTask()) // 用户关闭页面，终止模型
    .onErrorResume(e -> Flux.just(ServerSentEvent.builder("对话中断").build()));
```

## 设计考量

- AI应用的"高延迟 + 长连接 + 流式输出"三大特性决定了必须用WebFlux
- WebFlux不能随意调用阻塞API，否则会卡死EventLoop线程
- 客户端断开时必须释放模型资源（doOnCancel）

## 关联模块

- 上游：[[9-LLM调用流程]]
- 共享：[[11-Task任务管理]]
- 技术栈：[[Spring AI]]