# Output Schema: Primary-Market Quick-Look

Use this schema as a reference shape. It is intentionally lightweight so teams can adapt it to Markdown, JSON, tables, or internal tools.

## v0.2 Required Semantics

The JSON below is a minimum container, not the complete canonical contract. A v0.2 output must include Business Understanding, Project Essence, Investment Judgment Candidate, causal Thesis Candidate, Strongest Counter, falsification conditions, fastest falsifier, highest-value next evidence, risks/conflicts/Unknowns, and next verification. The 3/3/3 snapshot fields are optional presentation aids, not the analysis spine. Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md).

```json
{
  "skill": "primary-market-quick-look",
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
    "executive_snapshot": {
      "one_sentence_project_essence": "...",
      "workflow_status": "source-limited quick look | ready for risk radar | needs more materials before DD question map | ready for evidence audit before circulation",
      "current_material_maturity": "...",
      "three_preliminary_highlights": [
        "..."
      ],
      "three_key_risks_or_counter_hypotheses": [
        "..."
      ],
      "three_next_verification_priorities": [
        "..."
      ],
      "recommended_next_skill_to_run": [
        "investment-risk-radar"
      ]
    },
    "recommended_next_workflow_step": "...",
    "project_essence": "...",
    "business_model": "...",
    "investment_logic": "...",
    "highlights": "...",
    "counter_hypotheses": "...",
    "core_risks": "...",
    "evidence_gaps": "...",
    "next_steps": "..."
  },
  "quality_flags": [
    "needs_human_review"
  ]
}
```

## Optional Executive Snapshot / 5-minute brief

This legacy snapshot can remain as an optional presentation aid. It does not replace the v0.2 judgment spine. If used, include:

- `one_sentence_project_essence`.
- `workflow_status`, describing workflow readiness only.
- `current_material_maturity`.
- selected preliminary highlights.
- selected key risks / counter-hypotheses.
- prioritized next verification items.
- Recommended next skill to run, framed as workflow guidance only.

## Optional Source References

`source_references` is optional. Use it when lightweight references are available, such as a filename, page number, section title, interview date, or spreadsheet tab. Do not require every output item to have a `source_id`, and do not fabricate source IDs when the source location is unavailable.

## Recommended Next Workflow Step

Recommended next workflow step: `investment-risk-radar` to stress-test the initial logic, or `dd-question-map` if a management meeting or diligence sprint is scheduled.

This is a workflow suggestion only. Do not force the next skill to run when the available evidence or user intent does not support it, and do not frame the workflow step as an investment decision.

## Field Rules

- Each analytical claim should include an evidence label.
- Missing facts should remain missing, not invented.
- High-sensitivity conclusions should include what would change the view.
- The output must not decide whether to invest.
