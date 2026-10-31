# Open questions and decisions

Use this log during handover. “Open” means the repository/context reviewed did not resolve the item. Assign an owner and evidence before treating a row as decided.

| ID | Question / decision | Proposed owner(s) | Evidence needed / gate | Status |
|---|---|---|---|---|
| D1 | Which investor segment and primary job should MVP serve? | Product / research | User interviews, task tests, outcome baseline | Open |
| D2 | What was agreed or learned in discussions with Setu, Protean and CAMSFinServ? Who owns each relationship? | Provider/commercial owner | Dated correspondence, exact entity/role, proposal, next step | Contacted per brief; details unavailable |
| D3 | What role would Finanz play in any AA flow, and is it eligible for the intended use? | Legal/compliance + provider | Current framework review and provider confirmation | Open |
| D4 | Which source route is feasible: AA, CAS import, manual entry, or a combination? | Product + engineering | Coverage, user research, provider sandbox, data quality | Open |
| D5 | Which instruments and account types are in MVP, and how are duplicates/joint accounts handled? | Product + data engineering | Source schema coverage and reconciliation rules | Open |
| D6 | Where will the service run, and which identity, API, storage, key management and observability components are approved? | Engineering + security | Architecture ADR, threat model, vendor/security review | Open |
| D7 | What data is stored, for how long, and how do deletion, backup expiry and legal holds work? | Privacy/legal + engineering | Data map, applicable obligations, retention schedule | Open |
| D8 | What consent purposes, categories, duration, frequency, renewal and revocation SLA apply? | Legal/compliance + provider | Approved copy, protocol, tested revocation | Open |
| D9 | What exactly does “amount invested” mean with withdrawals, charges, opening balances and estimates? | Product + finance/data | Metric specification and sample reconciliation | Open |
| D10 | How are XIRR, CAGR, measured swing, realised/unrealised gains and missing flows defined? | Product + engineering + finance | Versioned methodology, edge-case test vectors | Open |
| D11 | Is market pricing needed, which source is licensed, and how fresh must values be? | Product + commercial + legal | Source contracts, costs, valuation policy | Open |
| D12 | Are benchmark comparison and performance score in scope? If so, what methodology and disclosures? | Product + legal/compliance + data | Licensing, methodology validation, consumer review | Open |
| D13 | Can tax-related educational holding periods be shown, and who validates rule changes? | Legal/tax + product | Current advice and maintenance process | Open |
| D14 | Which languages, accessibility standard and support hours are required? | Product/design/operations | Research, accessibility audit, localization plan | Open |
| D15 | What is the intended business model and success metric without optimizing for trades or recommendations? | Product/leadership | Strategy, unit economics and outcome approval | Open |
| D16 | How should source outage, partial import, correction, grievance and incident escalation work? | Operations + engineering + provider | Runbooks, SLAs and tested scenarios | Open |
| D17 | Should manual statement upload exist; if so, what file handling, retention, malware scanning and extraction controls apply? | Product + security/privacy | Threat model, secure ingestion design, user research | Open |

## Decision record template

For each closed item, record: decision; date; accountable approver; alternatives considered; evidence links; assumptions; impact on scope/data/security; and conditions for revisiting. Do not mark provider interest as approval, sandbox availability as production authorization, or a technical design as legal sign-off.

## Initial assumptions to validate

- The initial experience is read-only and descriptive, as the prototype copy suggests.
- A user values an aggregate view more than another provider-specific view.
- A reliable source can provide enough history for useful returns.
- Manual entry or CAS can be a workable fallback.
- Data provenance and estimate warnings improve trust and comprehension.
- User consent, withdrawal and deletion can be implemented consistently with the selected flow.

These are hypotheses; none is confirmed by the prototype alone.
