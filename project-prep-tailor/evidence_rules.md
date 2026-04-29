# Evidence Rules

All project prep output must be evidence-first. The goal is to help the user understand and explain what can be supported, not to make the project look stronger than it is.

## Evidence Levels

### Strong Evidence

Use label: `强证据`

Examples:
- README or docs explicitly describe the feature
- source code implements the feature
- API routes, schemas, services, models, workflows, or tests show the behavior
- dependency and runtime wiring confirm actual use
- Docker, CI, deployment, or config files show delivery setup

Allowed wording:
- "仓库中实现了..."
- "代码显示..."
- "配置文件证明..."

### Medium Evidence

Use label: `中证据`

Examples:
- directory structure strongly suggests a module boundary
- dependencies and partial wiring suggest likely use
- naming and references show an intended capability but not the full flow

Allowed wording:
- "仓库结构显示..."
- "项目中包含相关模块..."
- "从依赖和调用关系看，可能用于..."

### Weak Evidence

Use label: `弱证据`

Examples:
- only directory names imply a feature
- comments mention a plan but code is incomplete
- dependency exists but no implementation path is found

Allowed wording:
- "仓库中有相关迹象..."
- "可以作为待确认点..."
- "不建议主动强调为已完整实现..."

### Resume-Only Claim

Use label: `仅简历声称`

Use when:
- the resume states a capability
- repository evidence has not confirmed it

Required behavior:
- do not present the claim as verified
- ask for repository evidence or mark it as risk
- provide conservative interview language

### User-Context-Only Claim

Use label: `仅用户背景声称`

Use when:
- the user provides company, business, metric, ownership, or delivery context
- the repository does not independently confirm it

Required behavior:
- distinguish user-provided context from repository evidence
- avoid converting user context into confirmed fact

### Pending Repo Verification

Use label: `待仓库验证`

Use when:
- no repository is available
- a claim is plausible but not verified
- the needed files or modules were not found

### Insufficient Evidence

Use label: `证据不足`

Use when:
- a claim cannot be supported by available inputs
- the claim is too broad for the evidence
- the claim depends on hidden production context

### Should Not Claim

Use label: `不应声称`

Use when:
- the claim is unsupported and high risk
- it would misrepresent the project
- it creates false technical depth, business impact, or personal contribution

## Evidence Matrix Fields

Use this table shape when a matrix is useful:

| Claim | Source | Evidence | Evidence Level | Recommended Wording | Risk |
|---|---|---|---|---|---|

For JD + resume + repo, use:

| JD Requirement | Resume Claim | Repo Evidence | Evidence Level | Prep Advice | Risk |
|---|---|---|---|---|---|

## Claims That Require Extra Care

Require strong evidence for:
- business metrics
- performance gains
- user scale
- production launch
- revenue or conversion impact
- security or compliance claims
- high availability or reliability claims
- "designed architecture"
- "owned end-to-end"
- "independently implemented"
- "optimized model accuracy"
- "built a full RAG / agent system"

## Dependency Rule

A dependency in `package.json`, `requirements.txt`, `pyproject.toml`, `pom.xml`, or another manifest is not enough to claim full implementation.

Example:
- `langchain` dependency alone does not prove a complete agent workflow
- `redis` dependency alone does not prove production cache design
- `pytest` dependency alone does not prove meaningful test coverage

## Conservative Wording

Use conservative wording when evidence is incomplete:
- "项目中包含基础实现..."
- "仓库显示使用了..."
- "简历中提到，但仓库证据不足..."
- "可作为被动回答准备，不建议主动强调..."
- "需要进一步确认..."
