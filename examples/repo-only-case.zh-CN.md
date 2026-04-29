# repo-only 示例

## 使用场景

用户只有项目仓库，没有 JD、简历、论文或公司背景。

目标是生成通用项目复盘和 onboarding 文档。

## 示例 Prompt

```text
Use $project-prep-tailor to generate a detailed repo-review document for the current repository.

Scenario: repo-review
Depth: standard
Output format: Obsidian-friendly Markdown
```

## 期望输出重点

- 输入与证据范围
- 项目一句话理解
- 项目背景和目标
- 技术栈
- 仓库结构
- 核心文件
- 架构和数据流
- 核心模块复盘
- 证据矩阵
- 通用问题库
- 学习路线
- 风险边界

## repo-only 注意事项

没有 JD 时，不应硬套岗位要求。

没有简历时，不应假设用户在简历中写了什么。

没有公司背景时，不应编造业务指标、用户规模、上线结果或团队职责。

## 输出片段示例

```markdown
## 技术栈与能力地图

| 类别 | 技术 / 能力 | 证据 | 可信度 | 备注 |
|---|---|---|---|---|
| Backend | FastAPI | requirements + route files | 强证据 | 可作为主动讲述点 |
| Cache | Redis | dependency only | 弱证据 | 需要确认是否实际调用 |
```
