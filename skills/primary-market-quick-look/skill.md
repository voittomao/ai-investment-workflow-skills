# Primary-Market Quick-Look Skill

## 1. Skill Objective

This skill produces a first, evidence-bounded investment judgment candidate by answering: **What is this project really betting on?**

Its core reasoning chain is:

`Project Essence → Thesis Candidate → Strong Counter → Falsification → Value of Information → Next Verification`

The output is a working hypothesis for professional review, not an investment recommendation or accepted decision.

## 2. Suitable Use Cases

Use this skill when an investor, founder, analyst, or strategy team needs a fast but substantive company view from limited, usable materials. It is suitable when the goal is to identify the real investment bet and the evidence most likely to change the view—not to fill a standard template.

## 3. Not Suitable For

Do not use it as an investment recommendation engine, securities trading tool, legal opinion, financial advice, tax advice, or investment committee substitute. Do not use it when the source package is too weak even to state a bounded hypothesis; run Source Material Triage and retain Unknown instead.

## 4. Input Requirements

Inputs should be anonymized or permissioned and include only the minimum relevant context:

- material triage result and evidence `as_of`;
- company-provided BP or summary;
- product, customer, market, commercial, and competition evidence when available;
- financial or traction snapshots when available;
- source conflicts and known missing evidence;
- the decision or research question the quick look should inform.

## 5. Output Requirements

Produce a concise, evidence-aware working view with:

- one-sentence Project Essence;
- Business Understanding, separated from investment judgment;
- current Investment Judgment Candidate and boundary;
- Thesis Candidate with a causal chain and required assumptions;
- the Strongest Counter that could defeat or materially weaken the thesis;
- explicit falsification conditions and the fastest plausible falsifier;
- Value of Information: the next evidence most worth obtaining and why;
- core risks, conflicts, and Unknowns; and
- prioritized next verification actions.

Do not organize the main analysis mechanically as “three highlights plus three risks.” Use the causal investment question as the spine; concise lists may support it.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Attribute company claims, distinguish independent evidence, label inference, preserve Unknown and conflict, and state the evidence `as_of` where timing matters.

Generated analysis—including the Thesis Candidate—is not source evidence. Cite lightweight `source_id` references when available and never fabricate locators.

## 7. Prohibited Wording

Do not output deterministic investment conclusions or invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds. Do not present a company narrative as an independently supported thesis, or a working judgment candidate as an accepted investment view.

Avoid no-risk, guaranteed-growth, validation-complete, automatic-decision, and final-investment-call language.

## 8. Process

1. State the research question, evidence boundary, `as_of`, and material maturity.
2. Explain the Business Understanding: what the company sells, to whom, why customers may buy, and how value and economics could be created.
3. State the Project Essence in one sentence: the real business and investment-relevant bottleneck, not a category label.
4. Form a Thesis Candidate as a causal chain. Identify what must be true for the investment logic to hold.
5. Construct the Strongest Counter through inversion: if the view is wrong, identify the most plausible reason and supporting signals.
6. Define falsification conditions and the fastest fact that could materially break or weaken the logic.
7. Rank missing evidence by Value of Information: expected judgment impact, uncertainty resolved, and practical accessibility. Do not require false numerical precision.
8. End with a bounded Investment Judgment Candidate, core Unknowns, and prioritized next verification.

## 9. Output Format

Use a short Markdown memo or lightweight structured sections.

Core fields:

- `executive_snapshot`
- `evidence_as_of`
- `business_understanding`
- `project_essence`
- `investment_judgment_candidate`
- `thesis_candidate_and_causal_chain`
- `strongest_counter`
- `falsification_conditions`
- `fastest_falsifier`
- `highest_value_next_evidence`
- `core_risks_conflicts_and_unknowns`
- `next_verification`
- `needs_human_review`

## 10. Human Review Requirement

Human review is mandatory. A responsible professional confirms the problem definition, source boundary, thesis logic, strength of the counter, evidence sufficiency, exceptions, risk tolerance, and any use in a workpaper or decision process.

## 11. AI InvestOS Module Mapping

This skill maps to: **Project essence / thesis candidate / strong counter / falsification / next verification**.
