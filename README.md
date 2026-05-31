# Prompt Master

Prompt Master is a bilingual prompt engineering skill and template library for Codex and AI agents.

It is built for one practical goal: turn vague human intent into prompts that agents can execute, verify, and reuse.

> 中文：Prompt Master 不是简单的“提示词大全”，而是一套面向 Codex / AI Agent 的双语提示词工程工作流。它帮助你把模糊需求变成结构清晰、可执行、可复用、可评审的高质量提示词。

## Core Competitiveness

Most prompt repositories collect prompts. Prompt Master focuses on the full prompt production workflow:

1. **Agent-first design**
   Prompts are written for tool-using agents, not only chatbots. They include context gathering, execution rules, verification, risk handling, and output contracts.

2. **Bilingual prompt engineering**
   Chinese-English prompt work is treated as a first-class workflow. The library preserves technical terms, code blocks, constraints, and intent instead of doing literal translation.

3. **Reusable structure, not magic wording**
   The project teaches repeatable patterns: role, task, context, constraints, output format, examples, verification, and failure handling.

4. **Before/after case studies**
   Each improvement shows what changed and why, so users can learn the method instead of copying blindly.

5. **Quality review system**
   Prompts can be scored and improved with checklists, rubrics, and concrete failure modes.

6. **Codex skill integration**
   This repo is both documentation and a usable Codex skill. You can install it locally and use it as a prompt optimization assistant.

## Why Star This Repo

- You write prompts for coding agents, research agents, automation, or AI workflows.
- You need Chinese-English prompt translation that does not break technical meaning.
- You want copy-ready templates with clear placeholders.
- You want to learn how to improve prompts, not just collect them.
- You want a local Codex skill that can review, rewrite, and structure prompts.

## What This Repo Contains

| Area | Content |
| --- | --- |
| Core method | [Prompt Engineering Framework](docs/prompt-engineering-framework.md) |
| Differentiation | [Core Competitiveness](docs/core-competitiveness.md) |
| Case studies | [Real Workflow Case Studies](examples/case-studies.md) |
| Before/after | [Before and After Examples](examples/before-after.md) |
| Templates | [Agent](assets/templates/agent-system-prompt.md), [Code Review](assets/templates/code-review-prompt.md), [Research](assets/templates/research-brief-prompt.md), [Translation](assets/templates/translation-prompt.md), [Bug Fix](assets/templates/bug-fix-prompt.md), [PRD to Tasks](assets/templates/prd-to-tasks-prompt.md), [Data Analysis](assets/templates/data-analysis-prompt.md), [Content Rewrite](assets/templates/content-rewrite-prompt.md) |
| Quality system | [Prompt Quality Checklist](assets/checklists/prompt-quality-checklist.md), [Prompt Review Rubric](assets/checklists/prompt-review-rubric.md) |
| Growth | [Star Growth Plan](docs/star-growth-plan.md) |

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

## Typical Use Cases

### 1. Turn a vague request into an agent-ready prompt

Input:

```text
Help me fix this bug.
```

Output:

```text
Act as a senior debugging partner. Inspect the error, reproduce the failure when possible, identify the smallest root cause, implement a focused fix, and verify it with the most relevant test or command.

Context:
- Project: [project name]
- Error: [paste error]
- Expected behavior: [expected behavior]
- Actual behavior: [actual behavior]
- Recent changes: [recent changes]

Rules:
- Do not rewrite unrelated code.
- Preserve existing style and public behavior.
- If reproduction is impossible, explain what evidence is missing and provide the safest next diagnostic step.

Output:
1. Root cause
2. Fix summary
3. Files changed
4. Verification result
```

### 2. Translate a Chinese prompt without damaging technical constraints

Bad translation changes terms, loses guardrails, or rewrites code-like text.

Prompt Master translation keeps:

- File paths
- API names
- CLI flags
- JSON fields
- Code blocks
- Output format
- Negative instructions

### 3. Review a system prompt before shipping it

Prompt Master can score a prompt across:

- Goal clarity
- Context completeness
- Tool-use readiness
- Output contract
- Constraint quality
- Failure handling
- Evaluation criteria

## Repository Structure

```text
prompt-master/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── checklists/
│   └── templates/
├── docs/
├── examples/
├── CONTRIBUTING.md
└── README.md
```

## Method: CRAFT-V

Prompt Master uses a simple framework called **CRAFT-V**:

| Step | Meaning | Question |
| --- | --- | --- |
| C | Context | What does the model need to know? |
| R | Role | What perspective should it take? |
| A | Action | What exactly should it do? |
| F | Format | What should the output look like? |
| T | Tests | How do we know it succeeded? |
| V | Verification | What should it check before answering? |

Read the full method in [docs/prompt-engineering-framework.md](docs/prompt-engineering-framework.md).

## Example: Prompt Upgrade

Weak prompt:

```text
帮我写一个日报。
```

Improved prompt:

```text
请你作为业务分析助理，根据下面的原始信息生成一份适合发给团队的日报。

背景：
- 读者：[团队/老板/客户]
- 语气：[正式/简洁/轻松]
- 今日目标：[今天最重要的目标]

要求：
- 先总结关键进展，再列出风险和明日计划。
- 不要编造没有提供的数据。
- 对阻塞事项给出建议下一步。
- 保持 300 字以内。

输出格式：
## 今日进展
- [要点]

## 风险与阻塞
- [要点]

## 明日计划
- [要点]

原始信息：
[粘贴内容]
```

Why it is better:

- Defines audience and tone
- Prevents fabricated data
- Gives an output contract
- Turns a generic writing request into a repeatable workflow

More examples:

- [Before and After Examples](examples/before-after.md)
- [Real Workflow Case Studies](examples/case-studies.md)

## Good Prompts in This Repo Are

- Specific enough to execute
- Structured enough to reuse
- Bounded enough to avoid drift
- Verifiable enough to trust
- Practical enough for real workflows
- Bilingual when translation is part of the job

## Roadmap

- Add 30+ battle-tested prompt templates
- Add more Chinese-English case studies
- Add domain packs for coding, research, writing, product, data, and operations
- Add evaluation examples for prompt regression testing
- Add short demo videos or GIFs for the Codex skill workflow

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
