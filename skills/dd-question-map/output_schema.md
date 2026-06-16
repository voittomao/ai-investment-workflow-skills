# Output Schema: DD Question Map

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

```json
{
  "skill": "dd-question-map",
  "case_name": "NovaCompute fictional example",
  "evidence_boundary": {
    "all_examples_are_fictional": true,
    "requires_human_review": true
  },
  "output": {
    "dd_id": "..."
    "dd_category": "..."
    "dd_type": "..."
    "question_or_task": "..."
    "target_source": "..."
    "linked_risk": "..."
    "evidence_needed": "..."
    "support_signal": "..."
    "break_signal": "..."
    "priority": "..."
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
