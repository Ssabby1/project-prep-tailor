# 使用说明

`project-prep-tailor` 是一个 lite skill。当前版本不需要安装客户端，也不需要配置模型 API。

## 推荐使用方式

在 Codex、Claude Code、Cursor 等工具中，让 AI 读取：

- `project-prep-tailor/SKILL.md`
- 按需读取相关规则文件
- 对目标项目仓库进行分析

## 推荐输入

完整复盘请提供项目仓库。

可选上下文：
- 学习目标
- 简历项目经历
- 岗位 JD
- 论文题目 / 摘要 / 答辩要求
- 公司项目背景 / 负责内容 / 汇报目标

## 推荐 Prompt

```text
Use $project-prep-tailor to generate a detailed Markdown project prep document.
Scenario: interview
Depth: standard
Output format: Obsidian-friendly Markdown

Please analyze the current repository first.

JD:
...

Resume project text:
...
```

## 输出深度

- `quick`：快速复习
- `standard`：默认详尽复盘
- `deep`：深度技术复盘
- `from-zero`：从 0 学项目

## no-repo fallback

如果没有仓库，只能做 claim audit。不要要求它生成完整项目复盘。

fallback 适合：
- 审查简历 claims
- 生成可能追问
- 标记需要仓库验证的点
- 给出保守表达建议

fallback 不适合：
- 目录结构分析
- 核心文件分析
- 数据流分析
- 模块实现复盘
- 代码阅读路线
