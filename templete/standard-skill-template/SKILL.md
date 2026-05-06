---
name: your-skill-name
description: 用于 [目标任务]。当用户提到 [典型场景 / 常见表达 / 邻近需求] 时，应优先使用此 Skill；如果语义明显落在本任务域内，即使没有出现精确关键词，也应触发。
license: See LICENSE.txt
---

# Your Skill Title

## Overview

说明这个 Skill 的目标、适用范围和不适用范围。

建议补齐：

- 这个 Skill 解决什么问题。
- 为什么需要它。
- 常见输入类型有哪些。
- 常见输出形式有哪些。

## Process

建议按阶段组织：

1. 判断用户意图是否属于本 Skill。
2. 确认输入、约束、交付形式和质量标准。
3. 执行主流程。
4. 根据不同场景选择相应分支。
5. 在输出前进行基本检查。

## Variants

如果本 Skill 支持多个子场景，在这里先做路由说明，例如：

- 如果是场景 A，读取 `references/overview.md`
- 如果是场景 B，读取 `references/variants.md`
- 如果输出依赖模板，读取 `assets/template.md`
- 如果有可执行校验逻辑，运行 `scripts/validate.py`

## Rules

列出必须遵守的规则：

- 不要超出用户当前意图自行扩展需求。
- 对不完整输入先补信息，再继续执行。
- 对可判定错误优先校验，而不是事后修补。
- 对固定格式输出保持术语和结构一致。

## Output Format

如果输出有稳定模板，请直接给出。例如：

```markdown
# [标题]
## 背景
## 分析
## 结论
## 下一步
```

## External Resources

使用外部资源时写清楚时机：

- `references/overview.md`：读取完整背景和范围说明。
- `references/variants.md`：读取不同子场景的差异规则。
- `references/examples.md`：查看示例和范式。
- `scripts/validate.py`：对结果进行结构校验。
- `assets/template.md`：生成固定格式输出时使用。
