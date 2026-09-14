# 从 0 交互学习示例

## 场景

用户有项目仓库，但项目大量由 AI 辅助生成，只知道大概能运行。目标是掌握后端 API、数据模型和任务/Agent 主流程。

## Prompt

```text
Use $project-prep-tailor to teach me this repository from zero.
Scenario: self-learning
Mode: Deep Tutor
Learning goal: 理解后端 API、数据库模型和任务 / Agent 运行链。

请先扫描仓库并 trace 一条真实请求；之后一次教一个模块，检查我的理解，
并让我做至少一个小型修改规划和一个 Debug 练习。暂时不要生成完整学习文档。
```

## 预期首轮行为

- 给出简洁 Project Mental Model；
- 用仓库证据说明 Architecture 与 Entry Points；
- 输出按 Core / Important / Supporting / Infrastructure / Generated / Low Priority 分类的 Repository Map；
- trace 一条代表性的真实 Runtime Flow；
- 按依赖、运行顺序和难度提出 Learning Roadmap；
- 直接开始第一教学单元；
- 以一个 Prediction、Code Navigation 或 Explain Back 问题结束，等待用户回答。

不应在首轮一次性输出所有模块讲解、所有练习答案和完整 Obsidian 文档。

## 交互片段

```text
[Repo Fact] `src/api/tasks.py::create_task` 接收并校验请求，再调用 `TaskService.create`。
[General Concept] API 层负责传输协议，service 层负责应用流程。
[Inference] 这种分层可能便于单元测试，但仓库没有设计文档直接说明动机。

问题：如果请求校验成功，但任务没有进入执行器，你会沿着这条 flow 先查哪两个 symbol？先不要看答案。
```

用户回答后，Skill 应判断遗漏、回到源码补充、让用户重新解释，并更新掌握度；不是立刻替用户写一个漂亮答案。

## 学习后导出

用户主动要求时，再导出 Runtime Flow、关键源码、模块理解、练习结果、Mastery Summary、Remaining Gaps 与 Interview Readiness。
