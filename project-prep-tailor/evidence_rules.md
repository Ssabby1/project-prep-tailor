# Evidence Rules

All teaching and preparation must distinguish what the repository proves, what is inferred, what is general knowledge, and how strong a claim is. These are two related but separate dimensions.

## Teaching Provenance Labels

Use these labels in repository explanations:

### `[Repo Fact]`

The statement is directly supported by inspected repository evidence. Cite `path::symbol` and a reliable line or range when available. State whether runtime behavior was observed or only statically wired when that distinction matters.

### `[Inference]`

The statement is a reasonable interpretation of structure, naming, partial wiring, or likely design intent, but is not directly proven. Include the basis and avoid definitive language.

### `[General Concept]`

The statement explains transferable software or AI knowledge. Tie it to the inspected code, but never use it as proof that this project implements the concept.

Example:

```text
[Repo Fact] `src/agent.py::dispatch_tool` maps the selected tool name to a registered callable.
[General Concept] This is a tool-dispatch pattern: model output is converted into a deterministic program call.
[Inference] The separation may make tool validation easier; no design note confirms that rationale.
```

If an important statement cannot be confirmed, say so and identify the missing evidence.

## Claim-Strength Labels

Use these for resume, JD, business, ownership, maturity, and impact claims. They do not replace the provenance labels above.

### `强证据`

Direct implementation and wiring, an executing test, reliable documentation plus matching code, or relevant runtime/deployment evidence supports the scoped claim.

### `中证据`

Structure and partial wiring support a narrower interpretation, but the complete behavior or scope is not established.

### `弱证据`

Only names, comments, dependencies, scaffolding, or incomplete code suggest the capability.

### `仅简历声称`

The resume states the claim, but inspected evidence has not confirmed it.

### `仅用户背景声称`

The user provides company, business, metric, ownership, or delivery context that the repository cannot independently confirm.

### `待仓库验证`

The repository is unavailable or the relevant evidence has not yet been inspected.

### `证据不足`

Available inputs cannot support the requested scope, typically because the claim depends on hidden production, business, scale, or personal-contribution context.

### `不应声称`

The claim is contradicted, materially misleading, or high-risk and unsupported.

## Evidence Matrices

Use only when a table helps review or export:

| Claim | Source | Evidence Anchor | Evidence Level | Recommended Wording | Risk |
|---|---|---|---|---|---|

For JD + resume + repo:

| JD Requirement | Resume Claim | Repo Evidence | Evidence Level | Preparation Advice | Risk |
|---|---|---|---|---|---|

## Extra-Care Claims

Require strong, correctly scoped evidence for:

- business metrics, performance gains, user scale, revenue, conversion, or cost impact;
- production launch, security, compliance, availability, reliability, or scale;
- “designed the architecture,” “owned end-to-end,” or “independently implemented”;
- model accuracy, evaluation gains, or self-developed models;
- a complete RAG, agent, recommendation, or microservice system.

A dependency is never enough. A framework integration is not original framework development. Static deployment files are not proof of a production launch. User understanding is not proof of personal authorship, and repository authorship is not safely inferable from code alone.

## Conservative Language

Prefer scoped wording when evidence is incomplete:

- “项目中包含基础实现……”
- “仓库显示使用了……，但完整运行链尚未确认。”
- “简历中提到，但当前仓库证据不足……”
- “可作为补学或被动回答准备，不建议主动强调……”
- “需要运行日志、测试、部署记录或用户背景进一步确认……”
