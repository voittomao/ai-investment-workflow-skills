# Versioned Investment Update Skill

## 1. Skill Objective

This skill is used to preserve V1/V2 judgment history and explain which views were strengthened, weakened, newly introduced, de-risked, or still unverified after new materials arrive.

## 2. Suitable Use Cases

Use this skill when a BP-only quick look is updated with new financial snapshots, interview notes, customer materials, or technical documents.

## 3. Not Suitable For

Do not rewrite a fresh report without explaining judgment movement. Do not claim new materials fully verify facts unless the evidence supports that conclusion.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials needed for the task:

- V1 workpaper
- new material inventory
- V2 material summaries
- prior risks and DD issues
- human review notes

## 5. Output Requirements

The output should be structured, evidence-aware, and usable by an investment, strategy, or diligence team:

- version change summary
- material maturity change
- strengthened views
- weakened views
- new risks
- de-risked items
- still-to-verify items
- workpaper update recommendations

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

1. Preserve the prior judgment and material boundary.
2. Summarize new materials and classify their evidence strength.
3. Compare judgment movement by module.
4. Separate strengthened, weakened, new, closed, and still-open issues.
5. Recommend workpaper updates without pretending the prior view never existed.

## 9. Output Format

Use Markdown tables or JSON-like structured sections. Every material claim should carry an evidence label or an explicit note that it needs human review.

Core fields:

- version_id
- material_change
- strengthened
- weakened
- new_risks
- de_risked
- still_to_verify
- workpaper_updates

## 10. Human Review Requirement

Human review is mandatory before the output is used in an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Versioned update / judgment change tracking**.
