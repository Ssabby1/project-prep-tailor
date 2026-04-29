# 面试准备示例

## 使用场景

用户有：
- 项目仓库
- 岗位 JD
- 简历项目经历

目标是生成技术面试前的项目复盘文档。

## 示例 Prompt

```text
Use $project-prep-tailor to prepare this repository for technical interview.

Scenario: interview
Depth: deep
Output format: Obsidian-friendly Markdown

JD:
我们招聘 AI 应用开发工程师，要求熟悉 Python、FastAPI、RAG、向量数据库、LLM API 调用、Prompt 工程和工程化部署。

Resume project text:
基于 FastAPI 和 LangChain 实现智能知识库问答系统，支持文档解析、向量检索、RAG 问答和多轮对话，优化回答准确率和响应速度。
```

## 期望输出重点

完整模式必须先分析仓库，然后输出：

- 输入与证据范围
- JD 要求拆解
- 简历 claims 抽取
- 仓库结构与核心文件
- RAG / API / 数据流证据
- JD / resume / repo 三方矩阵
- 30 秒项目讲述
- 2 分钟项目讲述
- 高频追问
- 需要补学的知识点
- AI 辅助项目理解检查
- 不建议主动强调的 claims

## 风险处理示例

如果仓库只看到 `langchain` 依赖，但没有完整 retriever、embedding、vector store 和 query flow，不应写：

```text
完整实现了生产级 RAG 引擎。
```

应写：

```text
仓库存在 RAG 相关依赖或部分模块，但完整检索链路证据不足。面试中可以准备 RAG 原理和项目意图，不建议主动强调生产级完整实现。
```
