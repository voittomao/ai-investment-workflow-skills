# NovaCompute End-to-End Example

This fully fictional example shows how a first-time user can combine the six formal Skills without knowing AI InvestOS or any private system. NovaCompute is not a real company; every material, metric, customer, and transaction reference below is synthetic.

For each step, give an AI assistant the relevant `skill.md`, `input_contract.md`, `output_schema.md`, and `quality_checklist.md` together with the fictional materials. The outputs remain working candidates for Human Review.

## Case Boundary

- Evidence `as_of`: 2026-08-31 (fictional).
- Initial held materials: a fictional BP, a one-page product note, and company-claimed operating metrics.
- Later materials: fictional monthly operating data, a management interview note, and an unverified third-party article.
- Advice boundary: no investment, legal, financial, tax, or securities advice.

## Journey A — Material-led First Look

## 1. Source Material Triage

This is **Material-led** because internal company materials already exist. Start with `source-material-triage` to establish what the held materials can support.

- **Research need:** determine whether the held package supports a bounded first look.
- **Material maturity / minimum relevant context:** company-only and source-limited; sufficient to frame hypotheses, not to verify an investment judgment.

| Source | Type / date | Authority and currentness | Usable for | Not usable for |
| --- | --- | --- | --- | --- |
| Fictional BP | Company material / 2026-08-01 | `company_claim`; currentness not independently confirmed | Company narrative, product positioning | Verified customer, revenue, or performance facts |
| Product one-pager | Company material / 2026-08-03 | `company_claim`; marketing scope | Claimed workflow and feature set | Independent differentiation |
| Operating metrics page | Company report / August 2026 | `company_claim`; definitions and period need review | Testable operating claims | Verified usage, retention, or cash collection |

- **Conflict:** none observed across the held documents; absence of conflict is not independent confirmation.
- **Missing evidence:** metric definitions, cohort retention, customer-level usage, contracts/cash evidence, reproducible benchmark records, and independent market/competition sources.
- **Human Review:** confirm permission, dates, relevance, and whether this boundary is sufficient for a quick look.

## 2. Primary-Market Quick-Look

- **Business Understanding:** NovaCompute is presented as software for orchestrating AI-training workloads. `company_claim`
- **Project Essence:** the investment question is whether the product creates reproducible, recurring software value beyond cloud-native, open-source, or service-heavy alternatives. `inferred`
- **Investment Judgment Candidate:** the problem is intelligible, but differentiation, retention, and software economics remain unverified. `inferred` `missing_evidence`
- **Thesis Candidate / causal chain:** reproducible efficiency gain → embedded customer workflow → high renewal → recurring software economics. `inferred`
- **Strongest Counter:** selected benchmarks and services work may create apparent performance and retention without durable product differentiation. `inferred`
- **Falsification:** representative workloads fail to reproduce the claimed gain, or customer cohorts show weak renewal and heavy implementation dependence. `missing_evidence`
- **Highest-value next evidence:** permissioned cohort retention plus customer-level usage and cash evidence, because it tests both recurring value and commercial quality. `missing_evidence`
- **Next Verification:** run `investment-risk-radar`; send its highest-sensitivity risks to `dd-question-map`.
- **Human Review:** confirm the problem definition, evidence sufficiency, counter-thesis, and whether targeted DD is warranted.

## Journey B — Deep DD

The prior judgment is: “The core thesis depends on high renewal, but current support is mainly company claim.” This is **Deep DD**.

## 3. Investment Risk Radar

| Linked thesis | Why it may fail | Evidence signal | Fastest falsifier | Judgment sensitivity | DD priority | Target / next action |
| --- | --- | --- | --- | --- | --- | --- |
| High renewal proves recurring value | Reported renewal may exclude churned pilots or include service-led contracts | Cohort definition, eligible denominator, contract status, usage and cash | Reconcile one permissioned renewal cohort from eligible customers through contract, usage, invoice, and cash | Low true renewal materially weakens recurring-value and software-economics judgments | Verify first | Permissioned customer-level cohort; request reconciliation table |

## 4. DD Question Map

| Research need | Value of Information | Verification target | Question / material request | What answer changes the judgment? |
| --- | --- | --- | --- | --- |
| Establish true renewal | High: directly tests the core thesis | Eligible customer cohort | Provide cohort rules and customer-level start, renewal, churn, usage, invoice, and cash fields | Low renewal or service-only renewal weakens the thesis; consistent paid renewal strengthens it; incomplete fields retain Unknown |
| Separate product pull from services | High: tests scalability | Delivery effort by renewed customer | Provide implementation hours, support hours, reusable components, and exceptions | Persistent heavy customization weakens software scalability even if contracts renew; inaccessible customer-level data retains Unknown |

Questions and requests are verification actions, not evidence. Human reviewers confirm permissions, proportionality, target sources, and how obtained answers should move the judgment.

## Journey C — Incremental Update and Evidence Audit

Assume a V1 judgment dated 2026-08-31. In September, fictional monthly operating data, a management interview, and an unverified third-party article arrive. This is **Incremental Update**.

## 5. Versioned Investment Update

| Delta | Synthetic result |
| --- | --- |
| Prior judgment / `as_of` | Retention is central but unverified as of 2026-08-31 |
| Material Delta | Three new logical materials arrived |
| Evidence Delta | Company data and interview add detail but remain company-side claims; the article adds a non-independent/unverified market signal |
| Judgment Delta — strengthened | None yet; no independent customer or cash evidence |
| Judgment Delta — weakened | Confidence in the headline renewal metric declines if cohort definitions differ across materials |
| Judgment Delta — unchanged | Recurring customer value remains the core question |
| Still Unknown | Eligible denominator, churned pilots, paid renewal, usage depth, service intensity |
| Risk / DD change | Cohort-definition conflict becomes verify-first; request customer-level renewal, usage, and cash reconciliation |
| Candidate update | Retain the V1 boundary and prioritize cohort reconciliation; do not overwrite history |

Human Review confirms the historical baseline, source authority/currentness, conflicts, and whether any candidate update should be adopted.

## 6. Investment Evidence Audit

| Draft claim | Finding | Smallest corrective action |
| --- | --- | --- |
| “Renewal proves strong product-market fit.” | Company-reported metric lacks cohort, usage, and cash support; overclaim | Attribute the claim, state the missing denominator, and retain the judgment as Unknown pending cohort evidence |
| “An independent report confirms market leadership.” | The article's independence, date, and method are unverified | Describe it as an unverified third-party report and request source/method review |
| “The risk is resolved after management explained it.” | Interview explanation is not resolution evidence; unsupported state inference | Record the explanation as `interview_note`; keep the risk open for Human Review |

The audit does not approve circulation. A human decides whether support is sufficient and whether the workpaper may be used.

## Journey D — Greenfield Honesty Boundary

With no internal material, the mode is **Greenfield**. The six formal Skills do **not** include a complete external source-discovery Skill. `External Research & Evidence Build` remains a Candidate under real-world validation.

A user may collect permissioned public materials with their ordinary browser, research tool, or AI assistant, recording source, publisher, date, `as_of`, and access boundary. Once a bounded source set exists:

1. run `source-material-triage` to classify authority, currentness, conflicts, and missing evidence;
2. run `primary-market-quick-look` only if the source set supports a bounded hypothesis; and
3. retain Unknown and request evidence when it does not.

This repository does not claim to perform automatic web discovery, provide a production CLI, or supply a seventh formal Skill.

## End State

The six Skills produce a source-bounded working judgment, thesis-linked risks, decision-changing DD, a traceable candidate update, and an evidence audit. Human Review remains responsible for evidence sufficiency, exceptions, judgment adoption, risk acceptance, and any business or investment decision.
