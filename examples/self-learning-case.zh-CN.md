# 从 0 学项目示例

## 使用场景

用户有：
- 项目仓库
- 学习目标

目标是从 0 理解项目，而不是直接准备面试话术。

## 示例 Prompt

```text
Use $project-prep-tailor to help me learn this repository from zero.

Scenario: self-learning
Depth: from-zero
Output format: Obsidian-friendly Markdown

Learning goal:
我想理解这个项目的后端 API 流程、数据库模型和任务处理逻辑。我是初学者，请给出阅读顺序、概念解释、练习任务和自测问题。
```

## 期望输出重点

- 项目一句话理解
- 前置概念地图
- 仓库阅读顺序
- 核心文件说明
- API 流程
- 数据模型
- 任务处理逻辑
- 每一步要理解什么
- 小练习
- 自测问题
- 暂时可以跳过的文件

## from-zero 输出片段示例

```markdown
## 从 0 学习路线

| Step | Goal | Files | What To Understand | Self-Check |
|---|---|---|---|---|
| 1 | 理解项目启动方式 | README, main entry | 项目如何运行 | 我能否说清服务如何启动 |
| 2 | 理解 API 入口 | routes/controllers | 请求如何进入系统 | 我能否画出一个接口调用链 |
```

## AI 辅助项目提示

如果项目是 AI 辅助完成，输出中应加入：
- 哪些模块必须亲自理解
- 哪些代码可以通过小修改验证理解
- 哪些 claims 在理解前不应主动说
