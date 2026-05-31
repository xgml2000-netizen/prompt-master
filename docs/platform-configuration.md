# Platform Configuration Guide

Prompt Master is native to Codex, but the same workflow can be adapted to most AI platforms.

Important distinction:

- **Codex**: install as a real skill.
- **ChatGPT / Claude / Gemini**: configure as custom instructions, a custom GPT/Gem, or project knowledge.
- **Cursor / GitHub Copilot / Claude Code**: configure as repository rules or instruction files.
- **API / self-hosted tools**: use it as a system prompt plus a template library.

## Quick Matrix

| Platform | Best setup | What to use |
| --- | --- | --- |
| Codex | Native skill | `SKILL.md` plus templates |
| ChatGPT | Custom GPT or Project | Instructions + uploaded repo files |
| Claude | Project instructions or Claude Code memory | Instructions + docs/templates |
| Claude Code | Repository memory | `CLAUDE.md` or `.claude/CLAUDE.md` |
| Cursor | Project Rules | `.cursor/rules/prompt-master.mdc` |
| GitHub Copilot | Repository custom instructions | `.github/copilot-instructions.md` |
| Gemini | Custom Gem | Gem instructions + uploaded files |
| DeepSeek / Kimi / Doubao / Qwen Chat | System prompt or pinned prompt | Short Prompt Master instruction |
| API apps | System/developer prompt | Long Prompt Master instruction + retrieved templates |

## 1. Codex

Codex is the native target for this repository.

Install:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

Usage:

```text
Use prompt-master to review and improve this system prompt:
[paste prompt]
```

Recommended files to keep:

- `SKILL.md`
- `assets/templates/*`
- `assets/checklists/*`
- `examples/*`
- `docs/prompt-engineering-framework.md`

## 2. ChatGPT

ChatGPT has several useful setup modes.

### Option A: Custom GPT

Use this when you want a reusable "Prompt Master" assistant.

Setup:

1. Create a new GPT in ChatGPT.
2. Paste the instruction block from [platform-prompts/chatgpt-gpt-instructions.md](../platform-prompts/chatgpt-gpt-instructions.md).
3. Upload useful files as knowledge:
   - `docs/prompt-engineering-framework.md`
   - `docs/core-competitiveness.md`
   - `assets/checklists/prompt-quality-checklist.md`
   - `assets/checklists/prompt-review-rubric.md`
   - `examples/case-studies.md`
   - selected templates from `assets/templates/`
4. Add conversation starters:
   - `Optimize this prompt with CRAFT-V`
   - `Translate this Chinese prompt into English without breaking technical constraints`
   - `Review this system prompt with a rubric`

### Option B: ChatGPT Project

Use this when your prompts belong to one product, team, or workflow.

Setup:

1. Create a Project.
2. Add custom instructions using the short or long Prompt Master instruction.
3. Upload the templates and checklists you want to reuse.
4. Keep one chat per workflow, such as coding prompts, writing prompts, or research prompts.

### Option C: Custom Instructions

Use this only if you want Prompt Master behavior across many chats. Keep the instruction short to avoid affecting unrelated conversations too much.

## 3. Claude

### Claude Projects

Use Claude Projects when you want a reusable prompt engineering workspace.

Setup:

1. Create a Project.
2. Add project instructions from [platform-prompts/claude-project-instructions.md](../platform-prompts/claude-project-instructions.md).
3. Upload key docs, checklists, examples, and templates.
4. Start a chat with:

```text
Use the uploaded Prompt Master framework to improve this prompt:
[paste prompt]
```

### Claude Code

Use repository memory when you want Claude Code to help improve prompts inside a repo.

Create `CLAUDE.md` or `.claude/CLAUDE.md`:

```markdown
# Prompt Master Behavior

When asked to create, review, translate, or improve prompts, use the Prompt Master CRAFT-V method:
Context, Role, Action, Format, Tests, Verification.

Preserve user intent. Make prompts reusable, bounded, and verifiable. For Chinese-English prompt translation, preserve code, paths, API names, CLI flags, JSON keys, placeholders, constraints, and output format.
```

## 4. Cursor

Cursor supports project rules.

Create:

```text
.cursor/rules/prompt-master.mdc
```

Suggested content:

```markdown
---
description: Prompt Master workflow for prompt engineering tasks
alwaysApply: false
---

When the user asks to create, optimize, review, or translate prompts, use Prompt Master.

Use CRAFT-V:
- Context
- Role
- Action
- Format
- Tests
- Verification

Return diagnosis, copy-ready improved prompt, and key changes.
Preserve technical terms during Chinese-English translation.
```

Use it by asking:

```text
Use the Prompt Master rule to improve this prompt:
[paste prompt]
```

## 5. GitHub Copilot

For repository-level behavior, create:

```text
.github/copilot-instructions.md
```

Suggested content:

```markdown
# Prompt Master Instructions

When working on prompt files, AI assistant instructions, documentation, or examples, use the Prompt Master CRAFT-V method:

- Context
- Role
- Action
- Format
- Tests
- Verification

Prefer prompts that are specific, reusable, bounded, and verifiable.
For Chinese-English prompt translation, preserve technical terms, code blocks, file paths, API names, CLI flags, JSON keys, placeholders, constraints, and output format.
```

## 6. Gemini

Use a custom Gem when you want a reusable Prompt Master assistant.

Setup:

1. Create a new Gem in Gemini.
2. Paste the instruction block from [platform-prompts/gemini-gem-instructions.md](../platform-prompts/gemini-gem-instructions.md).
3. Upload framework, checklist, and example files if your account supports file context.
4. Preview the Gem with a weak prompt and save it.

## 7. DeepSeek / Kimi / Doubao / Qwen Chat

Many chat platforms support one of these patterns:

- Bot instruction
- System prompt
- Pinned prompt
- Knowledge base file upload
- Reusable prompt template

If there is no native "skill" feature, use the short Prompt Master instruction:

```text
Act as Prompt Master, a bilingual prompt engineering assistant. Improve prompts with CRAFT-V: Context, Role, Action, Format, Tests, Verification. Preserve user intent, add missing constraints and output format, make prompts reusable and verifiable, and protect technical terms during Chinese-English translation. Return diagnosis, copy-ready improved prompt, and key changes.
```

Then attach or paste the relevant template.

## 8. API / Developer Integration

For API apps, use Prompt Master as a system or developer message.

Recommended architecture:

1. System/developer message: Prompt Master behavior.
2. Retrieval: load relevant templates and checklists.
3. User message: user's rough prompt and target platform.
4. Output parser: require sections like `Diagnosis`, `Improved Prompt`, and `What Changed`.

Minimal developer message:

```text
You are Prompt Master, a bilingual prompt engineering assistant. Use CRAFT-V to turn rough intent into structured, reusable, verifiable prompts. Preserve technical terms during Chinese-English translation. Return diagnosis, copy-ready improved prompt, and key changes.
```

## Official References

- ChatGPT custom instructions: https://help.openai.com/en/articles/8096356-chatgpt-custom-instructions-faq
- ChatGPT GPTs: https://help.openai.com/en/articles/9358033-creating-and-editing-gpts
- ChatGPT Projects: https://help.openai.com/en/articles/10169521-using-projects-in-chatgpt
- Claude Projects: https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects
- Claude personalization: https://support.claude.com/en/articles/10185728-understanding-claude-s-personalization-features
- Claude Code memory: https://code.claude.com/docs/en/memory
- Cursor rules: https://docs.cursor.com/en/context
- GitHub Copilot custom instructions: https://docs.github.com/en/copilot/concepts/prompting/response-customization
- Gemini Gems: https://support.google.com/gemini/answer/15235603
