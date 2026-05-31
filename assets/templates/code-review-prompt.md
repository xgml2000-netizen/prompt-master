# Code Review Prompt Template

```markdown
Act as a senior code reviewer. Review the following change for correctness, security, maintainability, performance, and missing tests.

Context:
- Project: [project name]
- Stack: [languages/frameworks]
- Change goal: [what this change is supposed to do]
- Risk areas: [security, data migration, payments, auth, concurrency, etc.]

Review rules:
- Prioritize bugs, regressions, security risks, and missing tests.
- Do not comment on style unless it affects correctness or maintainability.
- If a concern is speculative, label it as a question or assumption.
- If no serious issues are found, say that clearly.

Output format:
## Findings
| Severity | Location | Issue | Suggested Fix |
| --- | --- | --- | --- |

## Questions
- [Open question, if any]

## Test Gaps
- [Missing test or verification, if any]

Code or diff:
[paste code or diff]
```

## 中文版

```markdown
请你作为资深代码审查者，检查下面的改动是否存在正确性、安全性、可维护性、性能和测试缺口问题。

背景：
- 项目：[项目名]
- 技术栈：[语言/框架]
- 改动目标：[这次改动要实现什么]
- 风险区域：[安全、数据迁移、支付、权限、并发等]

审查规则：
- 优先指出 bug、回归风险、安全风险和缺失测试。
- 除非影响正确性或可维护性，否则不要只评论代码风格。
- 如果问题只是推测，请标记为问题或假设。
- 如果没有严重问题，请明确说明。

输出格式：
## 问题
| 严重程度 | 位置 | 问题 | 建议修复 |
| --- | --- | --- | --- |

## 疑问
- [开放问题，如有]

## 测试缺口
- [缺失的测试或验证，如有]

代码或 diff：
[粘贴代码或 diff]
```
