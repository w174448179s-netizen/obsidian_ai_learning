# MOC-踩坑记录

## 环境与配置
- Spring Boot 3.2+ 的响应式MDC需要使用 `Hooks.enableAutomaticContextPropagation()`
- Redis分布式限流需要注意Lua脚本的原子性

## Spring AI
- 响应式环境下需要使用 `Flux`/`Mono` 返回值
- Function Calling 需要定义清晰的 JSON Schema

## 模型API调用
- 不同模型的temperature参数范围不同（OpenAI: 0-2, Qwen: 0-1）
- 需要注意模型的Token限制和计费规则

## 向量数据库
- Chunk大小影响检索效果，需要根据文档类型调整
- 向量数据库选择需要考虑数据规模和查询性能

## 部署与运维
- Kubernetes健康检查探针配置不当会导致服务频繁重启
- 优雅关闭需要正确处理SSE长连接

## 架构设计
- 网关是"薄层"，不要把业务逻辑放进去
- 限流是"预防"，熔断是"止损"，组合编排顺序很重要