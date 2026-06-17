# Primary-Market Quick-Look Skill

## 1. Skill Objective

This skill is used to produce a quick-look analysis that captures project essence, business model, investment logic, highlights, counter-hypotheses, core risks, evidence gaps, and next verification steps.

## 2. Suitable Use Cases

Use this skill when an investor, founder, analyst, or strategy team needs to understand a company through an investment research lens from limited but usable materials.

## 3. Not Suitable For

Do not use it as an investment recommendation engine, securities trading tool, legal opinion, financial advice, tax advice, or investment committee substitute.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- material triage result
- company-provided BP or summary
- product and market notes
- financial or traction snapshots if available
- known missing evidence

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- Executive Snapshot / 5-minute brief
- one-paragraph quick look
- project essence
- investment logic
- highlight analysis
- counter-hypotheses
- risk summary
- evidence gaps
- next verification priorities

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

Start with an **Executive Snapshot / 5-minute brief** that includes one-sentence project essence, `workflow_status`, current material maturity, three preliminary highlights, three key risks or counter-hypotheses, three next verification priorities, and the recommended next skill to run. `workflow_status` describes only workflow readiness, such as `source-limited quick look`, `ready for risk radar`, `needs more materials before DD question map`, or `ready for evidence audit before circulation`; it must not express an investment recommendation.

1. Start with what the company appears to be and why it matters.
2. Separate business model understanding from investment view.
3. Write investor-style logic with evidence tags.
4. State anti-thesis and kill-case conditions.
5. List what would change the view and what must be verified next.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- executive_snapshot
- project_essence
- business_model
- investment_logic
- highlights
- counter_hypotheses
- core_risks
- evidence_gaps
- next_steps

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Project essence / investment logic / highlights / counter-hypotheses**.
