# Prompt Master

### Prompt-Engineering-Skill fuer Codex, ChatGPT, Claude, Cursor, Gemini, Copilot und AI Agents

[English](README.md) | [中文](README_ZH.md) | [日本語](README_JA.md) | Deutsch

Prompt Master ist keine einfache Prompt-Sammlung. Es ist ein mehrsprachiger Prompt-Engineering-Workflow, der vage Absichten in strukturierte, wiederverwendbare und verifizierbare Prompts fuer AI Agents verwandelt.

## What It Does

- Verbessert schwache oder unklare Prompts.
- Erstellt wiederverwendbare Prompt-Templates.
- Unterstuetzt Prompt-Uebersetzung ohne technische Details zu verlieren.
- Funktioniert nativ als Codex Skill.
- Kann in ChatGPT, Claude, Cursor, Gemini, Copilot und API-Anwendungen als Custom Instruction, Project Rule oder System Prompt genutzt werden.

## Core Method: CRAFT-V

| Step | Meaning |
| --- | --- |
| C | Context |
| R | Role |
| A | Action |
| F | Format |
| T | Tests |
| V | Verification |

## Quick Start

Codex:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

Other platforms:

```text
Act as Prompt Master, a bilingual prompt engineering assistant. Improve prompts with CRAFT-V: Context, Role, Action, Format, Tests, Verification. Preserve user intent, add missing constraints and output format, make prompts reusable and verifiable, and protect technical terms during translation.
```

## Documentation

- [How to Use](docs/how-to-use.md)
- [Platform Configuration Guide](docs/platform-configuration.md)
- [Prompt Engineering Framework](docs/prompt-engineering-framework.md)
- [Core Competitiveness](docs/core-competitiveness.md)

## Status

English and Chinese documentation are the most complete. German documentation is currently a lightweight entry point and will be expanded.
