# Prompt Master 用户手册

这份手册说明如何把 Prompt Master 用作 Codex Skill、提示词模板库，以及跨平台提示词工程工作流。

## 目录

1. [Prompt Master 是什么](#prompt-master-是什么)
2. [安装](#安装)
3. [基础用法](#基础用法)
4. [平台配置](#平台配置)
5. [使用模板](#使用模板)
6. [提示词评审](#提示词评审)
7. [提示词翻译](#提示词翻译)
8. [推荐工作流](#推荐工作流)
9. [常见问题](#常见问题)

## Prompt Master 是什么

Prompt Master 帮你把粗糙需求转化为高质量提示词。

好的提示词应该：

- 具体
- 有结构
- 可复用
- 可验证
- 适合 AI Agent 执行
- 在中英文翻译时不损坏技术含义

它特别适合：

- 代码 Agent
- 研究助手
- 文档写作
- 产品规划
- 数据分析
- 提示词库建设
- 系统提示词设计

## 安装

### Codex

macOS / Linux:

```bash
cp -r prompt-master ~/.codex/skills/
```

Windows PowerShell:

```powershell
Copy-Item -Recurse .\prompt-master $env:USERPROFILE\.codex\skills\
```

### 其他平台

其他平台通常不是直接安装 `SKILL.md`，而是把 Prompt Master 配置成自定义指令、项目规则、知识库或 system prompt。

参考：

- [平台配置指南](../../platform-configuration.md)
- [ChatGPT GPT Instructions](../../../platform-prompts/chatgpt-gpt-instructions.md)
- [Claude Project Instructions](../../../platform-prompts/claude-project-instructions.md)
- [Gemini Gem Instructions](../../../platform-prompts/gemini-gem-instructions.md)

## 基础用法

优化提示词：

```text
使用 prompt-master 帮我优化这个提示词：
[粘贴提示词]
```

评审提示词：

```text
请用 Prompt Master 的 Rubric 评审这个提示词：
[粘贴提示词]
```

翻译提示词：

```text
请把这个中文提示词翻译成适合 AI 编程 Agent 使用的英文提示词：
[粘贴提示词]
```

## 平台配置

| 平台 | 配置方式 |
| --- | --- |
| Codex | 原生 Skill |
| ChatGPT | Custom GPT、Project 或 Custom Instructions |
| Claude | Project instructions 或 Claude Code memory |
| Cursor | `.cursor/rules/*.mdc` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Gemini | Gem |
| API 应用 | system/developer prompt + 模板检索 |

完整说明：[平台配置指南](../../platform-configuration.md)

## 使用模板

从最接近你场景的模板开始：

- [Bug Fix](../../../assets/templates/bug-fix-prompt.md)
- [Code Review](../../../assets/templates/code-review-prompt.md)
- [Research Brief](../../../assets/templates/research-brief-prompt.md)
- [PRD to Tasks](../../../assets/templates/prd-to-tasks-prompt.md)
- [Data Analysis](../../../assets/templates/data-analysis-prompt.md)
- [Content Rewrite](../../../assets/templates/content-rewrite-prompt.md)
- [Translation](../../../assets/templates/translation-prompt.md)
- [Agent System Prompt](../../../assets/templates/agent-system-prompt.md)

把方括号里的占位符替换成你的实际信息：

```text
[项目名]
[目标读者]
[错误信息]
[输出格式]
```

## 提示词评审

评审维度：

- 目标清晰度
- 背景完整度
- 角色有效性
- 任务具体度
- 约束质量
- 输出格式
- 示例
- 验证标准
- 可复用性

参考：[Prompt Review Rubric](../../../assets/checklists/prompt-review-rubric.md)

## 提示词翻译

翻译提示词时要保护：

- 代码块
- 文件路径
- API 名称
- 命令行参数
- 环境变量
- JSON 字段
- 占位符
- 输出格式
- 约束和护栏

使用：[Translation Prompt](../../../assets/templates/translation-prompt.md)

## 推荐工作流

1. 从用户的粗糙需求开始。
2. 识别缺失背景。
3. 使用 CRAFT-V：
   - Context 背景
   - Role 角色
   - Action 动作
   - Format 格式
   - Tests 标准
   - Verification 验证
4. 输出可复制提示词。
5. 解释改了什么。
6. 把可复用版本沉淀为模板。

## 常见问题

### 输出太泛怎么办？

补充读者、输入、约束、示例和成功标准。

### AI 不按格式输出怎么办？

使用更明确的输出契约，例如固定标题、表格或 JSON schema。

### 提示词太长怎么办？

拆成：

- 核心指令
- 背景
- 模板
- 示例

### 翻译时技术术语被改坏怎么办？

使用翻译模板，并明确保护代码、路径、API 名称、命令行参数和 JSON 字段。
