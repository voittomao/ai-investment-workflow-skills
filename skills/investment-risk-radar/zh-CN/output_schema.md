# 投资风险雷达：输出 Schema

## Schema

```json
{
  "risks": [{
    "risk_id": "string",
    "risk_title": "string",
    "risk_category": "logic_breakpoint|highlight_overclaiming|counter_hypothesis|evidence_gap|information_conflict|financial_dd|legal_dd|commercial_dd|transaction|technology|customer|competition|team|supply_chain|market_timing|other",
    "linked_reasoning_ids": ["string"],
    "risk_signal": "string",
    "current_evidence_status": "string",
    "why_it_matters": "string",
    "impact_if_true": "string",
    "severity": "high|medium|low",
    "probability": "unknown|low|medium|high",
    "priority": "verify_first|focus|follow_up",
    "diligence_action": "string",
    "material_request": "string",
    "target_source": "string",
    "next_decision_point": "string",
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
