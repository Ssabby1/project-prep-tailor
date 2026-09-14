# Cursor 使用说明

可将 `project-prep-tailor/references/prompt.md` 配置为 Cursor project rule，或在 Agent 中直接引用 Skill 文件。

## Project Rule 描述

```text
Use this rule for repository-grounded interactive project learning and preparation. For self-learning, trace a real runtime flow first, teach one module at a time, test the user's understanding, and export notes only when requested.
```

## 使用示例

```text
Use project-prep-tailor in Deep Tutor mode for this repository.
先给我 Repository Map 和一条真实运行链，然后开始第一个模块；
不要一次性生成全部学习文档，也不要马上给出练习答案。
```

面试时改用 `Mode: Interview`，一次问一题；发现缺口时先回到源码教学。

没有仓库时只能做 claim audit，不得生成虚构的目录、入口、运行链或模块实现。
