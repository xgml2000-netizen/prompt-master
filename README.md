# Prompt Master

A Codex skill for prompt engineering, optimization, and management. Supports both Chinese and English workflows.

## Features

- **Prompt Optimization** - Refine and improve AI prompts with structured techniques
- **Prompt Translation** - Convert prompts between Chinese and English while preserving technical accuracy
- **Template Creation** - Generate reusable prompt templates with clear structure
- **Prompt Design** - Design effective system prompts from requirements

## Installation

Copy this directory to your Codex skills folder:

```bash
cp -r prompt-master ~/.codex/skills/
```

## Usage

Trigger the skill by asking Codex to:
- "optimize this prompt"
- "create a prompt template for code review"
- "translate this prompt to English"
- "提示词优化"
- "设计一个提示词模板"

## Structure

```
prompt-master/
├── SKILL.md              # Main skill instructions
├── agents/
│   └── openai.yaml       # UI metadata
├── assets/               # Templates and resources
├── scripts/              # Helper scripts
└── LICENSE               # MIT License
```

## License

MIT - See LICENSE file
