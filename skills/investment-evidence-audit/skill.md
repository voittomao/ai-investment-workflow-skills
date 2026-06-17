# Investment Evidence Audit Skill

## 1. Skill Objective

This skill is used to identify company claims, unsupported facts, overconfident wording, prohibited conclusions, missing evidence, and rewrite recommendations before an investment workpaper is circulated.

## 2. Suitable Use Cases

Use this skill as the evidence boundary gate before sharing quick-look analysis, risk radar, DD question maps, or investment workpapers.

## 3. Not Suitable For

Do not use it to make the analysis empty or evasive. The goal is disciplined, useful analysis, not a checklist with no judgment.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- draft analysis
- evidence labels if available
- source summary
- known missing materials
- prohibited expression list

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- evidence audit findings
- claim classification
- overstatement flags
- prohibited conclusion flags
- rewrite suggestions
- human review required items

## 6. Evidence Label Rules

Use these labels:

- user_provided
- company_claim
- interview_note
- financial_snapshot
- third_party_unverified
- inferred
- missing_evidence
- needs_human_review

When available, cite source references using a lightweight `source_id` such as filename, page number, section title, interview date, or spreadsheet tab. Do not fabricate source IDs when the source location is unavailable.

Never treat a `company_claim` as verified fact. Use `inferred` for analytical judgment and `missing_evidence` when a conclusion cannot be supported. Use `needs_human_review` before the output is circulated.

## 7. Prohibited Wording

Do not output investment recommendations, securities trading advice, legal advice, financial advice, tax advice, or deterministic conclusions. Do not invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds.

Avoid wording that implies certainty when evidence is incomplete. Examples of prohibited conclusion patterns include unconditional outcome language, no-risk language, verified-growth language, automatic investment decisions, or final investment-call language.

## 8. Process

1. Scan for facts that lack support.
2. Downgrade company claims that read like verified facts.
3. Flag overconfident or prohibited wording.
4. Preserve useful investor judgment while adding evidence boundaries.
5. Produce concrete rewrites and final review notes.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- finding_id
- text_span
- issue_type
- evidence_label
- risk
- recommended_rewrite
- human_review_required

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Evidence boundary audit / quality gate**.
