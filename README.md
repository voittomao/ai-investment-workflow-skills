# AI Investment Workflow Skills

**Evidence-disciplined AI workflow skills for investor-style company research, business model understanding, diligence planning, versioned updates, and evidence review.**

[中文镜像 / Chinese mirror](README.zh-CN.md)

These workflow skills were originally designed from a primary-market technology investing context, but they are also useful for founders, analysts, strategy teams, product and business operators, and anyone who wants to understand a company through an investment research lens.

This is not a prompt collection. It is a small workflow package: each skill defines input boundaries, output structure, evidence discipline, prohibited wording, quality checks, sample inputs, sample outputs, and its relationship to an AI InvestOS-style investment workflow.

## What This Is Not

- Not an investment recommendation engine.
- Not legal, financial, tax, securities trading, or investment advice.
- Not a substitute for professional diligence, human judgment, investment committee review, or business decision-making.
- Not a claim that AI can automatically decide whether to invest.
- Not based on real project data. All examples are fictional and require human review.

## Who It Is For

**Core users**

- Primary-market investors and investment analysts.
- Venture capital, growth equity, CVC, strategic investment, and corporate strategy teams.
- FA / fundraising advisors and diligence teams.
- Technology, AI, robotics, AI infrastructure, and AI agent industry researchers.

**Extended users**

- Founders who want to understand how investors may read a company.
- Product, strategy, business operations, and commercial analysis teams.
- Readers who want to understand a company through project essence, business model, risk hypotheses, diligence questions, version changes, and evidence boundaries.

## 30-Second Overview

This repository helps turn company materials into structured investor-style research:

1. Triage source materials and evidence boundaries.
2. Produce a quick-look company analysis.
3. Map investment logic into risk hypotheses.
4. Convert risks into diligence questions and material requests.
5. Update the analysis when new materials arrive.
6. Audit the draft before an investment workpaper is circulated.

Commercial and business model understanding are core objects inside the investment research workflow. They are not positioned here as a generic business-analysis slogan.

## Recommended Starting Points

1. [`primary-market-quick-look`](skills/primary-market-quick-look/README.md)  
   Reason: the best starting point for understanding how to analyze a company through an investment research lens.

2. [`investment-risk-radar`](skills/investment-risk-radar/README.md)  
   Reason: converts highlights, assumptions, and evidence gaps into risk hypotheses and verification actions.

3. [`versioned-investment-update`](skills/versioned-investment-update/README.md)  
   Reason: shows the core workflow difference: new materials should update and explain judgment changes instead of simply overwriting the prior report.

`dd-question-map` remains the execution layer that turns risks into interview questions, material requests, data checks, technical validation, customer references, and transaction review. `investment-evidence-audit` remains the evidence boundary gate before an investment workpaper is circulated.

## Workflow

```mermaid
flowchart LR
  A["Source material triage"] --> B["Primary-market quick look"]
  B --> C["Investment risk radar"]
  C --> D["DD question map"]
  D --> E["Versioned investment update"]
  E --> F["Investment evidence audit"]
  F --> G["Investment analysis workpaper"]
```

## Six Skills

| Skill | Role | Main Output |
| --- | --- | --- |
| [`source-material-triage`](skills/source-material-triage/README.md) | Classify project materials and evidence boundaries | Material inventory, maturity, missing materials |
| [`primary-market-quick-look`](skills/primary-market-quick-look/README.md) | First-pass investor-style company view | Project essence, investment logic, highlights, counter-hypotheses |
| [`investment-risk-radar`](skills/investment-risk-radar/README.md) | Risk mapping from logic and evidence gaps | Linked risk hypotheses and verification actions |
| [`dd-question-map`](skills/dd-question-map/README.md) | Diligence execution map | Interview questions, material requests, data checks, technical and transaction validation |
| [`versioned-investment-update`](skills/versioned-investment-update/README.md) | Update analysis after new materials | V1/V2 judgment change summary |
| [`investment-evidence-audit`](skills/investment-evidence-audit/README.md) | Evidence boundary quality gate | Overstatement flags and rewrite suggestions |

## Evidence Labels

Use these labels consistently:

- `user_provided`: material provided by the user.
- `company_claim`: company statement that has not been independently verified.
- `interview_note`: interview note or meeting summary.
- `financial_snapshot`: financial or operating data snapshot.
- `third_party_unverified`: third-party material that still requires verification.
- `inferred`: analytical inference made from available material.
- `missing_evidence`: required evidence not yet available.
- `needs_human_review`: item requiring human review before circulation.

## Public Boundary

- All examples use the fully fictional company **NovaCompute**.
- All numbers, customers, materials, revenue, financing, valuation, and transaction references in examples are fictional examples.
- Outputs must be reviewed by humans before use.
- These workflows are designed for research organization and evidence discipline; they do not produce investment, legal, financial, tax, or securities trading advice.

## End-to-End Example

See [`examples/nova_compute_end_to_end.md`](examples/nova_compute_end_to_end.md) for a fictional walkthrough across all six skills.

## Relationship to AI InvestOS

AI InvestOS is a broader workflow concept for organizing investment research, evidence discipline, risk mapping, diligence planning, versioned workpapers, and human review. This repository extracts a public, data-free workflow layer that can be reused independently.

## Repository Structure

```text
README.md
README.zh-CN.md
LICENSE
RELEASE_CHECKLIST.md
CONTRIBUTING.md
CHANGELOG.md
examples/
  nova_compute_end_to_end.md
  nova_compute_end_to_end.zh-CN.md
skills/
  source-material-triage/
  primary-market-quick-look/
  investment-risk-radar/
  dd-question-map/
  versioned-investment-update/
  investment-evidence-audit/
```

Each skill directory contains the English canonical files plus a `zh-CN/` mirror.

## How to Reference

Suggested neutral wording:

> AI Investment Workflow Skills is an open workflow package for evidence-disciplined, investor-style company research and primary-market diligence. It includes six reusable skills covering source triage, quick-look analysis, risk mapping, DD question design, versioned updates, and evidence review.

## License

See [`LICENSE`](LICENSE).
