# Codex 使用说明

## 作为 Codex Skill 使用

把 Skill 本体目录放入 Codex skills 目录后，可直接调用 `$project-prep-tailor`。在本仓库开发时，也可以让 Codex 读取 `project-prep-tailor/SKILL.md`。

## 从 0 交互教学

```text
Use $project-prep-tailor to teach me the current repository from zero.
Mode: Deep Tutor
Learning goal: 理解核心后端和 Agent Tool runtime flow。

先扫描仓库并给出 Repository Map，trace 一条真实请求；
随后一次教一个模块，引用 path::symbol，并在每个阶段让我回答一个问题。
```

预期首轮是项目心智模型、架构、入口、优先级地图、代表性运行链、学习路线和第一道练习，不是完整 Obsidian 文档。

## 交互式面试

```text
Use $project-prep-tailor to run an evidence-grounded mock interview for this repository.
一次问一题。检查我的答案是否符合源码和 claim 边界；有缺口时回源码补学，再让我重答。

JD: ...
Resume project text: ...
```

## 请求导出

```text
Export the current learning state as Obsidian-friendly Markdown.
Include runtime flow, source anchors, mastery summary, remaining gaps, and interview readiness.
```

## 兼容与限制

旧参数 `quick`、`standard`、`deep`、`from-zero` 保持有效。完整源码教学必须能读取仓库；没有仓库时只能做 no-repo claim audit。
