# 源码闭环 Mock Interview 示例

## 场景

用户有项目仓库、目标 JD 和简历项目经历，希望准备技术面试。

## Prompt

```text
Use $project-prep-tailor to run an evidence-grounded mock interview for this repository.
Scenario: interview
Mode: Interview

一次问一题。请检查我的回答是否准确、是否只讲通用概念、是否超出 Repo Evidence；
发现缺口时回源码补学，再让我重新回答。

JD:
AI 应用开发工程师；Python、FastAPI、RAG、向量数据库、LLM API、部署。

Resume project text:
基于 FastAPI 和 LangChain 实现知识库问答，支持文档解析、向量检索和多轮对话，优化准确率和响应速度。
```

## 准备基线

Skill 应先用仓库确认项目目的、架构、入口、一条代表性运行链、JD 相关模块、简历 claims 和风险边界。如果用户尚不了解主流程，先短暂进入 Tutor Mode。

## 面试闭环

```text
Question → User Answer → Technical/Evidence Check → Gap
→ Source-grounded Tutor Unit → User Retries → Deeper Follow-up
```

例如，用户回答“使用 Agent 是因为更灵活”时，不应立刻润色。应指出缺少本项目的动态决策点、Agent/Tool 源码锚点和 deterministic workflow 对比，然后回到真实代码，补学后让用户重答。

## Claim 风险

如果仓库只有 `langchain` 依赖而没有完整 retriever、embedding、vector store 和 query flow，则不能把“完整 RAG”当事实。准确率和响应速度优化还需要 benchmark、评估或运行证据。

只有在用户证明理解后，才生成 30 秒 / 2 分钟项目讲述或最终复习导出；其范围不能超过仓库和用户背景证据。
