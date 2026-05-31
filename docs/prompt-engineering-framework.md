# Prompt Engineering Framework

Prompt Master uses **CRAFT-V** as its core method.

CRAFT-V means:

- Context
- Role
- Action
- Format
- Tests
- Verification

It is designed for prompts that need to be executed reliably by AI agents.

## C: Context

Context tells the model what situation it is operating in.

Good context includes:

- Project or domain
- User goal
- Audience
- Inputs
- Constraints
- Environment
- Time sensitivity
- Known risks

Weak:

```text
Write release notes.
```

Stronger:

```text
Write release notes for a developer tool release. The audience is existing users who want to know what changed, whether they need to migrate, and which bugs were fixed. Use the git diff and changelog entries as source material. Do not invent changes.
```

## R: Role

Role defines the perspective the model should use.

Good roles are functional, not decorative.

Weak:

```text
You are a genius writer.
```

Stronger:

```text
Act as a technical editor who improves clarity, preserves technical meaning, and removes unnecessary wording.
```

## A: Action

Action defines the exact work.

Good actions are observable:

- Review
- Rewrite
- Compare
- Extract
- Summarize
- Diagnose
- Generate
- Verify
- Rank
- Convert

Weak:

```text
Make this better.
```

Stronger:

```text
Rewrite this prompt to make the task, context, constraints, and output format explicit. Preserve the original intent and add placeholders for missing inputs.
```

## F: Format

Format reduces ambiguity and makes output easier to use.

Useful formats include:

- Markdown sections
- Tables
- JSON schemas
- Checklists
- Step-by-step plans
- Diff-style changes
- Scorecards

Example:

```text
Output:
## Diagnosis
- [Main issue]

## Revised Prompt
[Copy-ready prompt]

## Changes
| Change | Reason |
| --- | --- |
```

## T: Tests

Tests define success.

For prompts, tests can be:

- Expected output properties
- Must-include items
- Must-not-include items
- Edge cases
- Evaluation questions
- Example inputs and outputs

Example:

```text
The result is successful if:
- It includes exactly three options.
- Each option has pros, cons, and best-use case.
- It does not recommend tools outside the given budget.
```

## V: Verification

Verification tells the model what to check before finalizing.

Examples:

```text
Before answering, check whether every recommendation is supported by the provided source text.
```

```text
Before finalizing, verify that the JSON matches the requested schema and contains no comments.
```

```text
Before reporting success, run the relevant test command if available and include the result.
```

## Full Template

```markdown
# Role
Act as [role].

# Context
[Relevant background, inputs, audience, environment, risks]

# Task
[Specific action the model should perform]

# Constraints
- [Constraint]
- [Negative instruction]
- [Boundary]

# Output Format
[Required structure]

# Success Criteria
- [How to judge the result]

# Verification
Before finalizing, check that [verification rule].
```

## Chinese Summary

CRAFT-V 可以理解为：

- **Context 背景**：模型需要知道什么？
- **Role 角色**：模型应该以什么视角工作？
- **Action 动作**：具体要做什么？
- **Format 格式**：输出应该长什么样？
- **Tests 标准**：怎样算完成得好？
- **Verification 验证**：回答前要检查什么？

这套方法的重点不是让提示词更花哨，而是让提示词更可执行、可复用、可验证。
