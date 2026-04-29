# Output Contract

Default output is detailed Markdown suitable for Obsidian. Do not output a short outline unless the user explicitly asks for `quick` depth.

## Default Output Settings

- format: `obsidian-markdown`
- depth: `standard`
- scenario: infer from user request, default to `repo-review`
- language: follow the user's language, default to Simplified Chinese when the user writes Chinese
- evidence style: include labels and tables where useful

## Full Project Prep Output

Full output is allowed only when repository evidence is available.

A full project prep document may include:
- project background
- repository structure
- core files and entry points
- tech stack
- architecture and data flow
- API or interface flow when evidence exists
- core module review
- implementation walkthrough
- evidence matrix
- JD / resume / repo mapping when applicable
- high-frequency Q&A
- learning route
- thesis defense prep
- company review prep
- risk boundaries
- AI-assisted project transparency notes

## Default Full Markdown Structure

Use this structure for `standard` full mode. Adjust sections for the selected scenario.

```markdown
# 项目复盘与准备文档

## 0. 输入与证据范围

## 1. 项目一句话理解

## 2. 项目背景、目标与非目标

## 3. 技术栈与能力地图

## 4. 仓库结构与阅读路线

## 5. 核心文件与入口

## 6. 架构、接口流与数据流

## 7. 核心模块复盘

## 8. 场景化准备

## 9. Claims 与证据矩阵

## 10. 高频问题库

## 11. 需要补学的知识点

## 12. AI 辅助 / vibecoding 理解检查

## 13. 不建议主动强调的内容

## 14. 最终复习 checklist
```

## Scenario Sections

For `interview`, include:
- JD or role requirement analysis when available
- resume claims analysis when available
- project pitch: 30-second version and 2-minute version
- technical deep-dive talking points
- likely follow-up questions
- conservative wording for weak claims

For `thesis-defense`, include:
- research or project problem definition
- system design explanation
- implementation method
- testing or validation evidence
- innovation boundary
- defense questions and answer points

For `company-review`, include:
- project background and scope
- user's responsibility boundary when provided
- delivery summary
- technical decisions and tradeoffs
- risks, blockers, and follow-up plan
- unsupported business impact warnings

For `self-learning`, include:
- from-zero concept map
- repository reading order
- module-by-module study path
- exercises and self-check questions
- terms and prerequisites to learn first

For `repo-review`, include:
- neutral project summary
- repo onboarding route
- module and data-flow review
- risks and unknowns
- general question bank

## No-Repo Fallback Output

No-repo fallback output is intentionally limited. It may include only:
- claims extracted from input text
- claims that cannot be verified
- likely follow-up questions
- points that require repository verification
- conservative wording suggestions
- supplementary materials checklist

Every no-repo fallback document must include this warning near the top:

> 当前文档为 no-repo fallback 版本，未读取项目仓库。以下内容只能基于用户提供的文本进行 claims 审查、追问准备和保守表达建议，不能视为代码级项目复盘或仓库证据分析。

## No-Repo Forbidden Sections

No-repo fallback output must not include:
- repository directory structure
- core file list
- code entry points
- concrete request flow or data flow
- API or interface flow
- module implementation walkthrough
- code reading route
- repository evidence matrix
- verified tech stack beyond what the text explicitly claims
- confirmed architecture conclusions
- confirmed deployment, testing, monitoring, or production-readiness claims
- confirmed personal contribution or technical depth

## No-Repo Claim Labeling

All technical claims in no-repo fallback must use one of these labels:
- `仅简历声称`
- `仅用户背景声称`
- `待仓库验证`
- `不建议主动强调`
- `可作为被动回答准备`

Example:

| Claim | Source | Verification Status | Advice |
|---|---|---|---|
| 实现 RAG 检索流程 | 简历文本 | 待仓库验证 | 未看到仓库前不要主动强调完整实现 |
| 性能提升 40% | 简历文本 | 待仓库验证 | 需要 benchmark、日志或评估报告支持 |

## Fallback To Full Mode

If the user later provides a repository, switch from fallback mode to the appropriate full mode and regenerate the project prep document based on repository evidence.
