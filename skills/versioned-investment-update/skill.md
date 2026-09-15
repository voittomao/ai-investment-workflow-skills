# Versioned Investment Update Skill

## 1. Skill Objective

This skill preserves a historical investment judgment and explains what actually changed when new material or events arrive.

It keeps three deltas separate:

- **Material Delta:** what new or changed materials became available.
- **Evidence Delta:** what support, contradiction, authority, currentness, or Unknown changed because of those materials.
- **Judgment Delta:** what working conclusion, confidence, thesis, risk, or DD priority changed because of the Evidence Delta.

New material does not automatically overwrite the prior judgment. The output is a candidate update for Human Review.

## 2. Suitable Use Cases

Use this skill when an existing quick look or investment workpaper must be updated after new financial snapshots, customer evidence, technical materials, interviews, market events, diligence results, or other decision-relevant information.

## 3. Not Suitable For

Do not use it to:

- rewrite a fresh report without preserving the historical view;
- treat document arrival as evidence improvement;
- mark a risk resolved merely because the company answered a question;
- silently replace an accepted or working judgment; or
- implement approval, promotion, storage, or runtime state transitions.

## 4. Input Requirements

Inputs should be anonymized or permissioned and include only the minimum relevant context:

- prior workpaper or judgment and `prior_judgment_as_of`;
- prior evidence boundary and source references;
- new material inventory with source dates/effective periods;
- extracted new evidence and `evidence_as_of`;
- prior thesis, risks, DD issues, and Unknowns;
- known source conflicts, supersession, and unchanged items;
- Human Review notes and the decision question for the update.

## 5. Output Requirements

Produce a traceable update with:

- prior judgment and its `as_of` boundary;
- Material Delta;
- Evidence Delta, including new support, contradiction, currentness/authority change, conflict, and remaining Unknown;
- Judgment Delta, classified as strengthened, weakened, unchanged, newly introduced, resolved/de-risked, or still Unknown;
- reasons and evidence references for each material judgment movement;
- changed risks and DD priorities;
- candidate judgment update and workpaper changes; and
- explicit Human Review requirements.

An unchanged judgment is a valid result. It must not be rewritten as improvement merely because new documents exist.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). A new source may create a Material Delta without creating an Evidence Delta. An Evidence Delta may be real without being sufficient to create a Judgment Delta.

Generated comparison or update prose is not source evidence. Preserve source date, effective period, `as_of`, attribution, Unknown, and conflict.

## 7. Prohibited Wording

Do not output deterministic investment conclusions or invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds. Do not claim “verified,” “resolved,” “current,” or “de-risked” without evidence adequate to that specific statement.

Do not call the candidate update accepted, approved, final, or current. This public Skill describes a professional update method, not private state-machine mechanics.

## 8. Process

1. Freeze the prior judgment, `prior_judgment_as_of`, and prior evidence boundary. Do not rewrite history.
2. Identify the Material Delta using logical materials rather than confusing files, extracts, and evidence items.
3. Assess each new source's type, authority, date/effective period, currentness, independence, and conflict status.
4. Determine the Evidence Delta: new support, weakening evidence, contradiction, authority/currentness change, resolved conflict, new conflict, or no evidence change.
5. Determine the Judgment Delta only from the Evidence Delta. Classify each material view as strengthened, weakened, unchanged, newly introduced, resolved/de-risked, or still Unknown.
6. Explain why each judgment, risk, or DD priority changed—or why it did not.
7. Produce a candidate judgment update and focused workpaper edits for Human Review.

## 9. Output Format

Use a concise version summary plus three delta tables or lightweight structured sections.

Core fields:

- `prior_version_or_judgment`
- `prior_judgment_as_of`
- `prior_evidence_boundary`
- `material_delta`
- `new_evidence`
- `evidence_as_of`
- `evidence_delta`
- `judgment_delta`: `strengthened`, `weakened`, `unchanged`, `newly_introduced`, `resolved_or_de_risked`, `still_unknown`
- `risk_and_dd_changes`
- `candidate_judgment_update`
- `workpaper_update_recommendations`
- `needs_human_review`

## 10. Human Review Requirement

Human review is mandatory. A responsible professional confirms the historical baseline, evidence authority/currentness, conflict resolution, reasons for belief movement, unchanged items, exceptions, and whether any candidate update should be adopted for professional use.

## 11. AI InvestOS Module Mapping

This skill maps to: **Material Delta / Evidence Delta / Judgment Delta / candidate update**.
