# 项目资料分诊：输出 Schema

## Schema

```json
{
  "recommended_next_workflow_step": "string",
  "source_references": [
    {
      "source_id": "...",
      "evidence_label": "...",
      "note": "..."
    }
  ],
  "case_name": "string",
  "material_inventory": [
    {
      "material_id": "string",
      "file_name": "string",
      "material_type": "bp|interview|financial|customer|product|legal|transaction|other",
      "provider_role": "string",
      "version_or_date": "string",
      "evidence_label": "evidence_label",
      "usable_for": [
        "string"
      ],
      "not_sufficient_for": [
        "string"
      ],
      "sensitivity": "public_sample|internal|restricted",
      "notes": "string"
    }
  ],
  "maturity_assessment": {
    "status": "single_source|multi_source_unverified|cross_checked",
    "reasoning": "string"
  },
  "conflicts": [
    {
      "topic": "string",
      "materials": [
        "material_id"
      ],
      "resolution_needed": "string"
    }
  ],
  "missing_materials": [
    {
      "request": "string",
      "why_needed": "string",
      "priority": "high|medium|low"
    }
  ],
  "judgment_boundary": "string",
  "human_review_items": [
    "string"
  ]
}
```

## Optional Source References / 可选来源引用

`source_references` 为可选字段；如条件允许，可用文件名、页码、章节、访谈日期或表格 tab 标注来源。无法确认来源位置时，不得编造 `source_id`。

## Recommended Next Workflow Step / 推荐的下一步工作流

推荐的下一步 workflow：如资料包已足以支持初步判断，可运行 `primary-market-quick-look`。

这只是 workflow 推进建议；不得在证据不足或用户意图不支持时强制运行下一 skill，也不得把下一步 workflow 写成投资决策。

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
