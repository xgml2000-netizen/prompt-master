# Prompt Master

### 面向 Codex、ChatGPT、Claude、Cursor、Gemini、Copilot 和 AI Agent 的提示词工程 Skill

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Codex%20%7C%20ChatGPT%20%7C%20Claude%20%7C%20Cursor%20%7C%20Gemini-blue.svg)](docs/platform-configuration.md)
[![Templates](https://img.shields.io/badge/templates-agent%20%7C%20coding%20%7C%20research%20%7C%20writing-purple.svg)](assets/templates)
[![Languages](https://img.shields.io/badge/docs-English%20%7C%20中文%20%7C%20日本語%20%7C%20Deutsch-orange.svg)](#语言)

[English](README.md) | 中文 | [日本語](README_JA.md) | [Deutsch](README_DE.md) | [更新日志](CHANGELOG.md)

Prompt Master 不是简单的“提示词大全”，而是一套面向 Codex / AI Agent 的多语言提示词工程工作流。

它的目标很明确：把模糊的人类需求，转化为 AI Agent 能理解、能执行、能验证、能复用的高质量提示词。

## 语言

| 语言 | README | 手册 |
| --- | --- | --- |
| English | [README.md](README.md) | [User Manual](docs/user-manual/en/README.md) |
| 中文 | [README_ZH.md](README_ZH.md) | [用户手册](docs/user-manual/zh/README.md) |
| 日本語 | [README_JA.md](README_JA.md) | 即将完善 |
| Deutsch | [README_DE.md](README_DE.md) | 即将完善 |

## 核心竞争力

大多数提示词仓库都在收集提示词。Prompt Master 更关注完整的提示词生产流程：

1. **Agent 优先**
   不是只给聊天机器人用，而是为会读文件、调用工具、修改代码、运行测试的 AI Agent 设计。

2. **多语言提示词工程**
   中英文提示词不是简单翻译。Prompt Master 会保护代码块、文件路径、API 名称、命令行参数、JSON 字段、占位符、约束和输出格式。

3. **方法论而不是玄学**
   使用 CRAFT-V：Context、Role、Action、Format、Tests、Verification。

4. **案例驱动**
   不只给最终提示词，还解释原提示词为什么弱、改了什么、为什么这样改。

5. **可评审**
   提供检查清单和评分 Rubric，让提示词质量可以被讨论、比较和改进。

6. **Codex 原生 Skill**
   在 Codex 中可以作为真正的 Skill 安装；在其他平台则可以作为自定义指令、项目规则、知识库或 system prompt 使用。

## 快速开始

### Codex 原生安装

macOS / Linux:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

然后对 Codex 说：

```text
使用 prompt-master 帮我优化这个提示词：
[粘贴你的提示词]
```

### 其他 AI 平台

其他平台通常不是“安装 skill”，而是配置成：

- ChatGPT：Custom GPT、Project 或 Custom Instructions
- Claude：Project instructions、Project knowledge 或 Claude Code memory
- Cursor：`.cursor/rules/` 项目规则
- GitHub Copilot：`.github/copilot-instructions.md`
- Gemini：Gem
- DeepSeek / Kimi / Doubao / Qwen：system prompt、Bot instructions、置顶提示词或知识库
- API 应用：system/developer prompt + 模板检索

完整配置见：[平台配置指南](docs/platform-configuration.md)。

## 这个仓库包含什么

| 模块 | 内容 |
| --- | --- |
| 使用说明 | [How to Use](docs/how-to-use.md) |
| 用户手册 | [中文](docs/user-manual/zh/README.md), [English](docs/user-manual/en/README.md) |
| 平台配置 | [Platform Configuration Guide](docs/platform-configuration.md) |
| 文档中心 | [Documentation Hub](docs/README.md) |
| 方法论 | [Prompt Engineering Framework](docs/prompt-engineering-framework.md) |
| 核心竞争力 | [Core Competitiveness](docs/core-competitiveness.md) |
| 案例 | [Real Workflow Case Studies](examples/case-studies.md) |
| Before/After | [Before and After Examples](examples/before-after.md) |
| 模板 | [Agent](assets/templates/agent-system-prompt.md), [Code Review](assets/templates/code-review-prompt.md), [Research](assets/templates/research-brief-prompt.md), [Translation](assets/templates/translation-prompt.md), [Bug Fix](assets/templates/bug-fix-prompt.md), [PRD to Tasks](assets/templates/prd-to-tasks-prompt.md), [Data Analysis](assets/templates/data-analysis-prompt.md), [Content Rewrite](assets/templates/content-rewrite-prompt.md) |
| 质量体系 | [Prompt Quality Checklist](assets/checklists/prompt-quality-checklist.md), [Prompt Review Rubric](assets/checklists/prompt-review-rubric.md) |

## CRAFT-V 方法

| 步骤 | 含义 | 要回答的问题 |
| --- | --- | --- |
| C | Context 背景 | 模型需要知道什么？ |
| R | Role 角色 | 模型应该用什么视角工作？ |
| A | Action 动作 | 它具体要做什么？ |
| F | Format 格式 | 输出应该长什么样？ |
| T | Tests 标准 | 怎样算完成得好？ |
| V | Verification 验证 | 回答前需要检查什么？ |

## 示例

弱提示词：

```text
帮我修这个 bug。
```

改进后：

```text
请你作为资深调试伙伴，帮助我定位并修复下面这个 bug 的根因。

背景：
- 项目：[项目名]
- 技术栈：[语言/框架/运行时]
- 预期行为：[应该发生什么]
- 实际行为：[现在发生了什么]
- 错误信息：[粘贴完整错误]

工作流程：
1. 分析错误并判断最可能的问题区域。
2. 在可行时复现问题。
3. 找到最小根因。
4. 实施聚焦修复。
5. 用测试、命令或手动检查验证修复。

约束：
- 不要重写无关代码。
- 不要用宽泛异常捕获掩盖问题。
- 除非必须，否则保留现有公开行为。

输出：
## 根因
[解释]

## 修复
[改动]

## 验证
[验证结果]
```

## FAQ

### Prompt Master 只能用于 Codex 吗？

不是。Codex 可以原生安装为 Skill；其他平台可以通过自定义指令、项目知识、规则文件或 system prompt 使用。

### 它和普通提示词合集有什么区别？

普通提示词合集主要给你“结果”。Prompt Master 还提供方法、评分标准、案例、平台配置和复用结构。

### 支持中文吗？

支持。中英文提示词工程是核心场景之一。

## 贡献

欢迎贡献：

- 真实工作流模板
- Before/After 案例
- 中英文提示词翻译案例
- 平台配置示例
- 质量检查项

请先阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

MIT - see [LICENSE](LICENSE).
