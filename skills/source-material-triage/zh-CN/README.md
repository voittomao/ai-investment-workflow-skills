# 项目资料分诊

`source-material-triage` 用于判断已持有材料的来源类型、定性权威性、日期/时效性、历史或当前状态、冲突、成熟度、证据边界、最小相关上下文和缺失证据。它不主动承担完整外部研究，也不形成投资判断。

统一语义见 [Shared Evidence Semantics](../../../EVIDENCE_SEMANTICS.md)；英文 `skill.md` 为 canonical authority。

## 何时使用

- 首次收到项目资料，需要判断“现在能分析到什么程度”。
- 资料来自多个角色或版本，需要识别口径冲突与重复材料。
- 准备 quick look memo 前，需要形成资料清单、成熟度判断和补件计划。

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
