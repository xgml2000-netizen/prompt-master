# Prompt Master User Manual

This manual explains how to use Prompt Master as a Codex skill, a prompt library, and a cross-platform prompt engineering workflow.

## Table of Contents

1. [What Prompt Master Is](#what-prompt-master-is)
2. [Installation](#installation)
3. [Basic Usage](#basic-usage)
4. [Platform Setup](#platform-setup)
5. [Using Templates](#using-templates)
6. [Prompt Review](#prompt-review)
7. [Prompt Translation](#prompt-translation)
8. [Recommended Workflow](#recommended-workflow)
9. [Troubleshooting](#troubleshooting)

## What Prompt Master Is

Prompt Master helps you convert rough requests into prompts that are:

- Specific
- Structured
- Reusable
- Verifiable
- Suitable for AI agents
- Safe for Chinese-English technical translation

It is strongest when you are working with:

- Coding agents
- Research assistants
- Documentation workflows
- Product planning
- Data analysis
- Prompt libraries
- System prompts

## Installation

### Codex

macOS / Linux:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

### Other Platforms

Other platforms usually do not install `SKILL.md` directly. Use the relevant guide:

- [Platform Configuration Guide](../../platform-configuration.md)
- [ChatGPT GPT Instructions](../../../platform-prompts/chatgpt-gpt-instructions.md)
- [Claude Project Instructions](../../../platform-prompts/claude-project-instructions.md)
- [Gemini Gem Instructions](../../../platform-prompts/gemini-gem-instructions.md)

## Basic Usage

Ask:

```text
Use prompt-master to improve this prompt:
[paste prompt]
```

Or:

```text
Review this prompt with the Prompt Master rubric:
[paste prompt]
```

Or:

```text
Translate this Chinese prompt into English for an AI coding agent:
[paste prompt]
```

## Platform Setup

| Platform | Setup Method |
| --- | --- |
| Codex | Native skill |
| ChatGPT | Custom GPT, Project, or Custom Instructions |
| Claude | Project instructions or Claude Code memory |
| Cursor | `.cursor/rules/*.mdc` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Gemini | Gem |
| API apps | System/developer prompt plus template retrieval |

Read the full guide: [Platform Configuration Guide](../../platform-configuration.md).

## Using Templates

Start with the template closest to your workflow:

- [Bug Fix](../../../assets/templates/bug-fix-prompt.md)
- [Code Review](../../../assets/templates/code-review-prompt.md)
- [Research Brief](../../../assets/templates/research-brief-prompt.md)
- [PRD to Tasks](../../../assets/templates/prd-to-tasks-prompt.md)
- [Data Analysis](../../../assets/templates/data-analysis-prompt.md)
- [Content Rewrite](../../../assets/templates/content-rewrite-prompt.md)
- [Translation](../../../assets/templates/translation-prompt.md)
- [Agent System Prompt](../../../assets/templates/agent-system-prompt.md)

Replace placeholders in square brackets:

```text
[project name]
[target audience]
[error message]
[output format]
```

## Prompt Review

Use the review rubric when you want to improve a prompt systematically.

Review dimensions:

- Goal clarity
- Context completeness
- Role usefulness
- Task specificity
- Constraints
- Output format
- Examples
- Verification
- Reusability

See: [Prompt Review Rubric](../../../assets/checklists/prompt-review-rubric.md)

## Prompt Translation

When translating prompts, preserve:

- Code blocks
- File paths
- API names
- CLI flags
- Environment variables
- JSON keys
- Placeholders
- Output format
- Guardrails

Use: [Translation Prompt](../../../assets/templates/translation-prompt.md)

## Recommended Workflow

1. Start with the user's rough intent.
2. Identify missing context.
3. Apply CRAFT-V:
   - Context
   - Role
   - Action
   - Format
   - Tests
   - Verification
4. Produce a copy-ready prompt.
5. Explain what changed.
6. Save reusable prompts as templates.

## Troubleshooting

### The output is too generic

Add audience, inputs, constraints, examples, and success criteria.

### The AI ignores the format

Use a stricter output contract with headings, tables, or JSON schema.

### The prompt is too long

Split it into:

- Core instruction
- Context
- Template
- Examples

### Translation breaks technical terms

Use the translation template and explicitly protect code, paths, API names, CLI flags, and JSON keys.
