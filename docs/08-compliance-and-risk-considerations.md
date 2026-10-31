# Compliance, privacy and risk considerations

This is a review checklist, not legal advice or a determination of applicable laws. Legal/compliance teams must validate the current Indian regulatory framework, entity roles and exact product behavior before any real data is collected or product is launched.

## Regulatory boundary

The prototype's copy describes the experience as descriptive-only, says it gives no investment advice and shows no order placement. That intent does not by itself establish the regulatory classification of a production service. Product wording, personalized analysis, rankings, benchmark comparisons, marketing, distribution and partner flows can affect obligations. The concept previews themselves mention a broker partner and SEBI RA/RIA; they are explicitly not approved production features. Counsel should determine whether any proposed activity requires registration, authorization, disclosure, supervision or a regulated partner.

AA eligibility/role, consent wording and data handling must be validated with the appropriate participants and legal counsel. Contacting Setu, Protean and CAMSFinServ does not establish approval, access or a contract.

## Personal and financial data

Treat investment holdings, transaction history, identifiers, consent records and derived metrics as sensitive. Before design, map every data element, purpose, recipient, storage location, access role, retention and deletion behavior. Confirm applicable privacy/data protection, financial-sector and cybersecurity requirements; do not infer that consent alone resolves every obligation.

Apply data minimization, purpose limitation, transparent notices, access controls, encryption, secure secret handling, redacted observability, retention limits and tested deletion. Prohibit using investment data for credit underwriting, advertising, cross-selling or another purpose unless separately reviewed and supported by valid authorization and governance.

## Consent and user rights

Consent should be understandable, specific, informed, purpose-bound, recorded, and revocable through the appropriate flow. Explain duration, data categories, frequency, recipients, consequences and withdrawal. Maintain consent version and state. Make revocation propagate to retrieval jobs. Design correction, access, grievance and deletion pathways with legal/provider input. Define legal retention exceptions and how they are explained to users.

The prototype's acknowledgement checkbox and mock 12-month duration are demonstrations only; neither is a production consent model or approved retention period.

## Consumer protection and presentation

Avoid misleading completeness, performance promises, guaranteed outcomes, implied endorsement or actionable buy/sell advice. Show date, provenance, assumptions, estimates, fees/tax limitations and calculation methodology. Explain that past returns do not predict future results. Benchmark and performance-score views need independent methodology review, source licensing, context and bias testing before release. Tax-related labels must not look like a tax computation or filing recommendation.

Ensure disclosures are accessible, local-language tested and available before the user acts. Clearly distinguish educational content from personalized financial recommendations.

## Threats and controls to validate

| Risk | Candidate control |
|---|---|
| Unauthorized account linkage or cross-user data exposure | Strong identity binding, server-side authorization, tenant isolation, negative tests, least privilege |
| Over-broad/stale consent | Scope checks on every fetch, expiry/revocation enforcement, periodic reconciliation |
| Credential/token leakage | No provider secrets in client, managed secret storage, short-lived tokens, redacted logs |
| Incorrect portfolio / return result | Provenance, quality flags, calculation versioning, independent test vectors, reconciliation and correction path |
| Provider outage or malicious payload | Signature/authenticity checks, schema validation, isolation, safe retry and incident escalation |
| Misleading advice-like insight | Content/legal review, explicit descriptive scope, no recommendations, feature gate |
| Excessive retention or secondary use | Approved schedule, deletion propagation, purpose enforcement and audit |
| Misuse by staff | Role-based access, just-in-time access, audit, training and alerting |

## Required reviews before pilot

Legal/compliance: entity/role classification, AA/financial data rules, advice/distribution implications, disclosures, consent and grievance process. Security/privacy: threat model, DPIA or equivalent assessment if required, data map, vendor risk, retention/deletion, incident playbook and pen-test scope. Product/design: comprehension, accessibility, language and vulnerable-user review. Engineering/operations: secure environment, monitoring and recovery. Obtain sign-offs from named accountable owners; this document grants none.
