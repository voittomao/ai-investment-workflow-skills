# 核心待验证问题地图：输出 Schema

## Schema

```json
{
  "dd_items": [{
    "dd_id": "string",
    "dd_category": "management|technology_product|customer_commercial|financial_revenue|delivery_operations|legal_transaction|expert_third_party|material_request|other",
    "dd_type": "interview|material|data_check|technical_validation|customer_reference|legal_check|expert_call|other",
    "question_or_task": "string",
    "target_source": "string",
    "linked_risk_ids": ["string"],
    "why_it_matters": "string",
    "evidence_needed": "string",
    "support_signal": "string",
    "break_signal": "string",
    "material_request": "string",
    "priority": "verify_first|focus|follow_up",
    "expected_next_action": "string",
    "output_format": "string",
    "evidence_labels": ["evidence_label"]
  }]
}
```

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
