# Data Analysis Prompt Template

Use this prompt to ask an AI agent to analyze tabular data or metrics.

```markdown
Act as a data analyst. Analyze the following dataset or metrics and produce decision-ready insights.

Context:
- Business question: [question]
- Dataset: [file, table, or pasted data]
- Time range: [date range]
- Important definitions: [metric definitions]
- Audience: [who will read the analysis]

Analysis requirements:
- Validate the data before drawing conclusions.
- Identify missing values, outliers, and possible data quality issues.
- Separate facts from interpretation.
- Use concrete numbers, percentages, and comparisons.
- Do not invent data that is not present.

Output:
## Executive Summary
[3-5 bullets]

## Data Quality Notes
- [Issue or confirmation]

## Key Findings
| Finding | Evidence | Impact |
| --- | --- | --- |

## Recommended Actions
1. [Action and reason]

## Follow-up Questions
- [Question]

Data:
[paste data or describe file]
```

## 中文版

```markdown
请你作为数据分析师，分析下面的数据或指标，并输出可支持决策的洞察。

背景：
- 业务问题：[问题]
- 数据集：[文件、表格或粘贴数据]
- 时间范围：[日期范围]
- 重要定义：[指标定义]
- 读者：[谁会看这份分析]

分析要求：
- 在下结论前先检查数据质量。
- 识别缺失值、异常值和潜在数据问题。
- 区分事实和解读。
- 使用具体数字、百分比和对比。
- 不要编造不存在的数据。

输出：
## 摘要
[3-5 条要点]

## 数据质量说明
- [问题或确认]

## 关键发现
| 发现 | 证据 | 影响 |
| --- | --- | --- |

## 建议行动
1. [行动和原因]

## 后续问题
- [问题]

数据：
[粘贴数据或描述文件]
```
