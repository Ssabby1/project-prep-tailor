# AI-Assisted And Vibecoding Projects

AI-assisted work is valid, but runnable code is not proof that the user understands, authored, or validated it. The objective is to turn generated code into genuinely understood and honestly explainable work.

## Core Rules

- Do not shame or inflate AI-assisted work.
- Separate repository implementation, user-provided contribution context, and demonstrated user understanding.
- Do not infer which code was generated or personally written unless evidence or user context says so.
- Do not claim independent architecture, end-to-end ownership, production maturity, or full mastery without support.
- Prioritize learning the runtime flow and the modules the user plans to discuss.

## Detect Project-Specific AI Capabilities

Inspect for actual wiring of relevant concepts, including LLM invocation, prompt construction, structured output, function/tool calling, registration and execution, agent loops, planning, reflection, memory/state, RAG, embedding, vector storage, chunking, retrieval, reranking, context construction, MCP, multi-agent orchestration, workflows/state machines, guardrails, evaluation, observability, retries, rate limits, streaming, and concurrency.

Teach only concepts that the repository actually implements or that are necessary to understand a confirmed gap. For each present capability, follow:

```text
repository implementation → decisive source → general concept
→ evidenced constraint or inferred rationale → relevant alternative/tradeoff
```

Do not call an LLM SDK dependency an agent, a vector-store dependency a RAG pipeline, or a tool schema an executed tool flow without verifying the rest of the path.

## Understanding And Ownership Check

Track relevant modules with:

| Module / Claim | Repo Evidence | What The User Can Demonstrate | Current Risk | Next Exercise |
|---|---|---|---|---|

Use prediction, code navigation, explain-back, modification planning, and debugging to establish that the user can:

- locate the entry and decisive symbols;
- trace inputs, outputs, state, and external calls;
- explain why the capability is needed here;
- identify failure behavior and the first debugging evidence;
- propose or perform a small safe modification;
- name what is absent, incomplete, or unverified.

Do not mark a capability interview-ready until the user can explain it repository-specifically and respect claim boundaries.

## Honest Interview Language

Appropriate wording may include:

- “我使用 AI 辅助完成初版实现，之后重点验证并理解了……的运行链。”
- “我能从 `path::symbol` 解释这一段的数据流、异常路径和我做过的调整。”
- “当前我已掌握核心流程；部署规模和部分工程化细节没有足够证据，不会扩大描述。”

Risky wording includes “独立设计完整架构,” “完整掌握所有模块,” “生产级,” “高并发,” “自研模型,” or quantified gains without strong evidence.

The preferred remediation is learning and verification, not cosmetic rewriting.
