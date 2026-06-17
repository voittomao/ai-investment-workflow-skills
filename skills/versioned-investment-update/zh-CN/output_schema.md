# 新增资料后的版本化研判更新：输出 Schema

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
  "project_name": "string",
  "from_version": "string",
  "to_version": "string",
  "material_delta": [
    {
      "material": "string",
      "change": "added|updated|removed",
      "evidence_label": "evidence_label"
    }
  ],
  "maturity_change": {
    "before": "string",
    "after": "string",
    "boundary": "string"
  },
  "judgment_changes": [
    {
      "topic": "string",
      "status": "strengthened|weakened|unchanged|unknown",
      "before": "string",
      "after": "string",
      "evidence_refs": [
        "string"
      ],
      "human_review": "string"
    }
  ],
  "risk_changes": {
    "new": [
      "string"
    ],
    "mitigated": [
      "string"
    ],
    "remaining": [
      "string"
    ]
  },
  "dd_changes": {
    "added": [
      "string"
    ],
    "closed": [
      "string"
    ],
    "remaining": [
      "string"
    ]
  },
  "module_update_summaries": [
    {
      "module": "string",
      "change": "string",
      "next_action": "string"
    }
  ],
  "memo_update_recommendations": [
    "string"
  ]
}
```

## Optional Source References / 可选来源引用

`source_references` 为可选字段；如条件允许，可用文件名、页码、章节、访谈日期或表格 tab 标注来源。无法确认来源位置时，不得编造 `source_id`。

## Recommended Next Workflow Step / 推荐的下一步工作流

推荐的下一步 workflow：如风险画像发生变化，可回到 `investment-risk-radar`；对外或对内流转前运行 `investment-evidence-audit`。

这只是 workflow 推进建议；不得在证据不足或用户意图不支持时强制运行下一 skill，也不得把下一步 workflow 写成投资决策。

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
