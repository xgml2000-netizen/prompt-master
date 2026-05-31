# Before and After Examples

## Example 1: Code Review

Before:

```text
Review this code and tell me if it is good.
```

After:

```text
Act as a senior code reviewer. Review the following code for correctness, security, maintainability, and missing tests.

Prioritize actionable issues. For each finding, include severity, location, why it matters, and a suggested fix. Do not comment on style unless it affects correctness or long-term maintenance.

If there are no serious issues, say that clearly and list any remaining test gaps.

Code:
[paste code]
```

Why it is better:

- Defines the reviewer's role
- Names review criteria
- Sets priority and output expectations
- Prevents low-value style-only feedback

## Example 2: Research

Before:

```text
Tell me about AI coding tools.
```

After:

```text
Create a concise research brief comparing current AI coding tools for a solo developer choosing a daily coding assistant.

Scope:
- Include: OpenAI Codex, GitHub Copilot, Cursor, Claude Code, and other notable tools if relevant
- Focus on: coding workflow, repository understanding, terminal integration, review quality, and pricing
- Time sensitivity: use current information and include dates for product claims

Output:
## Summary
[3-5 bullets]

## Comparison Table
| Tool | Strengths | Weaknesses | Best For | Notes |

## Recommendation
[Clear recommendation with caveats]
```

Why it is better:

- Defines the decision being supported
- Names tools and comparison criteria
- Requires current, dated information
- Produces a useful decision format

## Example 3: Translation

Before:

```text
Translate this prompt into English.
```

After:

```text
Translate the following Chinese prompt into English for use as an AI system prompt.

Rules:
- Preserve headings, bullets, placeholders, and code blocks.
- Do not translate API names, file paths, command flags, or code identifiers.
- Keep constraints and negative instructions precise.
- Use natural English instructions, not literal word-for-word translation.

Output:
## Translation
[translated prompt]

## Notes
[only include if something is ambiguous]

Prompt:
[paste prompt]
```

Why it is better:

- Protects technical terms
- Preserves prompt structure
- Clarifies target usage
- Allows ambiguity notes without polluting the translation

## Example 4: Agent Task Execution

Before:

```text
Add login to my app.
```

After:

```text
Act as a full-stack engineer. Add a login feature to the existing app while preserving current behavior and project conventions.

Before coding:
1. Inspect the existing framework, routing, auth-related files, and data model.
2. Identify whether an auth library is already present.
3. Summarize the smallest safe implementation plan.

Requirements:
- Support email/password login.
- Add logout.
- Protect authenticated-only pages.
- Show clear error states for invalid credentials.
- Do not introduce a new auth framework if the project already has one.

Output:
## Plan
[Short plan]

## Changes
[Files and behavior changed]

## Verification
[Tests or manual checks performed]

## Follow-up
[Security or UX improvements not included]
```

Why it is better:

- Requires project inspection before implementation
- Prevents unnecessary framework changes
- Defines feature scope
- Requires verification

## Example 5: Chinese Daily Report

Before:

```text
帮我生成日报。
```

After:

```text
请你作为业务分析助理，根据我提供的原始信息生成一份适合发给团队的日报。

背景：
- 读者：[团队/直属领导/客户]
- 语气：[正式/简洁/轻松]
- 今日重点：[今天最重要的目标]

要求：
- 只基于我提供的信息写，不要编造数据。
- 先写关键进展，再写风险和明日计划。
- 风险要附带建议下一步。
- 控制在 300 字以内。

输出格式：
## 今日进展
- [要点]

## 风险与阻塞
- [要点 + 建议下一步]

## 明日计划
- [要点]

原始信息：
[粘贴内容]
```

Why it is better:

- Defines audience and tone
- Prevents fabricated information
- Creates a stable report structure
- Makes blockers actionable

## Example 6: Prompt Review

Before:

```text
Is this prompt good?
```

After:

```text
Review the following prompt using a prompt engineering rubric.

Evaluate:
- Goal clarity
- Context completeness
- Role usefulness
- Task specificity
- Constraint quality
- Output format
- Examples
- Verification criteria
- Reusability

Output:
## Scorecard
| Dimension | Score 1-5 | Note |
| --- | ---: | --- |

## Highest-Impact Fixes
1. [Fix]
2. [Fix]
3. [Fix]

## Revised Prompt
[Copy-ready improved prompt]

Prompt:
[paste prompt]
```

Why it is better:

- Turns taste into evaluation criteria
- Prioritizes fixes
- Produces an improved prompt, not only comments
