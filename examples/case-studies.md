# Real Workflow Case Studies

These case studies show how Prompt Master improves real prompts.

## Case 1: From Vague Bug Request to Debugging Agent Prompt

Original:

```text
Fix this error.
```

Problems:

- No project context
- No error details
- No expected behavior
- No boundary against unrelated rewrites
- No verification requirement

Improved:

```text
Act as a senior debugging partner. Help me identify and fix the root cause of the following error.

Context:
- Project: [project name]
- Stack: [language/framework/runtime]
- Error message: [paste full error]
- Expected behavior: [what should happen]
- Actual behavior: [what happens now]
- Recent changes: [recent commits, dependency updates, config changes]

Workflow:
1. Inspect the error and identify the most likely failing area.
2. Reproduce or explain how to reproduce the issue when possible.
3. Find the smallest root cause.
4. Suggest or implement a focused fix.
5. Verify with the most relevant test, command, or manual check.

Constraints:
- Do not rewrite unrelated code.
- Do not hide errors with broad try/catch blocks.
- Preserve existing public behavior unless the bug requires changing it.

Output:
## Root Cause
[Explanation]

## Fix
[What changed or should change]

## Verification
[Test or command result]

## Remaining Risk
[Anything still uncertain]
```

Why it works:

- Converts a vague request into a debugging workflow
- Requires evidence and reproduction
- Prevents overbroad rewrites
- Forces verification

## Case 2: From "Write Better" to Content Editing Workflow

Original:

```text
Make this article better.
```

Problems:

- "Better" is undefined
- No target audience
- No tone
- No preservation rules
- No output structure

Improved:

```text
Act as an editor for [target audience]. Improve the following article for clarity, structure, and usefulness while preserving the author's main ideas.

Context:
- Audience: [who will read it]
- Goal: [what the article should help readers understand or do]
- Tone: [professional, friendly, direct, persuasive, etc.]
- Length target: [shorter/same/longer/specific word count]

Editing rules:
- Preserve factual claims unless they are clearly unsupported.
- Do not add new facts unless marked as suggestions.
- Improve headings and flow.
- Remove repetition.
- Keep the author's voice where possible.

Output:
## Revised Article
[Edited version]

## Key Changes
- [Change and reason]

## Suggested Additions
- [Optional additions that require author confirmation]

Article:
[paste article]
```

Why it works:

- Defines quality criteria
- Protects the author's intent
- Separates edits from new suggestions
- Makes the revision reviewable

## Case 3: From Chinese Prompt to Production English Prompt

Original:

```text
帮我把这个 Python 项目打包成 exe，注意不要破坏现有功能。
```

Naive translation:

```text
Help me package this Python project into exe, be careful not to break existing features.
```

Problems:

- Too vague for an agent
- No environment details
- No packaging constraints
- No verification criteria
- Does not mention dependency or asset handling

Improved English prompt:

```text
Act as a Python release engineer. Help package this Python project into a Windows `.exe` while preserving existing behavior.

Context:
- Project path: [path]
- Entry point: [main script or module]
- Packaging tool preference: [PyInstaller, Nuitka, cx_Freeze, or unknown]
- Runtime assets: [models, config files, images, data files]
- External dependencies: [list known dependencies]

Workflow:
1. Inspect the project structure and entry point.
2. Identify runtime files that must be bundled.
3. Create or update the packaging configuration.
4. Build the executable.
5. Test the executable on Windows.

Constraints:
- Do not remove existing features.
- Do not hardcode local-only absolute paths unless there is no alternative.
- Keep packaging changes isolated from application logic when possible.

Output:
## Packaging Approach
[Tool and reason]

## Changes Made
[Files/config changed]

## Build Command
[Command]

## Verification
[How the exe was tested]

## Known Limitations
[Remaining risks]
```

Why it works:

- Preserves the Chinese intent
- Adds execution details required by an agent
- Makes verification explicit
- Protects existing functionality

## Case 4: From Product Idea to Implementation Plan

Original:

```text
做一个用户反馈功能。
```

Problems:

- No user flow
- No data model
- No permissions
- No priority
- No delivery plan

Improved:

```text
Act as a product-minded engineering lead. Turn the following feature idea into an implementation plan.

Feature idea:
Build a user feedback feature.

Context:
- Product: [product type]
- Users: [who submits feedback]
- Admins: [who reviews feedback]
- Stack: [frontend/backend/database]
- Existing auth model: [auth details]

Clarify or assume:
- Feedback fields
- Submission flow
- Admin review flow
- Notification requirements
- Abuse/spam handling
- Privacy concerns

Output:
## User Stories
- As a [user], I want [goal], so that [benefit].

## Data Model
| Field | Type | Notes |
| --- | --- | --- |

## API / Backend Changes
- [Endpoint or service]

## UI Changes
- [Screen/component]

## Edge Cases
- [Case]

## Implementation Steps
1. [Step]

## Tests
- [Test]
```

Why it works:

- Turns a feature idea into engineering tasks
- Covers product, backend, frontend, and testing
- Leaves room for assumptions while making them visible

## Case 5: From Prompt Collection to Prompt System

Original:

```text
Give me 10 prompts for marketing.
```

Problems:

- Generic outputs
- No reusable structure
- No target channel
- No brand constraints
- No evaluation standard

Improved:

```text
Create a reusable prompt pack for marketing content generation.

Context:
- Product: [product]
- Audience: [audience]
- Channels: [X, LinkedIn, newsletter, landing page, ads]
- Brand voice: [voice]
- Constraints: [claims to avoid, compliance notes, banned phrases]

For each prompt, include:
- Use case
- Copy-ready prompt
- Required inputs
- Output format
- Quality checklist
- Example input

Output:
## Prompt Pack
### 1. [Prompt Name]
Use case:
[Use case]

Prompt:
[Copy-ready prompt]

Required inputs:
- [Input]

Quality checklist:
- [Check]
```

Why it works:

- Produces a reusable asset instead of disposable prompts
- Captures brand and channel constraints
- Makes each prompt easier to test and maintain
