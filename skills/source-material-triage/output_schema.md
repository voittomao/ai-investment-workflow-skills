# Output Schema: Source Material Triage

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

## v0.2 Required Semantics

The JSON below is a minimum container, not the complete canonical contract. A v0.2 output must also represent `research_need`, `as_of`, source type, qualitative authority/evidence strength, source date/effective period, currentness, historical/current/superseded status, conflict, `usable_for`, `not_usable_for`, minimum relevant context, and missing evidence. Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md).

```json
{
  "skill": "source-material-triage",
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
    "case_name": "...",
    "material_maturity": "...",
    "materials": "...",
    "evidence_boundary": "...",
    "missing_materials": "...",
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

Recommended next workflow step: `primary-market-quick-look`, if the material package is usable enough for a first-pass company view.

This is a workflow suggestion only. Do not force the next skill to run when the available evidence or user intent does not support it, and do not frame the workflow step as an investment decision.

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
