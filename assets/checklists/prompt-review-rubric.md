# Prompt Review Rubric

Use this rubric to score and improve a prompt.

## Scorecard

| Dimension | 1 | 3 | 5 |
| --- | --- | --- | --- |
| Goal clarity | Vague or broad | Understandable but incomplete | Specific, measurable, and actionable |
| Context | Missing key background | Some context but gaps remain | Enough context for reliable execution |
| Role | Decorative or absent | Basic role | Functional role tied to task quality |
| Task | Ambiguous action | Action is clear but broad | Exact action and workflow are clear |
| Constraints | No boundaries | Some constraints | Clear boundaries and negative instructions |
| Output format | Unspecified | Partially specified | Concrete, reusable output contract |
| Examples | None when needed | Generic examples | Relevant examples or edge cases |
| Verification | No success check | Weak success check | Clear success criteria and validation steps |
| Reusability | One-off and brittle | Some reusable parts | Clean placeholders and reusable structure |

## Review Output Template

```markdown
## Score
Overall: [score]/45

| Dimension | Score | Note |
| --- | ---: | --- |
| Goal clarity | [1-5] | [note] |
| Context | [1-5] | [note] |
| Role | [1-5] | [note] |
| Task | [1-5] | [note] |
| Constraints | [1-5] | [note] |
| Output format | [1-5] | [note] |
| Examples | [1-5] | [note] |
| Verification | [1-5] | [note] |
| Reusability | [1-5] | [note] |

## Highest-Impact Fixes
1. [Fix]
2. [Fix]
3. [Fix]

## Revised Prompt
[Copy-ready prompt]
```

## Common Failure Modes

- The prompt asks for "better" but never defines quality.
- The role sounds impressive but does not change behavior.
- The prompt gives a task but no output format.
- The prompt includes constraints that conflict with each other.
- The prompt asks for factual claims but does not require sources.
- The prompt asks an agent to make changes but does not require verification.
- The prompt is too tied to one private example to be reusable.
