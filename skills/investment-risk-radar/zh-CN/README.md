# 投资风险雷达

`investment-risk-radar` 用于把风险回连到投资逻辑和失效机制，明确证据信号、最快证伪、判断敏感性、DD 优先级和下一验证动作，而不是生成泛化风险清单。

统一语义见 [Shared Evidence Semantics](../../../EVIDENCE_SEMANTICS.md)；英文 `skill.md` 为 canonical authority。

## 何时使用

- 已有项目初判，需要决定最先验证哪些风险。
- 风险清单过于泛化，无法回连投资逻辑和后续行动。
- 需要把财务、法律、商业、技术和交易问题纳入同一风险视图。

## 文件说明

| 文件 | 用途 |
| --- | --- |
| `skill.md` | 完整工作流指令、证据纪律和人工复核要求 |
| `input_contract.md` | 可接受输入、最小字段和敏感边界 |
| `output_schema.md` | 结构化输出合同 |
| `example_input.md` | NovaCompute 虚构样例输入 |
| `example_output.md` | 克制、可审阅的虚构样例输出 |
| `quality_checklist.md` | 运行后质量检查 |

## 快速使用

1. 先阅读 `input_contract.md`，确认输入边界。
2. 按 `skill.md` 执行工作流。
3. 用 `output_schema.md` 组织结果。
4. 用 `quality_checklist.md` 做人工复核。

## 边界

该 skill 辅助组织投资判断，不提供投资决策、法律、财务或税务意见，也不替代人工尽调。
