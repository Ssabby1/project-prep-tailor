# project-prep-tailor

[English](README.md)

`project-prep-tailor` 是一个 lite skill，用于生成 evidence-first 的项目复盘、学习、面试、答辩和公司项目汇报准备文档。

它默认输出详尽的 Markdown，适合放进 Obsidian 阅读和复习。

## 项目定位

这个 skill 帮助你基于项目仓库和可选上下文，真正理解项目，并准备把项目讲清楚。

支持的上下文包括：
- 学习目标
- 简历项目经历
- 岗位 JD
- 论文题目、摘要或答辩要求
- 公司项目背景、个人负责内容或汇报目标

核心原则：
- repo-first：完整项目复盘必须基于仓库
- evidence-first：能力、实现、技术点和结果都要尽量有证据
- 不夸大：不编造业务指标、上线结果、性能提升、用户规模、技术深度或个人贡献
- 对 AI 辅助 / vibecoding 项目，要帮助用户诚实理解和表达

## 和 repo-to-resume-tailor 的关系

`repo-to-resume-tailor` 解决的是：

```text
仓库 + 目标岗位 / JD -> 简历项目描述
```

`project-prep-tailor` 解决的是：

```text
仓库 + 可选上下文 -> 项目复盘、学习、面试、答辩或汇报准备文档
```

前者用于把项目写进简历，后者用于面试、答辩、汇报或自学前把项目讲清楚。

## 当前阶段：lite skill

第一版不包含：
- 客户端
- Web UI
- 需要用户配置 API key 的独立生成 CLI
- 模型调用逻辑
- `pyproject.toml`
- `install.py`
- `src/`

你可以直接在 Codex、Claude Code、Cursor 或其他 AI coding 工具中使用这个 skill / prompt 包。

## 主输入模式

完整项目复盘模式必须包含项目仓库：

- `repo-only`：项目理解、repo onboarding、从 0 学习文档
- `repo + learning goal`：按学习目标生成学习路线和模块阅读顺序
- `repo + resume`：对齐简历 claims 与仓库证据
- `repo + JD`：按岗位要求复盘项目
- `repo + JD + resume`：技术面试准备主模式
- `repo + thesis / defense requirement`：论文、毕设、课程设计答辩
- `repo + company context`：公司项目汇报、实习转正答辩、项目 review

## no-repo fallback

没有仓库时，只能做 claim audit，不是完整项目复盘。

fallback 支持：
- `resume-only fallback`
- `JD + resume fallback`

fallback 只能输出：
- 输入文本中的 claims
- 无法验证的 claims
- 可能追问
- 需要仓库验证的点
- 保守表达建议
- 补充材料清单

fallback 不能输出：
- 目录结构
- 核心文件
- 数据流
- 接口流
- 代码阅读路线
- 仓库证据矩阵
- 模块实现细节
- 已验证技术深度

## 支持场景

- `interview`：技术面试准备
- `thesis-defense`：论文 / 毕设 / 课程设计答辩
- `company-review`：公司项目汇报 / 实习转正答辩 / 项目 review
- `self-learning`：从 0 学习项目
- `repo-review`：通用仓库复盘和 onboarding

## 输出深度

- `quick`：快速复习
- `standard`：默认，详尽但不过度展开
- `deep`：深度技术复盘
- `from-zero`：从 0 学项目，强调概念解释、阅读路线、练习任务和自测问题

## 使用示例

在项目仓库目录中：

```text
Use $project-prep-tailor to generate a standard repo-review document for this repository.
```

面试准备：

```text
Use $project-prep-tailor to prepare this project for interview.
Scenario: interview
Depth: deep
JD:
...
Resume project text:
...
```

从 0 学项目：

```text
Use $project-prep-tailor to help me learn this repository from zero.
Scenario: self-learning
Depth: from-zero
Learning goal: understand the backend API flow and database model.
```

答辩准备：

```text
Use $project-prep-tailor to prepare a thesis-defense document.
Depth: deep
Defense requirement:
...
```

公司汇报：

```text
Use $project-prep-tailor to prepare a company-review document.
Company context:
...
```

## Obsidian 建议

默认输出已经适合 Obsidian：
- 使用清晰的 Markdown 标题层级
- 使用表格记录 evidence matrix
- 使用 checklist 做复习追踪
- 使用“需要补学”和“不建议主动强调”管理风险

详见 [docs/obsidian.zh-CN.md](docs/obsidian.zh-CN.md)。

## 文件结构

```text
project-prep-tailor/
├── README.md
├── README.zh-CN.md
├── project-prep-tailor/
│   ├── SKILL.md
│   ├── input_modes.md
│   ├── output_contract.md
│   ├── depth_modes.md
│   ├── evidence_rules.md
│   ├── repo_evidence.md
│   ├── resume_claims.md
│   ├── jd_analysis.md
│   ├── defense_prep.md
│   ├── company_review_prep.md
│   ├── self_learning.md
│   ├── ai_assisted_project.md
│   ├── question_bank.md
│   ├── safety_rules.md
│   └── references/
│       ├── prompt.md
│       └── examples.md
├── examples/
└── docs/
```

## Roadmap

后续可以增加安装 CLI，但 CLI 只负责安装 skill，不负责调用模型 API。

可能的后续命令：

```bash
project-prep-tailor init --ai codex
project-prep-tailor init --ai claude-code
project-prep-tailor init --ai cursor --project /path/to/project
```

客户端、Web UI、API 模型调用、自动保存到 Obsidian vault 等能力都属于后续增强，不进入 MVP。
