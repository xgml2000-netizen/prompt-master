name: prompt-master
description: >-
  Prompt Master - A Codex skill for prompt engineering and optimization. Helps refine, translate, and
  manage prompts for AI coding agents. Supports Chinese-English bilingual workflows, prompt templates,
  and structured prompt design patterns. Use when the user asks to improve prompts, create prompt templates,
  optimize AI instructions, translate prompts between languages, or design effective system prompts.
  Triggers include "optimize prompt", "improve this prompt", "create a prompt template", "translate prompt",
  "prompt engineering", "提示词优化", "优化提示词", "提示词模板", "设计提示词".
---

# Prompt Master

A Codex skill for prompt engineering, optimization, and management workflows.

## Quick Guide

When triggered, determine the user intent and route to the appropriate workflow:

- **Optimize**: User has a prompt that needs improvement
- **Translate**: Convert prompts between Chinese and English
- **Template**: Create reusable prompt templates for specific use cases
- **Design**: Design a new prompt from requirements
- **Review**: Score an existing prompt and list concrete fixes

### Workflow selection

Ask the user which mode if the intent is unclear. Otherwise, proceed directly.

## Prompt Optimization

When optimizing a prompt:

1. Read the original prompt carefully
2. Identify weaknesses: ambiguity, missing constraints, poor structure, unclear output format
3. Apply improvements:
   - Add specific constraints and guardrails
   - Structure with clear sections (Role, Task, Context, Output Format)
   - Add examples where helpful
   - Remove redundant or contradictory instructions
4. Present before/after comparison
5. Explain key changes made
6. Include a final copy-ready prompt

Use this output shape unless the user requests otherwise:

```markdown
## Diagnosis
- [Main issue]

## Improved Prompt
[Copy-ready prompt]

## What Changed
- [Change and reason]
```

## Prompt Translation

For Chinese-English prompt translation:

- Preserve all technical terms and code blocks exactly
- Adapt idioms naturally for the target language
- Keep the same structure and formatting
- Maintain all constraints and guardrails
- Do not translate code identifiers, environment variables, file paths, CLI flags, API names, or quoted literals unless the user explicitly asks
- When a phrase has no exact equivalent, preserve intent over word-for-word translation

## Prompt Templates

Create templates using this structure:

```markdown
## Role
[Define the AI role]

## Task
[Specific task description]

## Context
[Background information]

## Constraints
- [Constraint 1]
- [Constraint 2]

## Output Format
[Expected output structure]

## Examples
[Example inputs/outputs if helpful]
```

When the user asks for a reusable prompt, include placeholders in square brackets and make them easy to replace.

## Prompt Review

When reviewing a prompt, evaluate:

- Goal clarity
- Context completeness
- Input boundaries
- Output format
- Constraints and negative instructions
- Examples and edge cases
- Evaluation criteria
- Risk of conflicting instructions

Return a short scorecard and prioritized fixes:

```markdown
## Scorecard
| Area | Score | Note |
| --- | ---: | --- |
| Goal clarity | 0-5 | [note] |

## Highest-Impact Fixes
1. [Fix]

## Revised Prompt
[Copy-ready revision]
```

## Design Principles

- Be specific, not vague
- Include negative constraints when needed (what NOT to do)
- Provide output format examples
- Use imperatives ("Do X") not suggestions ("You could do X")
- Keep prompts concise but complete
- Optimize for the model's behavior, not for sounding impressive
- Prefer testable instructions over abstract qualities
