# 公司项目汇报示例

## 使用场景

用户有：
- 项目仓库
- 公司项目背景
- 自己负责的内容
- 汇报目标

目标是准备项目 review、实习转正答辩或内部技术汇报。

## 示例 Prompt

```text
Use $project-prep-tailor to prepare a company-review document for this repository.

Scenario: company-review
Depth: standard
Output format: Obsidian-friendly Markdown

Company context:
这是一个内部工单分析工具，我主要负责后端接口、数据清洗和报表查询模块。汇报对象是导师和技术负责人，目标是说明我完成了哪些模块、遇到哪些问题、后续如何优化。
```

## 期望输出重点

- 项目背景
- 输入信息和仓库证据区分
- 用户负责范围
- 已交付模块
- 技术栈和核心文件
- 关键流程
- 技术取舍
- 风险和 blocker
- 后续计划
- 可能被问的问题
- 需要公司侧数据证明的内容

## 业务指标边界示例

如果用户说“提升了处理效率”，但仓库没有 benchmark 或业务数据，不应写：

```text
将工单处理效率提升 50%。
```

应写：

```text
用户背景中提到该工具用于提升处理效率，但当前仓库只能证明相关技术模块实现，具体效率提升需要业务数据、日志或评估报告支持。
```
