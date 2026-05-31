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

## Prompt Translation

For Chinese-English prompt translation:

- Preserve all technical terms and code blocks exactly
- Adapt idioms naturally for the target language
- Keep the same structure and formatting
- Maintain all constraints and guardrails

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

## Design Principles

- Be specific, not vague
- Include negative constraints when needed (what NOT to do)
- Provide output format examples
- Use imperatives ("Do X") not suggestions ("You could do X")
- Keep prompts concise but complete
