# Examples

## Evidence Matrix Example

| Claim | Source | Evidence | Evidence Level | Recommended Wording | Risk |
|---|---|---|---|---|---|
| 项目包含 FastAPI 服务 | 代码 | `requirements.txt` 和 API route 文件 | 强证据 | 可以主动说明使用 FastAPI 构建服务接口 | 低 |
| 使用 Redis 做缓存优化 | 简历 | 仅看到 Redis 依赖，未看到缓存调用 | 弱证据 | 只说项目包含 Redis 相关依赖，缓存实现待确认 | 中 |
| 支撑高并发访问 | 简历 | 未看到压测、部署或监控证据 | 证据不足 | 不建议主动强调 | 高 |

## No-Repo Fallback Example

> 当前文档为 no-repo fallback 版本，未读取项目仓库。以下内容只能基于用户提供的文本进行 claims 审查、追问准备和保守表达建议，不能视为代码级项目复盘或仓库证据分析。

| Claim | Source | Verification Status | Advice |
|---|---|---|---|
| 实现 RAG 检索问答 | 简历文本 | 待仓库验证 | 需要确认 embedding、vector store、retriever 和 query flow |
| 优化响应速度 50% | 简历文本 | 待仓库验证 | 需要 benchmark 或日志支持，不建议主动强调 |

Forbidden in fallback:
- listing project directories
- naming core files
- describing data flow as verified
- creating a repository evidence matrix

## AI-Assisted Wording Example

Safe:
- "我使用 AI 辅助完成初版实现，但我重点理解和调整了 API 流程、数据结构和异常处理。"
- "这部分目前我能解释主流程，但部署和测试细节还需要继续补齐。"

Unsafe:
- "我独立设计了完整架构。"
- "系统已经达到生产级稳定性。"

## Interview Prep Example Shape

```markdown
## 项目讲述：30 秒版本

这个项目是... 仓库证据主要来自... 当前能确认的是...

## 高频追问

| 问题 | 回答要点 | 证据 | 风险 |
|---|---|---|---|
```

## From-Zero Learning Example Shape

```markdown
## 从 0 学习路线

| Step | Goal | Files | Self-Check |
|---|---|---|---|
| 1 | 理解项目入口 | README, main file | 能否说清项目如何启动 |
| 2 | 理解核心流程 | routes, services | 能否画出请求流 |
```
