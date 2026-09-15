# DD Question Map Skill

## 1. Skill Objective

This skill turns investment judgments and prioritized risks into a focused diligence map. Every high-priority item should answer: **What answer would change the judgment?**

Its working chain is:

`Judgment or Risk → Research Need → Value of Information → Verification Target → Interview Question / Material Request → Expected Judgment Impact`

## 2. Suitable Use Cases

Use this skill when a team must move from risk thinking to executable management, technology, customer, commercial, financial, operational, legal, transaction, or third-party diligence.

## 3. Not Suitable For

Do not reduce diligence to interview questions, reward question count, or create broad checklists disconnected from a judgment. Do not create questions that assume unverified facts are true, and do not treat a question or material request as supporting evidence.

## 4. Input Requirements

Inputs should be anonymized or permissioned and limited to the minimum relevant context:

- current Investment Judgment Candidate and Thesis Candidate;
- risk radar and judgment sensitivities;
- known evidence gaps and conflicts;
- available target sources and access constraints;
- prior diligence results, if any;
- human priorities and the decision the DD must inform.

## 5. Output Requirements

For each material issue, state:

- linked judgment, thesis assumption, or risk;
- precise research need;
- Value of Information and priority rationale;
- verification target and best available target source;
- interview question, material request, data check, test, or third-party validation task;
- evidence that would support, weaken, or break the view;
- expected judgment impact for plausible answer branches; and
- next action, owner, or escalation for Human Review when relevant.

## 6. Shared Evidence Semantics

Follow the repository's [Shared Evidence Semantics](../../EVIDENCE_SEMANTICS.md). Existing evidence may motivate a DD item, but questions, requests, planned searches, and expected answers are verification actions—not evidence.

Preserve Unknown and conflict until the requested evidence is actually obtained and reviewed.

## 7. Prohibited Wording

Do not output investment recommendations or invent customers, revenue, financing, valuation, technical metrics, transaction terms, or founder backgrounds. Do not imply that asking a question, receiving a company response, or requesting a document resolves the underlying risk.

Do not generate intrusive, unauthorized, or legally improper requests. Specialist legal, financial, tax, privacy, and technical scope remains subject to qualified professional review.

## 8. Process

1. Start from the judgment or risk that may change; do not start from a generic category checklist.
2. Define the unresolved research need and why it matters now.
3. Assess Value of Information qualitatively using expected judgment impact, uncertainty resolved, accessibility, time, and cost.
4. Choose the verification target and the source most capable of answering it.
5. Design the smallest useful interview question, material request, data check, technical test, customer reference, or third-party task.
6. State support, weaken, break, and remain-Unknown signals, plus their expected judgment impact.
7. Prioritize the issue and define the next action. Do not optimize for the number of questions.

## 9. Output Format

Use a concise DD issue map or lightweight structured sections.

Core fields:

- `dd_id`
- `linked_judgment_or_risk`
- `research_need`
- `value_of_information`
- `verification_target`
- `target_source`
- `interview_question`
- `material_request_or_other_task`
- `support_weaken_break_unknown_signals`
- `expected_judgment_impact`
- `priority_and_next_action`
- `needs_human_review`

## 10. Human Review Requirement

Human review is mandatory. The responsible team confirms necessity, proportionality, permissions, wording, target source, specialist scope, and how obtained evidence should change the judgment.

## 11. AI InvestOS Module Mapping

This skill maps to: **Judgment-linked DD map / verification design / expected decision impact**.
