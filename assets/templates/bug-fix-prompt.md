# Bug Fix Prompt Template

Use this prompt when asking an AI coding agent to debug and fix an issue.

```markdown
Act as a senior debugging partner. Help identify and fix the root cause of the following bug.

Context:
- Project: [project name]
- Stack: [language/framework/runtime]
- Environment: [OS, version, browser, database, etc.]
- Expected behavior: [what should happen]
- Actual behavior: [what happens instead]
- Error message or logs: [paste full error]
- Recent changes: [commits, dependency updates, config changes]

Workflow:
1. Inspect the error and identify the most likely failing area.
2. Reproduce or explain how to reproduce the issue when possible.
3. Find the smallest root cause.
4. Implement or recommend a focused fix.
5. Verify the fix with the most relevant test, command, or manual check.

Constraints:
- Do not rewrite unrelated code.
- Do not hide the problem with broad exception handling.
- Preserve existing public behavior unless changing it is required.
- If evidence is insufficient, state what is missing and give the next diagnostic step.

Output:
## Root Cause
[Explanation]

## Fix
[What changed or should change]

## Verification
[Test, command, or manual check]

## Remaining Risk
[Uncertainty or follow-up]

Bug details:
[paste details]
```

## 中文版

```markdown
请你作为资深调试伙伴，帮助我定位并修复下面这个 bug 的根因。

背景：
- 项目：[项目名]
- 技术栈：[语言/框架/运行时]
- 环境：[系统、版本、浏览器、数据库等]
- 预期行为：[应该发生什么]
- 实际行为：[现在发生了什么]
- 错误信息或日志：[粘贴完整错误]
- 最近改动：[提交、依赖升级、配置变化]

工作流程：
1. 分析错误，判断最可能的问题区域。
2. 在可行时复现问题，或说明如何复现。
3. 找到最小根因。
4. 实施或建议聚焦修复。
5. 用最相关的测试、命令或手动检查验证修复。

约束：
- 不要重写无关代码。
- 不要用宽泛的异常捕获掩盖问题。
- 除非必须，否则保留现有公开行为。
- 如果证据不足，请说明缺少什么，并给出下一步诊断动作。

输出：
## 根因
[解释]

## 修复
[改了什么或应该改什么]

## 验证
[测试、命令或手动检查]

## 剩余风险
[不确定性或后续事项]

Bug 详情：
[粘贴详情]
```
