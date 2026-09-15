# Input Contract: Primary-Market Quick-Look

## Required Inputs

- material triage result
- company-provided BP or summary
- product and market notes
- financial or traction snapshots if available
- known missing evidence

## v0.2 Required Context

Also provide the decision/research question, evidence `as_of`, source conflicts, and the minimum relevant company, product, customer, commercial, competition, and financial evidence available. The input must support a bounded hypothesis; otherwise retain Unknown and return to Source Material Triage.

Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Business Understanding and the Investment Judgment Candidate must remain distinct.

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

Draft a quick-look analysis for NovaCompute based on a fictional BP and source-limited evidence.

## Human Review

The user must confirm whether materials are suitable for analysis and whether any output can be circulated.
