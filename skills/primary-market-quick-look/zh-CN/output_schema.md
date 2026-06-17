# 一级市场项目初判：输出 Schema

## Schema

```json
{
  "executive_snapshot": {
    "one_sentence_project_essence": "string",
    "workflow_status": "source-limited quick look | ready for risk radar | needs more materials before DD question map | ready for evidence audit before circulation",
    "current_material_maturity": "string",
    "three_preliminary_highlights": [
      "string"
    ],
    "three_key_risks_or_counter_hypotheses": [
      "string"
    ],
    "three_next_verification_priorities": [
      "string"
    ],
    "recommended_next_skill_to_run": [
      "investment-risk-radar"
    ]
  },
  "recommended_next_workflow_step": "string",
  "source_references": [
    {
      "source_id": "...",
      "evidence_label": "...",
      "note": "..."
    }
  ],
  "project_essence": "string",
  "one_sentence_judgment": {
    "statement": "string",
    "evidence_labels": [
      "evidence_label"
    ],
    "boundary": "string"
  },
  "investment_logic": [
    {
      "logic_id": "string",
      "thesis": "string",
      "why_it_matters": "string",
      "supporting_evidence": [
        "evidence_ref"
      ],
      "missing_evidence": [
        "string"
      ],
      "confidence": "low|medium|high",
      "what_would_change_our_mind": "string"
    }
  ],
  "highlights": [
    {
      "highlight": "string",
      "why_it_matters": "string",
      "supporting_evidence": [
        "evidence_ref"
      ],
      "risk_of_overclaiming": "string"
    }
  ],
  "counter_hypotheses": [
    {
      "concern": "string",
      "evidence_needed": "string",
      "next_step": "string"
    }
  ],
  "key_risks": [
    "string"
  ],
  "evidence_gaps": [
    "string"
  ],
  "judgment_boundary": "string",
  "next_steps": [
    "string"
  ]
}
```

## Executive Snapshot / 5-minute brief

快速初判输出开头应包含：

- `one_sentence_project_essence`。
- `workflow_status`，仅描述工作流状态。
- `current_material_maturity`。
- 3 个初步亮点。
- 3 个关键风险 / 反方假设。
- 3 个下一步验证重点。
- 推荐的下一步 skill，且仅作为 workflow 建议。

## Optional Source References / 可选来源引用

`source_references` 为可选字段；如条件允许，可用文件名、页码、章节、访谈日期或表格 tab 标注来源。无法确认来源位置时，不得编造 `source_id`。

## Recommended Next Workflow Step / 推荐的下一步工作流

推荐的下一步 workflow：运行 `investment-risk-radar` 压测初步逻辑；如已安排管理层会议或尽调冲刺，可运行 `dd-question-map`。

这只是 workflow 推进建议；不得在证据不足或用户意图不支持时强制运行下一 skill，也不得把下一步 workflow 写成投资决策。

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
