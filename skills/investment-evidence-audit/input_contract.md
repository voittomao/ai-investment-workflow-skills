# Input Contract: Investment Evidence Audit

## Required Inputs

- draft analysis
- evidence labels if available
- source summary
- known missing materials
- prohibited expression list

## v0.2 Required Context

Provide the draft and intended use; evidence register/source summary; source types, dates/effective periods, and `as_of`; known company claims, independent evidence, conflicts, and Unknowns; relevant historical/current state boundaries; and prohibited-expression/Human Review requirements.

Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). The audit checks the draft against available evidence; it does not discover missing evidence or approve circulation.

## Source References

When available, cite source references using a lightweight `source_id` such as filename, page number, section title, interview date, or spreadsheet tab. Do not fabricate source IDs when the source location is unavailable.

## Common Evidence Labels (not exhaustive)

- user_provided
- company_claim
- interview_note
- financial_snapshot
- third_party_unverified
- independent_evidence
- inferred
- unknown
- missing_evidence
- conflict
- needs_human_review

## Input Boundary

- Use anonymized or fictional examples unless the user has explicit permission to process real materials.
- Do not include private customer lists, cap tables, financing documents, legal documents, or personal information in public examples.
- If material is missing, mark it as `missing_evidence` rather than inventing it.
- If a claim comes from the company, mark it as `company_claim`.

## Minimum Viable Input

Audit a NovaCompute quick-look memo for unsupported claims and overconfident language.

## Human Review

The user must confirm whether materials are suitable for analysis and whether any output can be circulated.
