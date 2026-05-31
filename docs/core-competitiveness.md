# Core Competitiveness

Prompt Master should not compete as a generic prompt collection. That market is crowded and easy to copy.

Its strongest position is:

> A bilingual prompt engineering workflow for Codex and tool-using AI agents.

This gives the project a clearer reason to exist and a stronger reason to Star.

## 1. Agent-First, Not Chat-Only

Many prompts are written for one-turn chat answers. Agent prompts need more structure because agents can inspect files, call tools, edit code, run tests, and make decisions across multiple steps.

Prompt Master prompts are designed around:

- Context inspection
- Task decomposition
- Tool-use boundaries
- Verification steps
- Error recovery
- Final reporting

This makes the library useful for Codex, coding assistants, research agents, workflow agents, and automation copilots.

## 2. Bilingual Prompt Engineering

Chinese-English prompt work is not simple translation.

Bad prompt translation often breaks:

- Technical terms
- File paths
- API names
- Code blocks
- CLI flags
- JSON keys
- Guardrails
- Tone and intent

Prompt Master treats bilingual prompt work as a first-class workflow. It preserves exact technical meaning while adapting the instruction style for the target language.

## 3. Reusable Prompt Architecture

The project emphasizes reusable prompt architecture instead of catchy wording.

Every strong prompt should answer:

- What is the model's role?
- What task should it perform?
- What context does it need?
- What constraints must it follow?
- What output format should it produce?
- How should it handle uncertainty?
- How can the user verify success?

This makes prompts easier to maintain, compare, and improve.

## 4. Case-Based Learning

Prompt Master should show before/after transformations.

This matters because users often do not know why a prompt fails. Case studies reveal the hidden problems:

- Missing audience
- Missing output format
- Conflicting constraints
- No success criteria
- Too much abstraction
- No failure handling
- No verification step

The value is not just the final prompt. The value is learning the repair pattern.

## 5. Prompt Quality System

A serious prompt library needs a way to judge quality.

Prompt Master includes:

- A prompt quality checklist
- A prompt review rubric
- Scored review dimensions
- Fix priorities
- Verification criteria

This turns prompt writing from taste into a repeatable engineering process.

## 6. Local Codex Skill Integration

Prompt Master is not only documentation. It can be installed as a Codex skill.

That means users can ask Codex to:

- Optimize prompts
- Translate prompts
- Create templates
- Review prompt quality
- Convert rough requirements into system prompts
- Build reusable prompt workflows

The repo becomes both a learning resource and a working tool.

## Positioning Statement

Use this sentence when describing the project:

> Prompt Master is a bilingual Codex skill and prompt engineering library that helps developers turn rough intent into structured, reusable, verifiable prompts for AI agents.

Chinese version:

> Prompt Master 是一个面向 Codex 和 AI Agent 的双语提示词工程技能库，帮助开发者把模糊需求转化为结构清晰、可复用、可验证的高质量提示词。

## What Makes It Worth Starring

People should Star this repo because it saves time in real workflows:

- They can copy a template immediately.
- They can learn why a prompt works.
- They can review their own prompts.
- They can translate prompts without breaking technical details.
- They can install it as a Codex skill and use it repeatedly.

That is stronger than "a list of useful prompts."
