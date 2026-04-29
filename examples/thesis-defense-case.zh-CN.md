# 论文 / 毕设答辩示例

## 使用场景

用户有：
- 项目仓库
- 论文题目或摘要
- 答辩要求

目标是准备答辩文档和答辩问答。

## 示例 Prompt

```text
Use $project-prep-tailor to prepare a thesis-defense document for this repository.

Scenario: thesis-defense
Depth: deep
Output format: Obsidian-friendly Markdown

Thesis title:
基于大语言模型的企业知识库问答系统设计与实现

Defense requirement:
需要说明研究背景、系统需求、系统设计、核心实现、测试验证、创新点和不足。
```

## 期望输出重点

- 输入与证据范围
- 论文题目和项目仓库的对应关系
- 问题定义
- 系统需求
- 系统架构
- 核心模块说明
- 数据流或问答流程
- 测试或验证证据
- 创新点边界
- 不足与未来工作
- 答辩问题库

## 创新点边界示例

如果仓库只是集成现有 LLM API 和向量库，不应写：

```text
本文提出了一种全新的大语言模型推理算法。
```

应写：

```text
本项目的实践重点是将 LLM API、文档处理和向量检索整合为知识库问答系统；当前仓库证据不支持原创模型算法层面的创新。
```
