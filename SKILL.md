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

## Positioning

Prompt Master is not a generic prompt collection. It is a bilingual prompt engineering workflow for Codex and tool-using AI agents.

Its core goal: turn rough human intent into prompts that are structured, reusable, verifiable, and safe for agent execution.

## Quick Guide

When triggered, determine the user intent and route to the appropriate workflow:

- **Optimize**: User has a prompt that needs improvement
- **Translate**: Convert prompts between Chinese and English
- **Template**: Create reusable prompt templates for specific use cases
- **Design**: Design a new prompt from requirements
- **Review**: Score an existing prompt and list concrete fixes
- **Case study**: Explain why a weak prompt fails and show a stronger version
- **Usage help**: Explain how to use Prompt Master in Codex or adapt it to another AI platform

### Workflow selection

Ask the user which mode if the intent is unclear. Otherwise, proceed directly.

## Usage Help

When the user asks how to use or configure Prompt Master, explain the platform distinction clearly:

- Codex can install Prompt Master as a native skill.
- Other AI platforms usually use Prompt Master as custom instructions, project knowledge, repository rules, or a system/developer prompt.
- Do not claim every AI platform supports Codex-style skills.

For Codex, provide:

```bash
cp -r prompt-master ~/.codex/skills/
```

For Windows PowerShell, provide:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

For non-Codex platforms, recommend the short instruction:

```text
Act as Prompt Master, a bilingual prompt engineering assistant. Improve prompts with CRAFT-V: Context, Role, Action, Format, Tests, Verification. Preserve user intent, add missing constraints and output format, make prompts reusable and verifiable, and protect technical terms during Chinese-English translation. Return diagnosis, copy-ready improved prompt, and key changes.
```

If the user asks for a specific platform, give concrete setup guidance for that platform.

## Core Method: CRAFT-V

Use CRAFT-V when improving or designing prompts:

- **Context**: What background, inputs, environment, audience, and risks does the model need?
- **Role**: What functional perspective should the model take?
- **Action**: What exact work should the model perform?
- **Format**: What should the output look like?
- **Tests**: How will the user judge whether the result succeeded?
- **Verification**: What should the model check before finalizing?

Do not optimize for fancy language. Optimize for reliable behavior.

## Prompt Optimization

When optimizing a prompt:

1. Read the original prompt carefully
2. Identify weaknesses: ambiguity, missing constraints, poor structure, unclear output format
3. Apply improvements:
   - Add specific constraints and guardrails
   - Structure with clear sections (Role, Task, Context, Output Format)
   - Add examples where helpful
   - Remove redundant or contradictory instructions
   - Add success criteria and verification steps
   - Preserve the user's original intent
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
- If translating a vague prompt, offer an optional "agent-ready improved version" after the faithful translation

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

## Case Study Output

When the user asks for examples, teaching content, or repo documentation, use this structure:

```markdown
## Original Prompt
[weak prompt]

## Problems
- [specific weakness]

## Improved Prompt
[copy-ready prompt]

## Why It Works
- [principle and effect]

## Reuse Pattern
[generalizable lesson]
```

## Core Competitiveness to Emphasize

When writing documentation for this project, emphasize:

- Agent-first prompts, not only chatbot prompts
- Chinese-English bilingual prompt engineering
- Reusable prompt architecture
- Before/after case studies
- Quality review rubrics
- Codex skill integration

## Design Principles

- Be specific, not vague
- Include negative constraints when needed (what NOT to do)
- Provide output format examples
- Use imperatives ("Do X") not suggestions ("You could do X")
- Keep prompts concise but complete
- Optimize for the model's behavior, not for sounding impressive
- Prefer testable instructions over abstract qualities
- Make prompts verifiable whenever tools, files, factual claims, or code changes are involved
- Use placeholders for reusable inputs
