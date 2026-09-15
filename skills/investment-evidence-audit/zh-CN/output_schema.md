# 投资分析证据边界审计：输出 Schema

## Schema

## v0.2 必需语义

下方 JSON 是最小容器，不是完整 canonical 合同。每项重要发现还必须表达：陈述分类、来源支持、权威性/独立性/时效性、问题类型、冲突或未知项、风险、最小修正动作、所需证据、人工复核和流转边界；审计必须识别过期证据、无依据状态/时间推断和生成分析冒充证据。统一语义见 [Shared Evidence Semantics](../../../EVIDENCE_SEMANTICS.md)。

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
  "audit_summary": {
    "overall_status": "pass_with_notes|revision_required|blocked_by_missing_evidence",
    "key_issues": [
      "string"
    ]
  },
  "statements": [
    {
      "statement_id": "string",
      "original_text": "string",
      "statement_type": "fact|company_claim|inference|investment_view|information_gap",
      "evidence_labels": [
        "evidence_label"
      ],
      "evidence_refs": [
        "string"
      ],
      "issue_type": "none|unsupported_claim|overcertainty|fabricated_specificity|missing_scope|prohibited_conclusion|professional_advice_boundary",
      "severity": "high|medium|low",
      "rewrite": "string",
      "required_evidence": "string",
      "needs_human_review": true
    }
  ],
  "must_fix": [
    "statement_id"
  ],
  "recommended_fixes": [
    "statement_id"
  ],
  "human_review_items": [
    "string"
  ]
}
```

## Optional Source References / 可选来源引用

`source_references` 为可选字段；如条件允许，可用文件名、页码、章节、访谈日期或表格 tab 标注来源。无法确认来源位置时，不得编造 `source_id`。

## Recommended Next Workflow Step / 推荐的下一步工作流

推荐的下一步 workflow：人工复核、修订工作底稿，并请求缺失证据。

这只是 workflow 推进建议；不得在证据不足或用户意图不支持时强制运行下一 skill，也不得把下一步 workflow 写成投资决策。

## 通用约束

- 所有重要判断必须包含证据引用或 evidence label。
- `company_claim` 不得自动升级为事实。
- `probability`、`confidence` 和 `priority` 是分析组织字段，不是系统投资决策线。
- 缺失字段应返回 warning 或 `missing_evidence`，不得编造补齐。
- 输出必须包含人工复核项和判断边界。
