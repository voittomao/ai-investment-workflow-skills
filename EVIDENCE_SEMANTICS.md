# Shared Evidence Semantics

These are lightweight public semantics for all six workflow skills. They are not a database schema, authority-ranking algorithm, or runtime routing system. Use only the fields that help the current professional task.

## Minimal Vocabulary

| Term | Meaning | Usage boundary |
| --- | --- | --- |
| `source` / `source_id` | The material or record behind a statement, with a lightweight locator when available | A locator improves traceability; it does not prove that the statement is true |
| `source_type` | The source's role, such as company-provided material, interview, financial record, independent third party, user/analyst note, or derived representation | Source type and file format are different concepts |
| `source_date` | Publication, interview, reporting, or capture date, when known | Also record the effective period when it differs from the document date |
| `as_of` | The cutoff date for the evidence set or working judgment | Later material is not automatically more authoritative or current |
| `authority` / `evidence_strength` | A qualitative assessment of how directly and reliably a source supports the specific claim | Keep the rationale visible; do not imply a universal numeric ranking |
| `user_provided` | Material or context supplied by the user | Provenance label only; user-provided does not automatically mean verified |
| `company_claim` | A statement made by the company, founder, management, or company-authored material | Preserve attribution until independently corroborated |
| `independent_evidence` | Evidence produced by a source meaningfully independent of the company claim being tested | Independence does not remove the need to assess method, date, and relevance |
| `interview_note` | A note or summary of what an interviewee said | Record speaker/date when available; do not treat a summary as the underlying record |
| `financial_snapshot` | Financial or operating figures from a report, model, management account, or extract | State period, unit, scope, and audit status when known |
| `third_party_unverified` | Third-party information whose provenance or support has not yet been checked | Do not relabel it as independent confirmation without review |
| `inferred` | Analysis derived from available evidence rather than stated directly by a source | Show the reasoning and what evidence could change it |
| `unknown` / `missing_evidence` | A decision-relevant fact or support relationship that is not established | Keep it explicit and convert it into a focused verification action when useful |
| `conflict` | Sources, dates, definitions, or states that cannot yet be reconciled | Preserve competing accounts and identify what could resolve them |
| `needs_human_review` | A judgment, exception, or evidence boundary that a responsible professional must review | It never substitutes for missing evidence or turns a candidate into an accepted conclusion |

## Five Invariants

1. **Company claim is not verified fact.** Preserve who made the claim and what independent corroboration is missing.
2. **Generated analysis is not source evidence.** A model's summary, inference, or rewrite cannot support itself.
3. **Newer document is not automatically current truth.** Check effective period, authority, definitions, supersession, and conflict.
4. **Unknown remains explicit.** Do not fill evidence gaps with plausible detail or hide them behind confident prose.
5. **Human Review remains required.** These skills prepare research work; they do not accept evidence, approve a workpaper, or make an investment or business decision.

## Lightweight Use

- Cite a filename, page, section, interview date, or spreadsheet tab when available; never fabricate a locator.
- Apply labels at the claim or evidence-item level when practical. A document can contain both supported facts and unsupported claims.
- Use qualitative evidence strength only when it helps the decision. Explain why the source is fit for the specific claim.
- Treat questions, material requests, planned searches, and generated analysis as verification actions or analysis—not as evidence.
- When sources conflict, report the conflict and the evidence needed to resolve it instead of silently selecting a preferred version.

The workflow may fail closed when a required evidence or Human Review boundary is unmet. How a private system routes, stores, promotes, or recovers state is outside this public reference.
