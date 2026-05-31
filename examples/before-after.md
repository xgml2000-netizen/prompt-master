# Before and After Examples

## Example 1: Code Review

Before:

```text
Review this code and tell me if it is good.
```

After:

```text
Act as a senior code reviewer. Review the following code for correctness, security, maintainability, and missing tests.

Prioritize actionable issues. For each finding, include severity, location, why it matters, and a suggested fix. Do not comment on style unless it affects correctness or long-term maintenance.

If there are no serious issues, say that clearly and list any remaining test gaps.

Code:
[paste code]
```

Why it is better:

- Defines the reviewer's role
- Names review criteria
- Sets priority and output expectations
- Prevents low-value style-only feedback

## Example 2: Research

Before:

```text
Tell me about AI coding tools.
```

After:

```text
Create a concise research brief comparing current AI coding tools for a solo developer choosing a daily coding assistant.

Scope:
- Include: OpenAI Codex, GitHub Copilot, Cursor, Claude Code, and other notable tools if relevant
- Focus on: coding workflow, repository understanding, terminal integration, review quality, and pricing
- Time sensitivity: use current information and include dates for product claims

Output:
## Summary
[3-5 bullets]

## Comparison Table
| Tool | Strengths | Weaknesses | Best For | Notes |

## Recommendation
[Clear recommendation with caveats]
```

Why it is better:

- Defines the decision being supported
- Names tools and comparison criteria
- Requires current, dated information
- Produces a useful decision format

## Example 3: Translation

Before:

```text
Translate this prompt into English.
```

After:

```text
Translate the following Chinese prompt into English for use as an AI system prompt.

Rules:
- Preserve headings, bullets, placeholders, and code blocks.
- Do not translate API names, file paths, command flags, or code identifiers.
- Keep constraints and negative instructions precise.
- Use natural English instructions, not literal word-for-word translation.

Output:
## Translation
[translated prompt]

## Notes
[only include if something is ambiguous]

Prompt:
[paste prompt]
```

Why it is better:

- Protects technical terms
- Preserves prompt structure
- Clarifies target usage
- Allows ambiguity notes without polluting the translation
