# Investment Risk Radar Skill

## 1. Skill Objective

This skill maps the most important ways an investment thesis may fail and identifies the fastest evidence that could test those failure modes.

Its working chain is:

`Risk → Linked Thesis → Why It May Fail → Evidence Signal → Fastest Falsifier → Judgment Sensitivity → DD Priority`

## 2. Suitable Use Cases

Use this skill after a quick-look analysis, before diligence planning, or whenever the analysis needs a sharper anti-thesis and a prioritized verification agenda.

## 3. Not Suitable For

Do not use it as a generic risk checklist. Do not rank risks only by abstract severity or list broad market, technology, team, or financial risks without tying them to the current thesis, evidence, conflict, and possible judgment change.

## 4. Input Requirements

Inputs should be anonymized or permissioned and limited to the minimum relevant context:

- current Thesis Candidate and causal assumptions;
- Project Essence and Investment Judgment Candidate;
- Strong Counter or counter-hypotheses;
- supporting evidence, source conflicts, and `as_of`;
- evidence gaps and existing verification work.

## 5. Output Requirements

For each material risk, state:

- the linked thesis or causal assumption;
- why and how that assumption may fail;
- available evidence and observable risk signals;
- the fastest falsifier or strongest practical test;
- judgment sensitivity: what changes if the risk is confirmed or cleared;
- DD priority based on decision impact and evidence accessibility; and
- the next diligence action, target source, or material request.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Separate company claims, independent evidence, interview notes, financial snapshots, inference, Unknown, and conflict. A risk hypothesis and its proposed test are analysis and verification actions, not evidence.

## 7. Prohibited Wording

Do not output deterministic investment conclusions, claim that a risk is eliminated without adequate evidence, or invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds.

Do not turn a qualitative priority into a fabricated probability. Use `critical/high/medium/low` or a similarly simple scale only when the rationale is visible.

## 8. Process

1. Identify the thesis and causal assumptions whose failure would materially change the current view.
2. For each, explain the most plausible failure mechanism rather than naming a generic category.
3. Match available evidence, company claims, counter-evidence, conflicts, and Unknowns to that failure mechanism.
4. Define observable support and break signals, then identify the fastest practical falsifier.
5. State the judgment sensitivity of confirmation, refutation, and continued uncertainty.
6. Prioritize by expected decision impact and evidence accessibility, not severity alone.
7. Define the next DD action and hand high-priority risks to the DD Question Map.

## 9. Output Format

Use a concise risk table or lightweight structured sections.

Core fields:

- `risk_id`
- `risk_title`
- `linked_thesis_or_assumption`
- `why_thesis_may_fail`
- `evidence_status_and_signal`
- `fastest_falsifier`
- `judgment_sensitivity`
- `dd_priority`
- `diligence_action`
- `target_source_or_material_request`
- `needs_human_review`

## 10. Human Review Requirement

Human review is mandatory. The investment team confirms materiality, priority, acceptable risk, exceptions, access constraints, and how new evidence should affect the working judgment. The Skill does not decide whether to proceed or stop.

## 11. AI InvestOS Module Mapping

This skill maps to: **Thesis-linked risk radar / fastest falsification / DD priority**.
