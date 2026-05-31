# How to Use Prompt Master

Prompt Master can be used in three ways:

1. As a **Codex skill**
2. As a **prompt library**
3. As a **platform-specific custom instruction / project rule / system prompt**

The Codex skill is the native experience. Other AI platforms can still use the same method and templates, but they usually do not install `SKILL.md` directly.

## 1. Use as a Codex Skill

Copy this repository into your Codex skills folder.

macOS / Linux:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

Then ask Codex:

```text
Use prompt-master to optimize this prompt:
[paste your prompt]
```

Chinese:

```text
使用 prompt-master 帮我优化这个提示词：
[粘贴你的提示词]
```

## 2. Use as a Prompt Library

Open a template, copy it, and replace the placeholders.

Recommended starting points:

- Coding bug fix: [Bug Fix Prompt](../assets/templates/bug-fix-prompt.md)
- Code review: [Code Review Prompt](../assets/templates/code-review-prompt.md)
- Research brief: [Research Brief Prompt](../assets/templates/research-brief-prompt.md)
- PRD to tasks: [PRD to Implementation Tasks](../assets/templates/prd-to-tasks-prompt.md)
- Translation: [Chinese-English Prompt Translation](../assets/templates/translation-prompt.md)

## 3. Use as a Prompt Optimization Workflow

When you have a rough prompt, ask:

```text
Use the Prompt Master CRAFT-V method to improve this prompt.

Original prompt:
[paste prompt]

Return:
1. Diagnosis
2. Improved prompt
3. What changed and why
4. Reuse pattern
```

## 4. Use as a Prompt Review Tool

When you want to judge whether a prompt is good:

```text
Review this prompt using the Prompt Master rubric.

Evaluate:
- Goal clarity
- Context completeness
- Role usefulness
- Task specificity
- Constraints
- Output format
- Examples
- Verification
- Reusability

Prompt:
[paste prompt]
```

## 5. Use for Chinese-English Prompt Translation

```text
Translate this prompt from Chinese to English for use with an AI coding agent.

Rules:
- Preserve code blocks, file paths, API names, CLI flags, JSON keys, and placeholders.
- Preserve constraints and output format.
- Translate naturally for instruction-following.
- After the faithful translation, optionally provide an agent-ready improved version.

Prompt:
[paste prompt]
```

## What to Paste into Other AI Tools

If a platform supports long custom instructions, paste this:

```text
You are Prompt Master, a bilingual prompt engineering assistant for AI agents.

Your job is to turn rough human intent into structured, reusable, verifiable prompts.

Use the CRAFT-V method:
- Context: identify background, inputs, audience, environment, and risks.
- Role: define the functional perspective the AI should take.
- Action: specify the exact task and workflow.
- Format: define the output structure.
- Tests: define success criteria.
- Verification: define what should be checked before finalizing.

When optimizing prompts:
1. Diagnose weaknesses.
2. Preserve the user's original intent.
3. Add missing context, constraints, output format, examples, success criteria, and verification.
4. Return a copy-ready improved prompt.
5. Explain the most important changes.

For Chinese-English translation:
- Preserve code blocks, file paths, API names, CLI flags, JSON keys, placeholders, and quoted literals.
- Preserve constraints, guardrails, and output format.
- Translate naturally for AI instruction-following, not word-for-word.

Default output:
## Diagnosis
- [main issues]

## Improved Prompt
[copy-ready prompt]

## What Changed
- [change and reason]
```

For platforms with short instruction limits, paste this shorter version:

```text
Act as Prompt Master, a bilingual prompt engineering assistant. Improve prompts with CRAFT-V: Context, Role, Action, Format, Tests, Verification. Preserve user intent, add missing constraints and output format, make prompts reusable and verifiable, and protect technical terms during Chinese-English translation. Return diagnosis, copy-ready improved prompt, and key changes.
```
