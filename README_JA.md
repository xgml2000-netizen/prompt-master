# Prompt Master

### Codex、ChatGPT、Claude、Cursor、Gemini、Copilot、AI Agent 向けのプロンプトエンジニアリング Skill

[English](README.md) | [中文](README_ZH.md) | 日本語 | [Deutsch](README_DE.md)

Prompt Master は、単なるプロンプト集ではありません。AI Agent が実行、検証、再利用しやすいプロンプトを作るための多言語プロンプトエンジニアリング・ワークフローです。

## What It Does

- 曖昧な依頼を、構造化された実行可能なプロンプトに変換します。
- Codex では native skill として利用できます。
- ChatGPT、Claude、Cursor、Gemini、Copilot では custom instructions、project rules、system prompt として利用できます。
- 中国語、英語、日本語、ドイツ語など多言語ドキュメントを順次整備しています。

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

The English and Chinese documentation are the most complete. Japanese documentation is currently a lightweight entry point and will be expanded.
