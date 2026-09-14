# Resume Claims

Use this file when resume project text is provided. A claim becomes interview-ready only when it is supported and the user can explain the relevant implementation.

## Extract

Classify claims about:

- project positioning and technologies;
- implemented modules and architecture;
- technical responsibilities and personal contribution;
- performance, business, user, or model impact;
- deployment, operations, scale, security, and reliability.

## Review Against Repository

Use [evidence_rules.md](evidence_rules.md) to classify support. Distinguish repository capability from personal ownership: code may prove that a feature exists but not who designed or implemented it.

| Resume Claim | Repo Evidence | Evidence Level | User Mastery | Interview Advice | Safer Wording |
|---|---|---|---|---|---|

For each important claim identify:

- the decisive source anchors;
- the runtime flow and concepts the user must explain;
- likely follow-ups and failure/debugging questions;
- an active-learning check or small modification that tests understanding;
- whether the claim is safe to emphasize, should be softened, or should not be used.

Do not produce polished claim-based answers before the user understands the relevant path. Route gaps to [self_learning.md](self_learning.md) or [interview_mode.md](interview_mode.md), then reassess.

## No-Repo Review

Without a repository, this is fallback only. Label implementation details `仅简历声称` or `待仓库验证`, identify likely follow-ups, and provide conservative wording. Do not imply implementation evidence or mastery.

## High-Risk Claims

Require especially strong evidence and demonstrated understanding for “主导架构设计,” “独立完成完整系统,” “端到端负责,” “上线生产,” high user/traffic scale, quantified performance or accuracy gains, and a complete RAG/agent/recommendation/microservice system.

Use [safety_rules.md](safety_rules.md) for final boundaries.
