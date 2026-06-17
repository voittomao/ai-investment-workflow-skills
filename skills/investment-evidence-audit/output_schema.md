# Output Schema: Investment Evidence Audit

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

```json
{
  "skill": "investment-evidence-audit",
  "case_name": "NovaCompute fictional example",
  "evidence_boundary": {
    "all_examples_are_fictional": true,
    "requires_human_review": true
  },
  "source_references": [
    {
      "source_id": "...",
      "evidence_label": "...",
      "note": "..."
    }
  ],
  "output": {
    "recommended_next_workflow_step": "...",
    "finding_id": "...",
    "text_span": "...",
    "issue_type": "...",
    "evidence_label": "...",
    "risk": "...",
    "recommended_rewrite": "...",
    "human_review_required": "..."
  },
  "quality_flags": [
    "needs_human_review"
  ]
}
```

## Optional Source References

`source_references` is optional. Use it when lightweight references are available, such as a filename, page number, section title, interview date, or spreadsheet tab. Do not require every output item to have a `source_id`, and do not fabricate source IDs when the source location is unavailable.

## Recommended Next Workflow Step

Recommended next workflow step: human review, revise the workpaper, and request missing evidence where needed.

This is a workflow suggestion only. Do not force the next skill to run when the available evidence or user intent does not support it, and do not frame the workflow step as an investment decision.

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
