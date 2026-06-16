# Investment Risk Radar Skill

## 1. Skill Objective

This skill is used to map why an investment logic could fail, why highlights may be overstated, and which diligence actions should test the risk.

## 2. Suitable Use Cases

Use this skill after quick-look analysis, before diligence planning, or whenever the analysis needs a sharper anti-thesis and verification agenda.

## 3. Not Suitable For

Do not use it as a generic risk checklist. Do not list broad risks without tying them to investment logic, highlights, evidence gaps, or material conflicts.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- investment logic
- highlight analysis
- counter-hypotheses
- evidence gaps
- material conflicts if any

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- risk radar table
- risk category
- linked logic/highlight/counter-hypothesis
- risk signal
- evidence status
- impact if true
- priority
- diligence action
- material request

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

1. Identify the logic that could break.
2. Translate overclaiming risk into testable risk signals.
3. Tie each risk back to evidence gaps or source conflicts.
4. Prioritize risks by judgment sensitivity.
5. Define material requests and next decision points.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- risk_id
- risk_title
- risk_category
- linked_logic
- risk_signal
- evidence_status
- why_it_matters
- priority
- diligence_action

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Risk radar / risk mapping**.
