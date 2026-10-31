# Functional specifications

**Legend:** “Prototype” describes observed clickable behavior using synthetic data. “Production requirement” is a candidate requirement and must be designed, built and validated.

## 1. Entry and source selection

**Prototype:** Start screen titled “Connect investment”; tabs for Accounts and Add manually; search; selectable Zerodha, Groww, Angel One, ICICI Direct, Upstox, CAMS/KFintech, and NSDL/CDSL. Screen copy says data would arrive read-only through AA or consolidated account statement, while explicitly stating the prototype connects to nothing.

**Production requirement:** List only sources actually available and approved, label supported asset classes and coverage, offer manual/CAS alternatives where appropriate, show failure/unsupported states, and never imply a connection exists merely because a brand appears. Search and filters must be keyboard and screen-reader accessible.

## 2. Consent and connection

**Prototype:** Selecting a provider opens a simulated consent explanation with purpose, data requested, duration, excluded permissions, read-only assurance, an acknowledgement checkbox, Continue and Not now. It explicitly says no provider is contacted. The screen describes a one-session demo and separately mentions a 12-month production concept; this is not an approved duration or consent design.

**Production requirement:** Present a source-specific purpose, categories, frequency, duration, recipients, revocation method and consequences in counsel-approved language. Obtain valid consent through the applicable provider/AA flow; capture version, timestamp, scope, status and artefact/reference as permitted. No data retrieval before consent. Withdrawal must stop future access and trigger defined deletion/retention handling. Handle expiry, rejection, revocation, duplicate requests, timeout and provider errors.

## 3. Import, normalization and status

**Prototype:** A short progress screen lists reading the statement, grouping folios/holdings, calculating returns/allocation, and preparing an insight. It then loads the bundled sample locally.

**Production requirement:** Validate source payloads, reconcile duplicates, retain provenance, normalize identifiers, map provider states to user-readable status, and avoid displaying partial results as complete. Support idempotent retry, delayed/asynchronous completion, parser versioning, and a failed-import recovery path. Record import and calculation version and “as of” timestamps.

## 4. Portfolio home and holdings

**Prototype:** Home shows total investments ₹9,02,383, recent seven-day movement, a generated plain-language insight, statement mismatch warning, and cards for holdings, returns, allocation, performance score, benchmark, credit, loans, funds/IPO education, and related lessons. The bottom navigation includes Home, Learn, Ask Finanz (labelled not in prototype), Invest and Shop. The concept preview area labels demat opening as needing a broker partner and research desk as needing SEBI RA/RIA.

Holdings shows five sample assets across equity, hybrid and debt, values based on units × NAV, category filters, statement warnings, and details including units, NAV, estimated opening balances, XIRR/CAGR, held-since date, share, realised gain, benchmark and transactions. One statement summary mismatch is surfaced; two mutual-fund cost bases are estimated.

**Production requirement:** Portfolio totals include only eligible, current and deduplicated positions; explain exclusions. Detail each position and source. Show data freshness and estimate flags at field level. Reconciliation errors must not be silently overwritten.

## 5. Returns, allocation and comparisons

**Prototype:** Returns view shows total value, invested amount, gain, XIRR, CAGR, measured swing, realised/unrealised gains, holding-period labels and daily history. It describes long/short holding periods but explicitly says this is not tax computation. Allocation groups by asset class, fund house or sector and says shares divide group value by portfolio value. Benchmark comparisons and a performance score are clickable concepts in the sample app.

**Production requirement:** Publish precise definitions, supported instruments, periods, treatment of cash flows, fees, taxes, missing NAVs, corporate actions, price source and rounding. Benchmark availability and suitability require approved data licensing and methodology. Treat score as out of MVP unless independently validated, explainable and approved. Do not infer tax due.

## 6. Manual entry and corrections

**Prototype:** The entry toggle implies adding investments manually; production behavior is not backed by a server.

**Production requirement:** Capture only minimum fields; validate date, amount, units, currency and instrument; distinguish user-entered values; permit correction and deletion with audit history; and explain the effect on derived metrics. Do not accept credentials or trading secrets.

## 7. Education, warnings and support

**Prototype:** “Learn what … means” help buttons, lesson cards (17 total indicated), plain-language insights, and discrepancy/estimated-cost warnings are visible. Credit/loan/market tiles and two amber concepts extend beyond the investment scope.

**Production requirement:** Content must be reviewed for accuracy, neutrality and applicable regulatory restrictions. Warnings should say what differs, which source was used and what the user can do. Provide accessible support paths. Avoid presenting prototype insight prose as an approved recommendation engine.

## 8. Cross-cutting states

Production needs explicit loading, empty, partial, stale, consent-pending, consent-expired, revoked, source unavailable, parse error, unsupported data, retry, deletion pending and deletion complete states. Log security-relevant events without logging full statements or credentials. Establish monitoring and customer support ownership before launch.
