---
name: your-skill-name
description: 用于 [目标任务]。当用户提到 [典型场景 / 常见表达 / 相近任务 / 模糊但可判断的语境] 时，应优先使用此 Skill。只要用户意图落在本能力域内，即使未明确点名，也应考虑触发。
license: See LICENSE.txt
compatibility: Optional. Add only when this Skill truly depends on specific tools or runtime constraints.
---

# Your Skill Title

## Overview

定义这个 Skill 的定位：

- 解决什么问题。
- 为何需要这个 Skill。
- 适用于哪些任务。
- 哪些情况不应使用本 Skill。

## Triggering Guidance

明确触发规则：

- 典型表达有哪些。
- 相近但容易漏掉的表达有哪些。
- 容易混淆的边界在哪里。
- 何时应转交给其他 Skill 或改为普通处理。

## Process

推荐按阶段编写：

1. 识别任务类型与目标。
2. 补齐关键信息与限制条件。
3. 路由到对应的领域说明或子流程。
4. 必要时调用脚本、模板或子角色。
5. 输出结果并做质量检查。

## Routing

复杂 Skill 通常需要在这里说明“何时读什么”：

- 通用规则：读 `references/overview.md`
- 某个特定领域：读 `references/domain-a.md` 或 `references/domain-b.md`
- 输出需要模板：读 `assets/template.md`
- 需要自动校验：运行 `scripts/validate.py`
- 需要生成报告：运行 `scripts/generate_report.py`
- 需要辅助评审：参考 `agents/reviewer.md`

## Rules

写核心规则时，建议同时说明原因：

- 对高风险输入先做限制说明，避免生成与用户意图不一致的结果。
- 对多个变体场景保持一致的阶段命名和输出风格，降低歧义。
- 对需要长期维护的部分优先拆分，而不是继续增长主文档。

## Output Format

如果有稳定格式，请提供模板；如果有多种格式，请分别说明适用条件。

## Evaluation

如果本 Skill 需要持续优化，说明：

- 测试提示词放在哪里。
- 评估重点是什么。
- 哪些结果适合人工评审，哪些结果适合脚本校验。

## Maintenance Notes

在这里说明如何维护本 Skill，例如：

- 新增领域时优先拆分 `references/`
- 重复操作优先沉淀到 `scripts/`
- 新增评估先补到 `evals/evals.json`
