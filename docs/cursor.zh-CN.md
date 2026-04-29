# Cursor 使用说明

当前版本不提供安装 CLI。可以把 `references/prompt.md` 配置为 Cursor project rule，或直接在 Agent 中引用本 skill 文件。

## 作为 Project Rule

在目标项目中创建：

```text
.cursor/rules/project-prep-tailor.mdc
```

将 `project-prep-tailor/project-prep-tailor/references/prompt.md` 的内容复制进去。

建议补充 rule 描述：

```text
Use this rule when preparing project review, interview prep, thesis defense prep, company review, or self-learning documents from repository evidence.
```

## 使用示例

```text
Use project-prep-tailor to generate an Obsidian-friendly Markdown interview prep document.
Scenario: interview
Depth: standard

Please analyze this repository first.
```

## 重要限制

完整复盘必须基于仓库。没有仓库时，只能做 no-repo fallback claim audit。
