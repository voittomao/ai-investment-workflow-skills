# 投资分析证据边界审计：输出 Schema

## Schema

```json
{
  "audit_summary": {
    "overall_status": "pass_with_notes|revision_required|blocked_by_missing_evidence",
    "key_issues": ["string"]
  },
  "statements": [{
    "statement_id": "string",
    "original_text": "string",
    "statement_type": "fact|company_claim|inference|investment_view|information_gap",
    "evidence_labels": ["evidence_label"],
    "evidence_refs": ["string"],
    "issue_type": "none|unsupported_claim|overcertainty|fabricated_specificity|missing_scope|prohibited_conclusion|professional_advice_boundary",
    "severity": "high|medium|low",
    "rewrite": "string",
    "required_evidence": "string",
    "needs_human_review": true
  }],
  "must_fix": ["statement_id"],
  "recommended_fixes": ["statement_id"],
  "human_review_items": ["string"]
}
```

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
