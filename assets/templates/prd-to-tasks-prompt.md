# PRD to Implementation Tasks Prompt

Use this prompt to convert product requirements into engineering work.

```markdown
Act as a product-minded engineering lead. Convert the following product requirement into an implementation-ready plan.

Context:
- Product: [product]
- Target users: [users]
- Stack: [frontend/backend/database/infrastructure]
- Existing constraints: [auth, permissions, data model, design system, deadlines]

Requirements:
[paste PRD or feature description]

Your job:
1. Extract the user goal and business goal.
2. Identify user flows and edge cases.
3. Propose a technical implementation plan.
4. Break the work into small tasks.
5. List tests and rollout risks.

Output:
## Summary
[Short feature summary]

## User Stories
- As a [user], I want [goal], so that [benefit].

## Scope
### In Scope
- [Item]

### Out of Scope
- [Item]

## Technical Plan
### Frontend
- [Task]

### Backend
- [Task]

### Data Model
| Field | Type | Notes |
| --- | --- | --- |

## Edge Cases
- [Case]

## Implementation Tasks
1. [Task]

## Tests
- [Test]

## Rollout Risks
- [Risk and mitigation]
```

## 中文版

```markdown
请你作为兼具产品意识的技术负责人，把下面的产品需求转化为可执行的研发计划。

背景：
- 产品：[产品]
- 目标用户：[用户]
- 技术栈：[前端/后端/数据库/基础设施]
- 现有限制：[权限、数据模型、设计系统、截止时间等]

需求：
[粘贴 PRD 或功能描述]

你的任务：
1. 提取用户目标和业务目标。
2. 识别用户流程和边界情况。
3. 提出技术实现方案。
4. 拆分成小任务。
5. 列出测试和上线风险。

输出：
## 摘要
[功能简述]

## 用户故事
- 作为[用户]，我希望[目标]，以便[收益]。

## 范围
### 范围内
- [事项]

### 范围外
- [事项]

## 技术方案
### 前端
- [任务]

### 后端
- [任务]

### 数据模型
| 字段 | 类型 | 说明 |
| --- | --- | --- |

## 边界情况
- [情况]

## 实施任务
1. [任务]

## 测试
- [测试]

## 上线风险
- [风险和缓解方案]
```
