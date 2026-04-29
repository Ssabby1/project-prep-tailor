# Codex 使用说明

## 当前版本定位

`project-prep-tailor` 当前是 lite skill，不提供安装 CLI。你可以通过手动放置 skill 目录，或在当前仓库中直接让 Codex 读取 skill 文件来使用。

## 方式一：在本仓库中直接使用

在 Codex 中打开包含 `project-prep-tailor/` 的工作区，然后对 Codex 说：

```text
请使用 project-prep-tailor/project-prep-tailor/SKILL.md 的规则，分析当前项目仓库，生成一个 Obsidian-friendly Markdown 项目复盘文档。

Scenario: repo-review
Depth: standard
```

如果要分析另一个项目仓库，请在该仓库目录中运行 Codex，或者明确提供项目路径。

## 方式二：作为 Codex skill 使用

可以把 skill 本体目录复制到 Codex skills 目录：

```text
~/.codex/skills/project-prep-tailor/
```

目标目录应包含：

```text
SKILL.md
input_modes.md
output_contract.md
depth_modes.md
evidence_rules.md
repo_evidence.md
resume_claims.md
jd_analysis.md
defense_prep.md
company_review_prep.md
self_learning.md
ai_assisted_project.md
question_bank.md
safety_rules.md
references/prompt.md
references/examples.md
```

之后可以使用：

```text
Use $project-prep-tailor to prepare this repository for interview.
Scenario: interview
Depth: deep
```

## 推荐 Codex Prompt

### repo-only

```text
Use $project-prep-tailor to generate a detailed repo-review document for the current repository.
Depth: standard
Output: Obsidian-friendly Markdown
```

### 面试准备

```text
Use $project-prep-tailor to prepare this project for interview.
Scenario: interview
Depth: deep

JD:
...

Resume project text:
...
```

### 从 0 学项目

```text
Use $project-prep-tailor to help me learn this repository from zero.
Scenario: self-learning
Depth: from-zero
Learning goal: understand the core backend flow and data model.
```

## 注意事项

完整项目复盘必须有 repo。如果当前没有仓库，Codex 应先提示 no-repo fallback 限制。

no-repo fallback 不能生成目录结构、核心文件、数据流、接口流、代码阅读路线、仓库证据矩阵或模块实现细节。
