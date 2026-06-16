# 项目资料分诊：输出 Schema

## Schema

```json
{
  "case_name": "string",
  "material_inventory": [{
    "material_id": "string",
    "file_name": "string",
    "material_type": "bp|interview|financial|customer|product|legal|transaction|other",
    "provider_role": "string",
    "version_or_date": "string",
    "evidence_label": "evidence_label",
    "usable_for": ["string"],
    "not_sufficient_for": ["string"],
    "sensitivity": "public_sample|internal|restricted",
    "notes": "string"
  }],
  "maturity_assessment": {
    "status": "single_source|multi_source_unverified|cross_checked",
    "reasoning": "string"
  },
  "conflicts": [{"topic": "string", "materials": ["material_id"], "resolution_needed": "string"}],
  "missing_materials": [{"request": "string", "why_needed": "string", "priority": "high|medium|low"}],
  "judgment_boundary": "string",
  "human_review_items": ["string"]
}
```

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
