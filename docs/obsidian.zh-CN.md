# Obsidian 导出建议

Obsidian Markdown 在 v2 中是学习结果的导出，不是 self-learning 的默认首轮输出。

## 建议导出时机

- 完成一条代表性 Runtime Flow；
- 完成一个或多个核心模块；
- 面试前最后复习；
- 用户主动要求保存学习笔记。

## 推荐结构

```text
Projects/project-name/
├── 00-Mental-Model-and-Architecture.md
├── 01-Runtime-Flow.md
├── 02-Core-Modules-and-Source-References.md
├── 03-Mastery-and-Knowledge-Gaps.md
├── 04-Interview-Readiness.md
└── 05-Claims-and-Evidence.md
```

导出应区分：仓库事实、推断、通用概念、助手已经讲过的内容，以及用户已经证明掌握的内容。

## Checklist

```markdown
- [ ] 我能指出程序入口与关键 symbol
- [ ] 我能不看笔记 trace 一条真实请求
- [ ] 我能解释核心模块的输入、输出、状态与依赖
- [ ] 我能定位一个小修改涉及的文件
- [ ] 我能说明一个失败场景与 Debug 路线
- [ ] 我知道哪些 claims 证据不足
```

保留证据矩阵与 Mastery Summary 表格，便于复习时快速区分“能讲”“待补学”和“不应声称”。
