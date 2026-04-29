---
name: project-prep-tailor
description: Evidence-first project review and preparation skill for repo-based onboarding, learning, interview prep, thesis defense prep, company review prep, and claim-risk audit. Use when the user wants to understand a project, prepare to explain it, align resume/JD/thesis/company context with repository evidence, or handle AI-assisted/vibecoding project claims honestly.
---

# Project Prep Tailor

## Purpose

Generate detailed, evidence-first Markdown project preparation documents. Use this skill to help the user understand a project from repository evidence, prepare for interviews, thesis or course defense, company project review, internship conversion review, or self-learning.

Default output is detailed Obsidian-friendly Markdown, not a short outline.

## Core Rule: Repo First

Full project prep requires a repository.

A repository is available when:
- the user provides a project path
- the current working directory is the project repository to analyze
- repository files are attached or visible in context
- the user clearly identifies a repository that can be inspected

If a repository is available, choose one full mode from [input_modes.md](input_modes.md):
- repo-only
- repo + learning goal
- repo + resume
- repo + JD
- repo + JD + resume
- repo + thesis / defense requirement
- repo + company context

If no repository is available, do not silently produce a full project review. First say:

> 当前缺少项目仓库，无法生成完整项目复盘文档。可以继续生成 no-repo fallback 文档，但只会包含 claims 审查、追问清单和保守话术；若需要完整项目学习文档，请提供项目仓库或在仓库目录中运行。

Only continue in no-repo fallback if the user explicitly accepts it or the request clearly asks for claim audit only.

## Workflow

1. Identify available inputs: repository, resume project text, JD, learning goal, thesis or defense requirement, company context.
2. Select the input mode using [input_modes.md](input_modes.md).
3. Select the scenario: `interview`, `thesis-defense`, `company-review`, `self-learning`, or `repo-review`.
4. Select depth using [depth_modes.md](depth_modes.md). Default is `standard`; use `from-zero` when the user wants to learn the project from scratch.
5. Inspect repository evidence before writing when a repo is available. Follow [repo_evidence.md](repo_evidence.md).
6. Apply evidence labels from [evidence_rules.md](evidence_rules.md).
7. Apply scenario rules:
   - JD and interview: [jd_analysis.md](jd_analysis.md), [resume_claims.md](resume_claims.md), [question_bank.md](question_bank.md)
   - thesis or course defense: [defense_prep.md](defense_prep.md)
   - company review: [company_review_prep.md](company_review_prep.md)
   - self-learning: [self_learning.md](self_learning.md)
8. Apply AI-assisted project rules from [ai_assisted_project.md](ai_assisted_project.md).
9. Apply safety rules from [safety_rules.md](safety_rules.md).
10. Produce the final Markdown document using [output_contract.md](output_contract.md).

## Evidence Discipline

Do not fabricate project capability, business metrics, performance gains, launch status, user scale, technical depth, or personal contribution.

If a claim is weak, label it. If a claim is unsupported, mark it as not recommended for active emphasis. If the project appears AI-assisted or vibecoded, help the user understand and explain the project honestly instead of disguising the development process.

## No-Repo Fallback Limits

No-repo fallback is claim-audit-only. It must not include:
- repository directory structure
- core files
- code entry points
- concrete data flow or API flow
- module implementation details
- code reading route
- repository evidence matrix
- verified architecture, deployment, testing, monitoring, or production-readiness claims

Fallback output may include only:
- claims extracted from user text
- unverifiable claims
- likely follow-up questions
- points requiring repository verification
- conservative wording suggestions
- supplementary materials checklist

## References

Read [references/prompt.md](references/prompt.md) when the user wants a reusable long-form prompt.

Read [references/examples.md](references/examples.md) when you need concrete examples of evidence labels, no-repo fallback, AI-assisted wording, or output structure.
