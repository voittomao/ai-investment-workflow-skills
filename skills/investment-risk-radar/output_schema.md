# Output Schema: Investment Risk Radar

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

```json
{
  "skill": "investment-risk-radar",
  "case_name": "NovaCompute fictional example",
  "evidence_boundary": {
    "all_examples_are_fictional": true,
    "requires_human_review": true
  },
  "output": {
    "risk_id": "..."
    "risk_title": "..."
    "risk_category": "..."
    "linked_logic": "..."
    "risk_signal": "..."
    "evidence_status": "..."
    "why_it_matters": "..."
    "priority": "..."
    "diligence_action": "..."
  },
  "quality_flags": [
    "needs_human_review"
  ]
}
```

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
