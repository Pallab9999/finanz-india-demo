# Finanz India investment module — project overview

**Audience:** product, design, engineering, operations, compliance and legal reviewers  
**Status:** handover baseline for discovery; not an approved production design

## Purpose

This module explores how Finanz India could help a retail investor understand investments they already hold. The user can connect or add an investment portfolio, see a consolidated view, and learn what values, returns, concentration and statement warnings mean. The intended experience is descriptive and educational. It should not recommend, rank or transact investments in the initial MVP.

The work was developed during summer in collaboration with Lollo, as stated in the project brief. The repository is a public GitHub Pages prototype: [live demo](https://pallab9999.github.io/finanz-india-demo/).

## Business rationale

Investment information is fragmented across broker, registrar, depository and statement views. A plain-language, read-only portfolio view may reduce the effort required to understand holdings, performance and data quality. A connected view may also create a useful starting point for financial education and future Finanz journeys. These are product hypotheses to validate with users and stakeholders, not measured outcomes or business commitments.

## What exists today

The repository contains README.md and a 755 KB single-file index.html. The app is a client-side clickable demo using synthetic sample data. Its start screen offers account/provider choices and a manual-add option; the consent-like screen is simulated. After proceeding, it presents sample portfolio, holdings, holding detail and transaction history, returns, allocation, benchmark, performance score, statement warnings, lessons, and concept previews. The home also exposes Credit, Savings, Portfolio and Tax section labels, but Tax is explicitly outside this investment-module prototype. The “Add manually” flow offers a CAS upload/photo or typed holding form; both are mockups, with typed data held in session state only. The upload screen offers “Use the sample statement” and an error-state preview. The prototype itself identifies two amber previews as concepts requiring a licence or partner.

There is no live backend, persistence, account aggregator, broker, registrar, depository, lender, credit bureau or market data connection. Providers named in the UI are illustrative selectable choices; they are not evidence of integration. No production security, consent, calculation or regulatory controls are implemented.

## Desired outcome

Give the team a common, reviewable baseline to decide whether and how to build an MVP. The first release should focus on trustworthy, clearly sourced and understandable read-only portfolio aggregation, data-quality transparency, and safe withdrawal/deletion handling. Provider selection, market-data sourcing, legal posture and architecture remain decisions for engineering, security, product and counsel.

## Scope boundary

**Discovery/MVP candidate:** access through a validated permitted source (potentially Account Aggregator or consolidated account statement), manual entry as a fallback, normalized holdings and transactions, transparent values and return calculations, data freshness/provenance, consent lifecycle, and support/incident operations.

**Out of scope until separately approved:** order placement, personalized investment advice, research recommendations, product marketplace, account opening, lending/credit bureau services, tax advice or filing, and any use of investment data for underwriting or marketing without explicit review and authorization.

## Stakeholders and handover use

Product owns user problem and outcome measures; design owns accessible flows and comprehension; engineering owns architecture, integration feasibility and operational controls; security/privacy owns threat and data lifecycle review; legal/compliance owns regulatory applicability and required disclosures; operations owns support and incident handling; provider owners validate contracts, capabilities and onboarding. Review the ten documents in order from the README index. Record decisions and owners in [10-open-questions-and-decisions.md](10-open-questions-and-decisions.md).

## Evidence and assumptions

Evidence is limited to repository inspection, the visible prototype flow, its README and the project brief. The README describes a self-contained browser build, synthetic data, no backend or live connections, and descriptive-only intent. Sample values are dated 20 July 2026 in the UI. The task states that Setu, Protean and CAMSFinServ have already been contacted. No correspondence, proposals, API specifications, approval, commercial terms or technical commitments were available in the repository context inspected. Treat their status as “contacted; diligence pending” until the accountable owner supplies verified records.
