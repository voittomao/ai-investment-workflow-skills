# 一级市场项目初判：输出 Schema

## Schema

```json
{
  "project_essence": "string",
  "one_sentence_judgment": {
    "statement": "string",
    "evidence_labels": ["evidence_label"],
    "boundary": "string"
  },
  "investment_logic": [{
    "logic_id": "string",
    "thesis": "string",
    "why_it_matters": "string",
    "supporting_evidence": ["evidence_ref"],
    "missing_evidence": ["string"],
    "confidence": "low|medium|high",
    "what_would_change_our_mind": "string"
  }],
  "highlights": [{
    "highlight": "string",
    "why_it_matters": "string",
    "supporting_evidence": ["evidence_ref"],
    "risk_of_overclaiming": "string"
  }],
  "counter_hypotheses": [{"concern": "string", "evidence_needed": "string", "next_step": "string"}],
  "key_risks": ["string"],
  "evidence_gaps": ["string"],
  "judgment_boundary": "string",
  "next_steps": ["string"]
}
```

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
