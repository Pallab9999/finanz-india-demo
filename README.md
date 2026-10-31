# Finanz India — Investment Module

A clickable prototype and handover package for the Finanz India investment module, developed during summer in collaboration with Lollo. The product concept is a read-only, descriptive view that helps people understand their existing investments.

- **Live prototype:** [pallab9999.github.io/finanz-india-demo](https://pallab9999.github.io/finanz-india-demo/)
- **Repository:** [Pallab9999/finanz-india-demo](https://github.com/Pallab9999/finanz-india-demo)

## Important prototype boundary

The prototype runs in the browser on synthetic sample data. It has no live backend, persistence, account aggregator, financial data connections, lenders, brokers, credit bureau or market-data integrations. Provider names and consent screens are illustrative. No commercial agreement, API access, technical approval or integration commitment is represented. Do not use it with real financial data.

## Handover documentation

Read in order:

1. [Project overview](docs/01-project-overview.md)
2. [Product requirements document](docs/02-product-requirements-document.md)
3. [Functional specifications](docs/03-functional-specifications.md)
4. [User journeys](docs/04-user-journeys.md)
5. [Technical requirements](docs/05-technical-requirements.md)
6. [Account Aggregator and provider evaluation](docs/06-account-aggregator-integrations.md)
7. [Data model and calculations](docs/07-data-model-and-calculations.md)
8. [Compliance and risk considerations](docs/08-compliance-and-risk-considerations.md)
9. [MVP roadmap and acceptance criteria](docs/09-mvp-roadmap-and-acceptance-criteria.md)
10. [Open questions and decisions](docs/10-open-questions-and-decisions.md)

## Reviewing the prototype

1. Open the live prototype link above in a modern browser.
2. Start on **Connect investment**. Select a demo source and review the simulated consent explanation. Continuing loads bundled sample data; no external provider is called.
3. Explore Home, Holdings and a holding detail, Returns, Allocation and the lesson/concept previews.
4. Look for “Demo data”, “Descriptive only”, “estimated”, the statement mismatch warning, and labels explaining that features are concepts.
5. Treat every amount, provider, consent state, score and insight as illustrative, not a financial fact or production commitment.

## Developer review

The existing application is a single self-contained `index.html` deployed through GitHub Pages. There is no build/test workflow or backend contract in this repository. Review the handover before proposing a production stack. Keep prototype code and appearance unchanged while using this branch as a documentation review. Validate calculations, provider feasibility, data protection, consent and regulatory scope with the accountable teams. Use [open questions](docs/10-open-questions-and-decisions.md) to assign owners and record decisions.

## Handover status

The project brief says Setu, Protean and CAMSFinServ have been contacted. The repository did not include discussion records or evidence of a contract, live access, technical approval or integration commitment; provider diligence remains open. This documentation proposes discovery requirements and leaves architecture and compliance decisions to engineering, security, legal/compliance and product owners.
