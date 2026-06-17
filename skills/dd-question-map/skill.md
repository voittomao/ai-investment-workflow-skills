# DD Question Map Skill

## 1. Skill Objective

This skill is used to turn risk hypotheses into a structured diligence question map across management, technology, customer, commercial, financial, operational, legal, transaction, and third-party validation workstreams.

## 2. Suitable Use Cases

Use this skill when a team needs to move from investor-style risk thinking to actionable diligence execution.

## 3. Not Suitable For

Do not reduce diligence to interview questions only. Do not create questions that assume unverified facts are true.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- risk radar
- quick-look analysis
- known material gaps
- available target sources
- human review priorities

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- DD issue map
- question or task
- target source
- evidence needed
- supporting signal
- breaking signal
- material request
- priority
- expected next action

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

1. Group questions by diligence category.
2. Match each question to a risk or investment logic.
3. Define what evidence would support or break the view.
4. Assign target sources and output formats.
5. Keep material requests separate from interview prompts.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- dd_id
- dd_category
- dd_type
- question_or_task
- target_source
- linked_risk
- evidence_needed
- support_signal
- break_signal
- priority

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Core validation issue map / DD execution**.
