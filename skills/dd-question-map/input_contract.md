# Input Contract: DD Question Map

## Required Inputs

- risk radar
- quick-look analysis
- known material gaps
- available target sources
- human review priorities

## v0.2 Required Context

Provide the current Investment Judgment Candidate, Thesis Candidate, risk radar with judgment sensitivity, evidence gaps/conflicts, available target sources, access constraints, prior diligence results, and the decision the DD must inform.

Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Questions, material requests, planned searches, and expected answers are verification actions—not evidence.

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

Create a DD question map for NovaCompute covering CTO, CFO, customer references, financial checks, and transaction review.

## Human Review

The user must confirm whether materials are suitable for analysis and whether any output can be circulated.
