# Export And Output Contract

Interactive learning is the primary product for `self-learning` and `from-zero`. Markdown or Obsidian output is an export produced when the user asks for notes, a project review, a final study document, a review sheet, or when a completed learning cycle makes a summary useful.

Do not silently turn the first tutor response into a full document. Conversational teaching may use compact Markdown without following the export structure.

## Defaults

- format: follow the user; for requested notes, default to Obsidian-friendly Markdown;
- language: follow the user, defaulting to Simplified Chinese for Chinese requests;
- export depth: `standard` unless the user requests quick or deep;
- evidence: preserve provenance labels, claim-strength labels, source anchors, uncertainties, and user mastery gaps;
- scenario: infer from the request.

## Learning Export

Include the useful accumulated state, not generic filler:

```markdown
# 项目学习与准备笔记

## 0. 输入、仓库范围与证据边界
## 1. Project Mental Model
## 2. Architecture 与核心 Entry Points
## 3. Repository Map 与学习优先级
## 4. Representative End-to-End Runtime Flow
## 5. 核心模块与关键源码
## 6. 设计取舍、失败场景与 Debug 路线
## 7. Mastery Summary
## 8. Key Source References
## 9. Remaining Knowledge Gaps
## 10. 下一步练习与 Interview Readiness
```

Include only taught or inspected material. Distinguish what the user has demonstrated from what the assistant merely explained.

## Preparation Exports

Adapt rather than forcing every section:

- **Interview:** JD/resume/repo mapping, corrected user answer points, source anchors, follow-ups, claim risks, mastery summary, and remaining gaps. Add 30-second or 2-minute pitches only after understanding is demonstrated or clearly label them as drafts requiring verification.
- **Thesis defense:** problem, method, repository implementation, representative flow, validation evidence, innovation boundary, limitations, likely questions, and unresolved gaps.
- **Company review:** project scope, responsibility context, repository-supported delivery, decisions, blockers, risks, next steps, and business claims requiring company evidence.
- **Repo review:** mental model, Repository Map, architecture, runtime flow, core modules, evidence matrix, risks, tests/operations, and onboarding route.

## Evidence Tables

Use tables only when they improve scanning:

| Claim | Source | Evidence Anchor | Evidence Level | Recommended Wording | Risk |
|---|---|---|---|---|---|

| Module | Mastery State | Demonstrated Evidence | Remaining Gap | Next Step |
|---|---|---|---|---|

## No-Repo Fallback

No-repo output is claim-audit-only and must place this warning near the top:

> 当前文档为 no-repo fallback 版本，未读取项目仓库。以下内容只能基于用户提供的文本进行 claims 审查、追问准备和保守表达建议，不能视为代码级项目复盘、源码教学或仓库证据分析。

It may include only extracted claims, unverified claims, likely follow-ups, repository evidence needed, conservative wording, and a supplementary-materials checklist.

It must not invent repository structure, core files, entry points, runtime/data/API flows, module implementation, code-reading routes, repository evidence matrices, verified architecture, deployment/testing/monitoring maturity, technical depth, or personal contribution.

Use `仅简历声称`, `仅用户背景声称`, `待仓库验证`, `证据不足`, or `不应声称` as appropriate. If a repository later becomes available, switch to the matching full mode and begin with reconnaissance; do not treat the fallback text as evidence.
