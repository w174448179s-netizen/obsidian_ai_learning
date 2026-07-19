# 十一、Task任务管理

## 一句话职责
管理AI对话任务的生命周期和状态。

## Task生命周期

### CREATED
- 任务创建成功
- 分配TaskId
- 初始化状态

### RUNNING
- 任务正在执行
- 模型正在生成
- SSE连接活跃

### SUCCESS
- 任务执行成功
- 模型响应完成
- SSE连接正常关闭

### FAILED
- 任务执行失败
- 模型调用出错
- 返回错误信息

### CANCELLED
- 用户主动取消
- 连接异常断开
- 超时自动取消

## Task保存

### Redis
- 实时状态存储
- 快速读写
- 过期时间设置

### 数据库
- 持久化存储
- 历史记录查询
- 审计日志关联

## 管理内容

### 核心信息
- **conversationId**：会话标识
- **traceId**：链路追踪标识
- **SSE连接状态**：活跃/断开
- **模型调用状态**：进行中/完成/失败

### 扩展信息
- 用户ID
- 模型名称
- Token消耗
- 耗时统计

## 状态管理流程

```
创建任务 → 保存Redis → 执行模型调用 → 更新状态为RUNNING
            → 模型完成 → 更新状态为SUCCESS → 清理资源
            → 模型失败 → 更新状态为FAILED → 记录错误
            → 用户取消 → 更新状态为CANCELLED → 终止模型
```

## 代码片段

### Task状态管理

```java
public class TaskManager {
    
    private final ReactiveRedisTemplate<String, TaskInfo> redisTemplate;
    
    public Mono<TaskInfo> createTask(TaskInfo task) {
        task.setStatus(TaskStatus.CREATED);
        task.setCreatedAt(LocalDateTime.now());
        return redisTemplate.opsForValue()
            .set(task.getTaskId(), task, Duration.ofMinutes(30))
            .thenReturn(task);
    }
    
    public Mono<Void> updateStatus(String taskId, TaskStatus status) {
        return redisTemplate.opsForValue().get(taskId)
            .flatMap(task -> {
                task.setStatus(status);
                return redisTemplate.opsForValue().set(taskId, task);
            })
            .then();
    }
    
    public Mono<TaskInfo> getTask(String taskId) {
        return redisTemplate.opsForValue().get(taskId);
    }
    
    public Mono<Void> deleteTask(String taskId) {
        return redisTemplate.delete(taskId);
    }
}
```

## 设计考量

- Task状态需要实时同步到Redis
- 客户端断开连接时需要及时清理Task
- Task过期时间需要合理设置
- 状态转换需要保证原子性

## 关联模块

- 上游：[[9-LLM调用流程]]
- 共享：[[10-SSE流式通信]]
- 数据：[[14-数据层]]