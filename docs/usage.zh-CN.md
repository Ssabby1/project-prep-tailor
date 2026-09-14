# 使用说明

`project-prep-tailor` v2 默认把自学请求作为交互教学，而不是一次性项目复盘文档生成。

## 推荐输入

代码级教学和准备必须提供可读取的项目仓库。可选上下文包括学习目标、简历项目经历、岗位 JD、论文/答辩要求、公司背景、个人负责范围和汇报目标。

## 从 0 学项目

```text
Use $project-prep-tailor to teach me this repository from zero.
Mode: Deep Tutor
Learning goal: 理解后端请求流、数据模型和任务处理。

请先做 Repository Reconnaissance，找到一条真实 End-to-End Runtime Flow，
再一次教一个模块，并通过预测、代码导航、复述、修改或 Debug 练习检查我的理解。
```

Skill 会先给出简洁的心智模型、架构、入口、Repository Map、真实运行链和学习路线，然后直接开始第一单元并等待用户回答。不会默认把全部课程和答案一次性铺开。

## 快速理解

```text
Use $project-prep-tailor in Quick Tutor mode.
我只有 30 分钟，请先讲项目目的、核心入口、一条真实主流程、5–10 个核心文件、主要风险与面试重点，并检查一次我的理解。
```

## 交互式面试

```text
Use $project-prep-tailor to run a source-grounded mock interview.
请一次问一题，检查我的答案是否准确、是否空泛、是否超出仓库证据；
如果有知识缺口，回到源码补学，再让我重新回答。

JD: ...
Resume project text: ...
```

## 导出笔记

学习完成或需要复习时再说：

```text
把当前学习结果导出成 Obsidian-friendly Markdown。
包含 Project Mental Model、Architecture、Runtime Flow、Key Source References、
Mastery Summary、Remaining Knowledge Gaps 和 Interview Readiness。
```

旧的 `quick`、`standard`、`deep`、`from-zero` 输入仍兼容；但 `from-zero` 会按 Deep Tutor 运行，`standard` 不会把 self-learning 强制变成一篇长文。

## no-repo fallback

没有仓库时只能做 claim audit：提取 claims、标记无法验证项、准备追问、列出需要的仓库证据并给出保守措辞。不能输出虚构的目录、文件、入口、运行链、模块实现或仓库证据矩阵。
