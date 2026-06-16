# Input Contract: Source Material Triage

## Required Inputs

- project name or anonymized case label
- list of available materials
- short excerpts or summaries
- source date and source owner if known
- known confidentiality boundary

## Accepted Evidence Labels

- user_provided
- company_claim
- interview_note
- financial_snapshot
- third_party_unverified
- inferred
- missing_evidence
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
