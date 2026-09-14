# project-prep-tailor

[English](README.md)

`project-prep-tailor` v2 是一个基于真实代码仓库的交互式项目导师与项目准备 Skill。它先帮助用户真正理解项目，再用于面试、JD/简历对齐、论文答辩、公司项目 review、onboarding，以及 AI 辅助项目的诚实表达。

## v2 的核心变化

在 `self-learning` / `from-zero` 场景下，默认不再一开始生成完整项目复盘 Markdown，而是进入渐进式教学：

```text
Repository Reconnaissance
→ Architecture 与 Entry Points
→ 一条真实 End-to-End Runtime Flow
→ 基于依赖与运行顺序的 Learning Roadmap
→ 单模块教学
→ 理解检查与小型修改 / Debug 练习
→ Interview
→ 按需导出 Markdown / Obsidian
```

核心原则仍是 repo-first、evidence-first，并进一步要求区分：

- `[Repo Fact]`：仓库可直接确认，尽量引用文件、Symbol 和可靠行号；
- `[Inference]`：基于源码结构的合理推断；
- `[General Concept]`：与当前源码相关的通用知识。

原有证据等级继续用于简历、业务、归属、成熟度和影响 claims，避免把推测、依赖或目录名称包装成已实现事实。

## 两个互补目标

- **Project Mastery**：理解项目目的、架构、入口、真实运行链、核心模块、依赖、AI/RAG/Agent/Tool 的实际实现、限制、修改点和 Debug 路线。
- **Project Preparation**：在理解基础上准备交互式面试、JD 对齐、简历 claim 审核、论文答辩、公司 review 与 AI 辅助项目说明。

不变的总原则是：**先理解，再表达。**

## 会话模式

- `Quick Tutor`：快速建立项目心智模型、Repository Map、5–10 个核心文件、一条真实运行链、关键取舍与理解检查。
- `Deep Tutor`：完整渐进教学、真实代码阅读、主动练习与掌握度追踪。
- `Interview`：一次一题的 Mock Interview；回答出现缺口时自动回到 Tutor Mode 补学，再重新回答。

旧参数 `quick`、`standard`、`deep`、`from-zero` 保持兼容。`self-learning` / `from-zero` 默认进入 Deep Tutor；明确面试请求默认进入 Interview。

## 输入与场景兼容性

仍支持：

- `repo-only`
- `repo + learning goal`
- `repo + resume`
- `repo + JD`
- `repo + JD + resume`
- `repo + thesis / defense requirement`
- `repo + company context`

场景仍包括 `repo-review`、`self-learning`、`interview`、`thesis-defense`、`company-review`。

没有仓库时仍只能进行 no-repo claim audit，不能编造目录、核心文件、运行链、模块实现、部署成熟度、技术深度或个人贡献。

## 使用示例

从 0 交互学习：

```text
Use $project-prep-tailor to teach me this repository from zero.
先 trace 一条真实请求，再按模块教我；每个阶段都检查我的理解。
Learning goal: 理解后端 API 和 Agent Tool 执行链。
```

面试训练：

```text
Use $project-prep-tailor to run an evidence-grounded mock interview for this repository.
请一次问一题；如果我的答案空泛，带我回到源码补学后再答。
JD: ...
Resume project text: ...
```

学习后导出：

```text
把当前学习结果导出成 Obsidian Markdown，包含 Runtime Flow、关键源码、Mastery Summary、Remaining Gaps 和 Interview Readiness。
```

详见 [docs/usage.zh-CN.md](docs/usage.zh-CN.md)、[docs/codex.zh-CN.md](docs/codex.zh-CN.md)、[docs/claude-code.zh-CN.md](docs/claude-code.zh-CN.md) 与 [docs/cursor.zh-CN.md](docs/cursor.zh-CN.md)。

## Skill 文件结构

Skill 本体仍保持扁平结构，原有场景文件不迁移；v2 新增：

```text
project-prep-tailor/
├── SKILL.md
├── reconnaissance.md
├── runtime_flow.md
├── module_tutor.md
├── active_learning.md
├── mastery_tracking.md
├── interview_mode.md
├── input_modes.md
├── output_contract.md
├── depth_modes.md
├── evidence_rules.md
├── repo_evidence.md
├── resume_claims.md
├── jd_analysis.md
├── defense_prep.md
├── company_review_prep.md
├── self_learning.md
├── ai_assisted_project.md
├── question_bank.md
└── safety_rules.md
```

v2 暂不加入 Tree-sitter、AST service、数据库、持久化学习状态、Web UI 或模型调用 CLI；当前价值来自更可靠的教学与准备工作流。
