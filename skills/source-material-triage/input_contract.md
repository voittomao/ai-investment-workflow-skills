# Input Contract: Source Material Triage

## Required Inputs

- project name or anonymized case label
- list of available materials
- short excerpts or summaries
- source date and source owner if known
- known confidentiality boundary

## v0.2 Required Context

In addition to the minimum list above, provide the research need, evidence `as_of`, source type/owner, source date and effective period, known current/historical/superseded status, conflicts, and confidentiality boundary when available. Use only the minimum relevant held materials; this input contract does not authorize full external research.

Follow [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Missing authority, date, currentness, or conflict information remains Unknown.

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

Triage a BP-only material package for NovaCompute, a fictional AI training platform sample company.

## Human Review

The user must confirm whether materials are suitable for analysis and whether any output can be circulated.
