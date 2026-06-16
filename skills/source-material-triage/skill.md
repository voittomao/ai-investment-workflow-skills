# Source Material Triage Skill

## 1. Skill Objective

This skill is used to classify BP, interview notes, financial snapshots, customer lists, product materials, transaction files, and supplemental documents by material type, maturity, evidence boundary, and missing follow-up materials.

## 2. Suitable Use Cases

Use this skill before any quick-look analysis or investment workpaper drafting, especially when the material package is uneven, source-limited, or mixed across company claims, interview notes, and internal analyst notes.

## 3. Not Suitable For

Do not use it to produce an investment view, make a go/no-go judgment, or infer missing customer, revenue, financing, valuation, technical, legal, or transaction facts.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- project name or anonymized case label
- list of available materials
- short excerpts or summaries
- source date and source owner if known
- known confidentiality boundary

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- material inventory
- material type classification
- material maturity assessment
- usable evidence boundary
- missing material list
- human review notes

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

Never treat a `company_claim` as verified fact. Use `inferred` for analytical judgment and `missing_evidence` when a conclusion cannot be supported. Use `needs_human_review` before the output is circulated.

## 7. Prohibited Wording

Do not output investment recommendations, securities trading advice, legal advice, financial advice, tax advice, or deterministic conclusions. Do not invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds.

Avoid wording that implies certainty when evidence is incomplete. Examples of prohibited conclusion patterns include unconditional outcome language, no-risk language, verified-growth language, automatic investment decisions, or final investment-call language.

## 8. Process

1. Inventory the materials without adding facts.
2. Assign material categories and evidence labels.
3. Separate verified facts, company claims, interview notes, financial snapshots, and missing evidence.
4. Assess whether the package supports quick-look analysis, risk mapping, or only preliminary triage.
5. Create a concrete request list for missing materials.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- case_name
- material_maturity
- materials
- evidence_boundary
- missing_materials
- human_review_required

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Source triage / material maturity**.
