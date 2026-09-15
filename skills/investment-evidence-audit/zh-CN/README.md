# 投资分析证据边界审计

`investment-evidence-audit` 用于审计陈述—证据关系，检查来源支持、权威性、独立性、日期/时效性、公司口径与独立证据、推断/未知/冲突、过期证据、状态越界和生成分析冒充证据。

统一语义见 [Shared Evidence Semantics](../../../EVIDENCE_SEMANTICS.md)；英文 `skill.md` 为 canonical authority。

## 何时使用

- quick look memo、风险雷达或投资母稿准备内部流转前。
- 模型输出内容较深，但需要检查是否越过证据边界。
- 需要把宣传性或确定性表述改成可审阅的投资判断。

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
