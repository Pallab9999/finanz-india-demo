# Product requirements document

**Status:** proposed requirements for discovery and MVP validation  
**Product:** Finanz India investment module

## Problem and opportunity

A retail investor may hold mutual funds, listed securities or other permitted products through several intermediaries and receive inconsistent summaries. The module should reduce the work needed to answer: what do I hold, what is it worth, what changed, how was performance calculated, and which source records are incomplete? The product hypothesis is that plain-language explanation plus clear provenance is more useful and safer than an unexplained aggregate number.

## Users and needs

- **Retail investor:** understand holdings, value, allocation and performance without needing to interpret every provider statement.
- **Investor with incomplete records:** understand which figures are estimated or missing and how to correct them.
- **First-time digital investor:** learn common concepts without being directed toward a product or trade.
- **Support/operator:** diagnose failed refreshes, consent status and data-quality issues without unnecessary exposure to financial data.

Personas, accessibility needs, language preferences, target segments and research evidence require validation.

## Goals and measures

Proposed outcomes: users can identify the source and “as of” date for portfolio data; explain the difference between value, invested amount and gain after viewing an explanation; complete a read-only connection or manual entry with informed consent; and find and resolve data-quality warnings. Proposed measures include connection completion and failure rates, time to understand portfolio summary, comprehension task success, data reconciliation rate, consent withdrawal completion, and support contacts per connected portfolio. Set targets after baseline research. Do not optimize for trades or product uptake in this descriptive MVP.

## Product principles

1. Read-only by default, with purpose-limited data access.
2. Explain every important number, its date, source and calculation.
3. Distinguish provider facts, user-entered facts, estimates and derived values.
4. Make limitations, stale data and partial coverage visible.
5. Let the user review, correct, disconnect and request deletion through defined flows.
6. Accessible, mobile-first language; localized copy and Indian number/currency conventions.
7. No recommendation, suitability claim, performance promise or transaction in the MVP.

## MVP scope proposal

**P0:** portfolio onboarding; informed source-specific consent; supported data retrieval with status and retry; manual portfolio/transaction entry; normalized holdings; portfolio total and allocation; return metrics only when input quality supports them; provenance/freshness; clear warnings; holding/transaction detail; consent withdrawal and data deletion; help/support and auditability.

**P1:** benchmark comparisons with licensed/approved data and methodological disclosure; educational content; additional asset/source coverage; richer historical charts.

**Later/conditional:** performance score, tax-related views, account-opening and research previews, marketplace, any personalized recommendation or transaction. Amber concept screens are expressly not production functionality.

## Non-goals

Investment execution, automated trading, buy/sell/hold advice, credit scoring, lending eligibility, tax computation, and assuming a provider is an approved partner.

## Functional and quality expectations

See [03-functional-specifications.md](03-functional-specifications.md), [05-technical-requirements.md](05-technical-requirements.md), and [09-mvp-roadmap-and-acceptance-criteria.md](09-mvp-roadmap-and-acceptance-criteria.md). Before launch, define service-level objectives, supported devices, accessibility standard, language coverage, refresh policy, source coverage, data retention, customer support and incident SLAs with accountable teams.
