# 新增资料后的版本化研判更新

`versioned-investment-update` 用于保留历史判断，并严格区分 Material Delta、Evidence Delta 与 Judgment Delta；输出强化、削弱、不变、新增、已解决/风险缓解、仍未知和候选判断更新，等待 Human Review。

统一语义见 [Shared Evidence Semantics](../../../EVIDENCE_SEMANTICS.md)；英文 `skill.md` 为 canonical authority。

## 何时使用

- 项目从 BP-only 进入多资料初步研判。
- 新增财务快照、客户数据、技术材料或访谈纪要后更新判断。
- 团队需要理解“为什么判断变了”，而非只看新版本全文。

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
