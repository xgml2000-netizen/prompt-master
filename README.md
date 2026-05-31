# Prompt Master

Prompt Master is a bilingual Codex skill and prompt library for turning rough ideas into clear, reusable, production-ready prompts.

It focuses on practical prompt work for coding agents, research agents, writing workflows, and Chinese-English prompt translation.

> 中文用户：这是一个面向 Codex / AI Agent 的提示词优化技能库，适合用来优化系统提示词、生成模板、翻译中英文提示词，以及沉淀可复用工作流。

## Why Star This Repo

- Ready-to-use prompt templates for common AI agent workflows
- Chinese-English prompt translation rules that preserve technical meaning
- A structured prompt review checklist for improving weak prompts
- Codex skill instructions that can be installed locally
- Examples that show before/after prompt upgrades

## What It Helps With

| Workflow | Use it for |
| --- | --- |
| Prompt optimization | Make vague prompts specific, structured, testable, and easier for AI agents to follow |
| Prompt translation | Translate prompts between Chinese and English while preserving constraints, code, and intent |
| Prompt templates | Create reusable prompts for code review, research, writing, automation, and planning |
| System prompt design | Convert product requirements or working habits into stable AI assistant behavior |
| Prompt review | Check missing context, unclear output format, conflicting rules, and weak guardrails |

## Quick Start

Install the skill into your Codex skills folder:

```bash
cp -r prompt-master ~/.codex/skills/
```

Then ask Codex:

```text
Use prompt-master to optimize this prompt:
[paste your prompt]
```

Or in Chinese:

```text
使用 prompt-master 帮我优化这个提示词：
[粘贴你的提示词]
```

## Repository Structure

```text
prompt-master/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── checklists/
│   └── templates/
├── examples/
├── docs/
└── README.md
```

## Popular Templates

- [Agent System Prompt Template](assets/templates/agent-system-prompt.md)
- [Code Review Prompt Template](assets/templates/code-review-prompt.md)
- [Research Brief Prompt Template](assets/templates/research-brief-prompt.md)
- [Chinese-English Prompt Translation Template](assets/templates/translation-prompt.md)

## Example: Prompt Upgrade

Weak prompt:

```text
Help me review this code.
```

Improved prompt:

```text
Act as a senior code reviewer. Review the following change for correctness, security, maintainability, and missing tests.

Focus on actionable findings first. For each finding, include severity, file or function reference, why it matters, and a suggested fix. If there are no serious issues, say that clearly and mention remaining test gaps.

Code:
[paste diff or files]
```

See more examples in [examples/before-after.md](examples/before-after.md).

## Prompt Quality Checklist

Before using a prompt, check whether it includes:

- A clear role or perspective
- A specific task
- Enough context and inputs
- Constraints and boundaries
- Output format
- Success criteria
- Examples, when they reduce ambiguity
- Negative instructions, when common mistakes are likely

See the full checklist in [assets/checklists/prompt-quality-checklist.md](assets/checklists/prompt-quality-checklist.md).

## Growth Plan

This repo can earn more Stars by becoming more useful at first glance:

1. Add high-quality templates for coding, research, writing, and product workflows.
2. Show before/after examples instead of only describing prompt engineering.
3. Add Chinese content, because bilingual prompt work is a real differentiator.
4. Publish small, frequent updates so the repo looks alive.
5. Add GitHub topics such as `prompt-engineering`, `codex`, `ai-agent`, `chatgpt`, `prompts`, `prompt-template`, `chinese`.
6. Share specific examples on X, Reddit, V2EX, Juejin, Zhihu, and AI coding communities.

See [docs/star-growth-plan.md](docs/star-growth-plan.md) for a more detailed roadmap.

## Contributing

Contributions are welcome. Good contributions include:

- A prompt template that solves a real workflow
- A before/after prompt improvement
- A bilingual prompt translation example
- A checklist item with a concrete example
- A bug fix to the Codex skill instructions

Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

MIT - see [LICENSE](LICENSE).
