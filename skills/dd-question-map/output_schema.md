# Output Schema: DD Question Map

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

## v0.2 Required Semantics

The JSON below is a minimum container, not the complete canonical contract. Each high-priority item must also state `linked_judgment_or_risk`, `research_need`, qualitative `value_of_information`, `verification_target`, support/weaken/break/remain-Unknown signals, `expected_judgment_impact`, and Human Review boundary. Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md).

```json
{
  "skill": "dd-question-map",
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
    "dd_id": "...",
    "dd_category": "...",
    "dd_type": "...",
    "question_or_task": "...",
    "target_source": "...",
    "linked_risk": "...",
    "evidence_needed": "...",
    "support_signal": "...",
    "break_signal": "...",
    "priority": "..."
  },
  "quality_flags": [
    "needs_human_review"
  ]
}
```

## Optional Source References

`source_references` is optional. Use it when lightweight references are available, such as a filename, page number, section title, interview date, or spreadsheet tab. Do not require every output item to have a `source_id`, and do not fabricate source IDs when the source location is unavailable.

## Recommended Next Workflow Step

Recommended next workflow step: `versioned-investment-update` after new materials arrive, or `investment-evidence-audit` before circulating a workpaper.

This is a workflow suggestion only. Do not force the next skill to run when the available evidence or user intent does not support it, and do not frame the workflow step as an investment decision.

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
