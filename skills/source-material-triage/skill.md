# Source Material Triage Skill

## 1. Skill Objective

This skill determines what materials are already available and what they can legitimately support. It classifies held materials by source type, qualitative authority, date and currentness, historical/current status, conflict, maturity, evidence boundary, and missing evidence.

It prepares a bounded source package for later analysis. It does not form an investment judgment.

## 2. Suitable Use Cases

Use this skill before quick-look analysis or workpaper drafting, especially when materials are uneven, source-limited, dated, duplicated, or inconsistent across company materials, interviews, financial records, third parties, and analyst notes.

The method is also reusable in investment banking, strategy, and corporate research when a team must understand the limits of an existing source set.

## 3. Not Suitable For

Do not use it to:

- produce an investment view or go/no-go judgment;
- fill missing customer, revenue, financing, valuation, technical, legal, or transaction facts;
- conduct a full external research program; or
- resolve a conflict by silently choosing the newest or most convenient document.

## 4. Input Requirements

Inputs should be anonymized or permissioned, source-bounded, and limited to the minimum materials relevant to the task:

- project name or anonymized case label;
- current research need and evidence `as_of` date, if known;
- available materials or bounded excerpts;
- source owner/publisher and `source_type`, when known;
- `source_date` and effective period, when known;
- known historical/current/superseded status and conflicts;
- confidentiality and use boundary.

## 5. Output Requirements

Produce a concise material inventory that states:

- source type and lightweight source reference;
- qualitative authority/evidence strength for the claim types at issue;
- source date, effective period, and currentness;
- historical, current, superseded, or unknown status;
- conflicts that remain unresolved;
- material maturity and usable evidence boundary;
- minimum relevant material context for the stated research need;
- missing evidence and focused follow-up request; and
- items requiring Human Review.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). In particular:

- company claim is not verified fact;
- user-provided is a provenance label, not proof;
- a newer document is not automatically current truth;
- Unknown and conflict must remain explicit; and
- generated summaries or classifications are not source evidence.

Use a lightweight `source_id` when available. Never fabricate a locator.

## 7. Prohibited Wording

Do not output investment recommendations, securities trading advice, legal advice, financial advice, tax advice, or deterministic conclusions. Do not invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds.

Do not describe a source as authoritative, current, independently verified, or conflict-free unless the available evidence supports that description.

## 8. Process

1. State the research need and select only the minimum relevant held materials.
2. Inventory each material without adding facts or launching broad external research.
3. Classify source type separately from file type, then record source date and effective period.
4. Assess qualitative authority and evidence strength for the specific claim the material may support.
5. Determine whether each material is historical, current, superseded, or unknown; do not infer currentness from recency alone.
6. Separate company claims, independent evidence, interview notes, financial snapshots, analyst/user notes, inferences, and Unknowns.
7. Preserve source conflicts and state what evidence could resolve them.
8. Assess package maturity and evidence boundary, then create a focused missing-evidence request.

## 9. Output Format

Use a Markdown table or lightweight structured sections. Avoid a large schema.

Core fields:

- `case_name`
- `research_need`
- `as_of`
- `materials[]`: `source_id`, `source_type`, `source_date`, `effective_period`, `authority_or_evidence_strength`, `currentness`, `historical_or_current`, `conflict`, `usable_for`, `not_usable_for`
- `material_maturity`
- `minimum_relevant_context`
- `evidence_boundary`
- `missing_evidence`
- `needs_human_review`

## 10. Human Review Requirement

Human review is mandatory before the triage output defines the source boundary for an investment workpaper, diligence plan, committee discussion, founder feedback, or business decision. A human confirms material relevance, authority, currentness, conflict treatment, and access boundaries.

## 11. AI InvestOS Module Mapping

This skill maps to: **Source triage / material maturity / evidence boundary**.
