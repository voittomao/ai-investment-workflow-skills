# Output Schema: Primary-Market Quick-Look

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

```json
{
  "skill": "primary-market-quick-look",
  "case_name": "NovaCompute fictional example",
  "evidence_boundary": {
    "all_examples_are_fictional": true,
    "requires_human_review": true
  },
  "output": {
    "project_essence": "..."
    "business_model": "..."
    "investment_logic": "..."
    "highlights": "..."
    "counter_hypotheses": "..."
    "core_risks": "..."
    "evidence_gaps": "..."
    "next_steps": "..."
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
