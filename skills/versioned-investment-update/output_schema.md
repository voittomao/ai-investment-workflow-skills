# Output Schema: Versioned Investment Update

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

## v0.2 Required Semantics

The JSON below is a minimum container, not the complete canonical contract. A v0.2 output must include prior judgment and `prior_judgment_as_of`, prior evidence boundary, `material_delta`, `new_evidence`, `evidence_as_of`, `evidence_delta`, `judgment_delta` (strengthened/weakened/unchanged/newly introduced/resolved or de-risked/still Unknown), risk/DD changes, candidate judgment update, and Human Review. Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md).

```json
{
  "skill": "versioned-investment-update",
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
    "version_id": "...",
    "material_change": "...",
    "strengthened": "...",
    "weakened": "...",
    "new_risks": "...",
    "de_risked": "...",
    "still_to_verify": "...",
    "workpaper_updates": "..."
  },
  "quality_flags": [
    "needs_human_review"
  ]
}
```

## Optional Source References

`source_references` is optional. Use it when lightweight references are available, such as a filename, page number, section title, interview date, or spreadsheet tab. Do not require every output item to have a `source_id`, and do not fabricate source IDs when the source location is unavailable.

## Recommended Next Workflow Step

Recommended next workflow step: `investment-risk-radar` if the risk profile changed, or `investment-evidence-audit` before circulation.

This is a workflow suggestion only. Do not force the next skill to run when the available evidence or user intent does not support it, and do not frame the workflow step as an investment decision.

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
