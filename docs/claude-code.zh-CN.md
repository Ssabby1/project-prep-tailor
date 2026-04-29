# Claude Code 使用说明

当前版本不提供安装 CLI。可以使用 `project-prep-tailor/project-prep-tailor/references/prompt.md` 作为 slash command 或直接复制到 Claude Code 对话中。

## 直接使用

在目标项目仓库中打开 Claude Code，然后输入：

```text
请读取 project-prep-tailor 的规则，尤其是 SKILL.md、input_modes.md、output_contract.md、depth_modes.md 和 evidence_rules.md。

请分析当前仓库，生成 detailed Obsidian-friendly Markdown 项目复盘文档。
Scenario: repo-review
Depth: standard
```

## 建议配置为 slash command

可以把 `references/prompt.md` 的内容放入 Claude Code command，例如：

```text
~/.claude/commands/project-prep-tailor.md
```

使用时：

```text
/project-prep-tailor Scenario: interview Depth: deep JD: ...
```

## no-repo fallback

如果没有仓库，只能生成 claims 审查、追问清单和保守话术，不能生成完整项目复盘。
