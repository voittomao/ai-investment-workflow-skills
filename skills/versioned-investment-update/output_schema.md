# 新增资料后的版本化研判更新：输出 Schema

## Schema

```json
{
  "project_name": "string",
  "from_version": "string",
  "to_version": "string",
  "material_delta": [{"material": "string", "change": "added|updated|removed", "evidence_label": "evidence_label"}],
  "maturity_change": {"before": "string", "after": "string", "boundary": "string"},
  "judgment_changes": [{
    "topic": "string",
    "status": "strengthened|weakened|unchanged|unknown",
    "before": "string",
    "after": "string",
    "evidence_refs": ["string"],
    "human_review": "string"
  }],
  "risk_changes": {
    "new": ["string"],
    "mitigated": ["string"],
    "remaining": ["string"]
  },
  "dd_changes": {"added": ["string"], "closed": ["string"], "remaining": ["string"]},
  "module_update_summaries": [{"module": "string", "change": "string", "next_action": "string"}],
  "memo_update_recommendations": ["string"]
}
```

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
