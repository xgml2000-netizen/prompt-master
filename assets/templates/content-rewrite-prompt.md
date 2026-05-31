# Content Rewrite Prompt Template

Use this prompt to improve articles, posts, documentation, or announcements.

```markdown
Act as an editor for [target audience]. Rewrite the following content to improve clarity, structure, and usefulness while preserving the original intent.

Context:
- Audience: [readers]
- Channel: [blog, README, docs, email, social post, internal update]
- Goal: [what readers should understand or do]
- Tone: [professional, direct, friendly, persuasive, technical, etc.]
- Length target: [shorter, same, longer, or specific word count]

Editing rules:
- Preserve factual claims unless they are clearly unsupported.
- Do not add new facts unless marked as suggestions.
- Remove repetition and vague wording.
- Improve headings and flow.
- Keep technical terms accurate.

Output:
## Revised Version
[rewritten content]

## Key Changes
- [Change and reason]

## Optional Suggestions
- [Suggested addition that needs author confirmation]

Original content:
[paste content]
```

## 中文版

```markdown
请你作为面向[目标读者]的编辑，在保留原意的基础上，改写下面的内容，使其更清晰、更有结构、更有用。

背景：
- 读者：[读者]
- 渠道：[博客、README、文档、邮件、社交媒体、内部更新]
- 目标：[希望读者理解或采取什么行动]
- 语气：[专业、直接、友好、有说服力、技术化等]
- 长度目标：[更短、保持、加长或具体字数]

编辑规则：
- 保留事实性表述，除非它明显缺乏支撑。
- 不要新增事实，除非标记为建议。
- 删除重复和空泛表达。
- 改善标题和行文结构。
- 保持技术术语准确。

输出：
## 改写版本
[改写后的内容]

## 关键修改
- [修改和原因]

## 可选建议
- [需要作者确认的补充建议]

原文：
[粘贴内容]
```
