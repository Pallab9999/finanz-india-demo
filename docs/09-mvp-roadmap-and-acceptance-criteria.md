# MVP roadmap and acceptance criteria

Sequencing is a proposal for planning, not a delivery commitment. Dates and staffing are intentionally not estimated without provider, scope and engineering decisions.

## Phase 0 — validate the problem and constraints

Confirm target user and top jobs through research; test comprehension of sample portfolio explanations; define measures; inventory data types, source coverage and applicable roles; gather actual provider materials from Setu, Protean and CAMSFinServ; and agree boundaries for advice, tax, benchmark and concept screens.

**Exit:** product opportunity and target outcomes approved; provider/AA feasibility evidence logged; legal/security owners identified; unresolved assumptions assigned.

## Phase 1 — architecture and provider proof

Choose candidate source route(s) only after due diligence. Build a sandbox proof of consent, retrieval, revocation, payload coverage, duplicate handling and representative failure states. Define API/data contracts, threat model, retention and deletion rules, calculation specifications, operational support and localization/accessibility approach.

**Exit:** reviewed architecture decision record; signed-off data flow and consent; provider sandbox evidence; calculation test vectors; pilot plan and rollback/support design.

## Phase 2 — read-only portfolio MVP

Implement one validated source route plus manual entry or statement path as product chooses. Deliver secure identity and consent lifecycle, import status/retry, normalized positions/transactions, source timestamps, quality warnings, holdings, basic allocation, and explainable return metrics only where data quality supports them. Include withdrawal/disconnection and approved deletion handling. Keep brokerage, lending, credit bureau, personalized recommendations, trading and tax computation out of scope.

**Exit criteria:**

- Users cannot view or retrieve another user's portfolio; automated access tests cover allowed and denied paths.
- No data request is issued without current authorization; revoked/expired access prevents new fetches within the agreed time.
- Each displayed value has a source and effective date; estimates/missing inputs are visibly labelled and flow into derived metrics.
- Reconciliation failures produce a warning or unavailable metric rather than silently fabricated totals.
- Calculations match approved independent test vectors across normal, boundary and invalid cash-flow cases.
- Retry is idempotent and does not duplicate positions or transactions.
- Users can complete a withdrawal/disconnect request and see status; operational team can verify downstream propagation.
- Accessibility, localization, privacy/security, legal/compliance and incident-response release gates are met.

## Phase 3 — controlled pilot and learn

Run a limited pilot with explicit participant criteria, support coverage and monitored source reliability. Measure connection completion, data reconciliation, task comprehension, stale/partial results, revocation/deletion success and support burden. Roll back or pause if data integrity, consent, security or consumer comprehension thresholds fail.

## Phase 4 — evaluate extensions

Consider benchmarks, historical charting, more sources, educational recommendations, performance score or tax features only after evidence, data licensing, methodology and regulatory review. Treat demat/account opening, research desk and marketplace previews as separately governed proposals.

## Acceptance ownership

Product defines user outcomes and comprehension thresholds; engineering owns reliability/security and calculation behavior; legal/compliance owns regulatory and disclosure gates; security/privacy owns data controls; operations owns support/runbooks; provider management owns technical and commercial readiness. No single acceptance criterion substitutes for domain sign-off.
