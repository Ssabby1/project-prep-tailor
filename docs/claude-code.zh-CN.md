# Claude Code 使用说明

当前仓库提供原生 Skill 规则和一个独立 fallback prompt。原生 Skill 不可用时，可把 `project-prep-tailor/references/prompt.md` 放入 Claude Code command。

## 交互学习

在目标项目仓库中输入：

```text
请按 project-prep-tailor v2 的规则带我从 0 理解当前仓库。
先做 Repository Reconnaissance，再 trace 一条真实 End-to-End Runtime Flow。
之后一次教一个模块，每次让我完成预测、导航、复述、修改或 Debug 练习之一；不要一开始生成完整长文。
```

## Mock Interview

```text
/project-prep-tailor Mode: Interview
请一次问一题。答案不准确或空泛时，回到相关 path::symbol 补学并让我重答。
JD: ...
Resume: ...
```

## 导出

学习后可要求导出 Obsidian Markdown；导出应保留 Runtime Flow、源码锚点、Mastery Summary、知识缺口和 claim 风险。

没有仓库时只能生成 no-repo claim audit，不能虚构项目结构或实现。
