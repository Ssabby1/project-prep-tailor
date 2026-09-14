# Compact Examples

## Repository-Grounded Explanation

```text
[Repo Fact] `src/api/chat.py::create_message` validates the request and passes the normalized message to `ChatService.reply`.

[Repo Fact] `src/services/chat.py::ChatService.reply` builds the model input and calls the configured client. A runtime test was not executed, so this confirms static wiring rather than observed production behavior.

[General Concept] The route/service split keeps transport validation separate from application logic.

[Inference] That separation may improve testability, but no design note confirms the authors' rationale.
```

## Repository Map

| Area / File | Priority | Role | Evidence Anchor | Learn Now? |
|---|---|---|---|---|
| `src/api/` | Core | Request entry | `chat.py::create_message` | Yes |
| `src/services/` | Core | Application flow | `chat.py::ChatService.reply` | Yes |
| `.github/` | Infrastructure | CI | workflow files | Later |
| `dist/` | Generated | Build output | generated assets | Skip |

## Runtime Flow

| Step | Evidence Anchor | Input | Action | Output | Next Hop |
|---|---|---|---|---|---|
| 1 | `src/api/chat.py::create_message` | HTTP payload | Validate and normalize | message DTO | `ChatService.reply` |
| 2 | `src/services/chat.py::ChatService.reply` | message DTO | Construct model request | model response | response mapper |

Do not add an Agent, Tool, RAG, database, or queue hop unless code establishes it.

## Active-Learning Turn

```text
现在先不要看答案：如果模型调用成功，但接口最终返回空内容，你会沿着上面的 flow 先检查哪两个 symbol？为什么？
```

After the user answers, compare it with the actual code, teach only the missing link, and ask for a revised explanation.

## Claim Matrix

| Claim | Source | Evidence | Evidence Level | Recommended Wording | Risk |
|---|---|---|---|---|---|
| 使用 FastAPI 构建服务 | code | route plus app registration | 强证据 | 仓库实现了 FastAPI API 层 | Low |
| Redis 缓存优化 | resume | dependency only, no call path | 弱证据 | 当前只确认依赖，缓存运行链待验证 | Medium |
| 支撑高并发 | resume | no benchmark/runtime evidence | 证据不足 | 不建议主动强调 | High |

## Interview Correction Loop

```text
Question: 为什么这里需要 Agent？
User: 因为 Agent 更灵活。
Assessment: 这是通用优势，还没有说明本项目中的动态决策点、源码位置或 deterministic workflow 是否可行。
Tutor fallback: 回到已确认的 agent loop 和 tool-dispatch symbols。
Retry: 请结合这两个 symbols 重新回答，并说明不用 Agent 的替代方案。
```

## No-Repo Fallback

> 当前文档为 no-repo fallback 版本，未读取项目仓库。以下内容只能基于用户提供的文本进行 claims 审查、追问准备和保守表达建议，不能视为代码级项目复盘、源码教学或仓库证据分析。

Do not list repository structure, source files, runtime flow, or verified architecture in fallback.
