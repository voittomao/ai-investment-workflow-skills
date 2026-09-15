# Investment Evidence Audit Skill

## 1. Skill Objective

This skill audits whether an investment analysis says anything more confidently than its evidence permits. It checks claim-support relationships, authority, date/currentness, attribution, inference, Unknown, conflict, state overreach, stale evidence, and generated analysis presented as evidence.

The goal is disciplined and useful judgment—not an empty checklist or the removal of every analytical view.

## 2. Suitable Use Cases

Use this skill as an evidence-boundary gate before sharing a quick look, risk radar, DD map, update, investment workpaper, or other consequential research output.

The method is also reusable in investment banking, strategy, and corporate research wherever claims must remain traceable and appropriately qualified.

## 3. Not Suitable For

Do not use it to:

- discover or acquire missing external evidence;
- classify an initial material package instead of auditing a draft;
- prove that a real-world fact is true solely from the draft;
- approve a workpaper or make an investment decision; or
- replace legal, financial, tax, technical, or other specialist review.

## 4. Input Requirements

Inputs should be anonymized or permissioned and limited to the minimum relevant context:

- draft analysis and intended use;
- evidence register or source summary;
- source references, types, dates/effective periods, and `as_of`, when available;
- known company claims, independent evidence, conflicts, and Unknowns;
- prior/current status boundaries relevant to the draft;
- prohibited-expression and Human Review requirements.

## 5. Output Requirements

Produce a concise claim-support audit that identifies:

- the claim or text span under review;
- source support and lightweight references;
- source authority, independence, date/currentness, and fit for the claim;
- company claim versus independent evidence;
- fact versus inference versus Unknown;
- supporting, partially supporting, conflicting, stale, or missing evidence;
- unsupported state or temporal inference;
- overclaim, fabricated specificity, and prohibited conclusion language;
- generated analysis masquerading as source evidence;
- recommended action: retain, qualify, rewrite, remove, request evidence, or send to Human Review; and
- an overall circulation boundary.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Audit at the claim/evidence-item level when practical: a single document can contain supported facts, company claims, inference, and Unknowns.

Neither a model-generated statement nor a previous analytical conclusion can serve as independent source evidence for itself.

## 7. Prohibited Wording

Do not invent evidence, locators, customers, revenue, financing, valuation, technical metrics, transaction terms, founder backgrounds, dates, or states. Do not label a claim verified, current, approved, completed, contracted, paid, or risk-free unless the supporting evidence establishes that exact scope and state.

Do not convert an audit result into legal, financial, tax, securities, or investment advice. Avoid automatic approval or final-investment-call language.

## 8. Process

1. Split the draft into material factual claims, attributed claims, analytical inferences, working judgments, and Unknowns.
2. Match each item to source support without treating generated analysis as evidence.
3. Check source type, authority, independence, date/effective period, currentness, `as_of`, and fit for the exact claim.
4. Test whether company claims, interviews, financial snapshots, and third-party reports have been overstated or stripped of attribution.
5. Identify unsupported state or temporal inference, stale support, unresolved conflict, fabricated specificity, and prohibited certainty.
6. Preserve useful judgment by showing the reasoning and boundary; qualify or remove only what the evidence cannot support.
7. Recommend the smallest corrective action and list items requiring Human Review before circulation.

## 9. Output Format

Use a concise evidence-audit table plus an overall conclusion.

Core fields:

- `finding_id`
- `claim_or_text_span`
- `claim_classification`
- `source_support`
- `authority_independence_and_currentness`
- `issue_type`
- `conflict_or_unknown`
- `risk`
- `recommended_action_or_rewrite`
- `required_evidence`
- `needs_human_review`
- `circulation_boundary`

## 10. Human Review Requirement

Human review is mandatory. A responsible professional decides whether the evidence is sufficient, whether exceptions are justified, whether a rewrite preserves the intended judgment, and whether the workpaper may be used or circulated. The audit does not accept evidence or approve the analysis.

## 11. AI InvestOS Module Mapping

This skill maps to: **Claim-support audit / evidence boundary / circulation quality gate**.
