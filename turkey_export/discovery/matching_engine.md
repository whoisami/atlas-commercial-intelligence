# Matching Engine

## Operating contract

This procedure implements [SPEC_003](../specs/03_matching_engine.md). It evaluates one proposed match among a foreign buyer need, a Turkish manufacturer and, when applicable, a sourcing company or commercial intermediary.

It does not discover entities, generate demand, enrich contacts, create CRM activity, draft/send outreach, issue quotations, place orders or authorize commitments.

## Entry gate

Open a [Matching Assessment](matching_assessment.md) only with:

- accepted demand record containing buyer/entity, country, requirement, timing, access route and status;
- accepted Turkish manufacturer record containing capability, materials, capacity/quality evidence, certifications, export readiness and status;
- sourcing-company record with mandate, access and conflicts when the match uses an intermediary;
- commercial-model hypothesis naming Atlas role, payer, revenue event and responsibilities;
- risk/contradiction record and evidence cutoff.

Set mode to `DIRECT` or `INTERMEDIARY` before scoring. An upstream `WATCH` record caps the match at `WATCH`; a decisive upstream `DROP` prevents assessment.

## Evidence states

- **VERIFIED:** directly supported by current first-party, authoritative or accepted Atlas evidence.
- **ESTIMATED:** derived from disclosed evidence and assumptions.
- **HYPOTHESIS:** plausible interpretation requiring a named test.
- **UNKNOWN:** absent, stale beyond usefulness, inaccessible or materially contradictory.

Every material claim records source URL or stable record ID, event/publication date, access date, source ownership, evidence state and limitation. `UNKNOWN` earns zero. Public contact data, supplier portals and network claims do not alone prove buyer need, mandate or access.

## Workflow

1. **Lock records and mode.** Record stable IDs, statuses, demand use case, model, owner, cutoff and expiries.
2. **Resolve entities.** Confirm buyer, manufacturer and optional intermediary are the correct operating entities.
3. **Normalize requirements.** Place buyer requirements and manufacturer evidence side by side; preserve units, standards, tolerances, materials, quantities and dates.
4. **Apply hard gates.** Test identity, demand, real manufacturing, mandatory specification, sanctions/legal eligibility, authorization and evidence integrity before scoring.
5. **Assess manufacturer-buyer fit.** Test technical, capacity, quality, delivery, qualification and economics compatibility for the same use case.
6. **Assess sourcing-company fit.** For `INTERMEDIARY`, verify mandate, category/geography, buyer access, supplier-management ability, trust, conflicts and compensation. For `DIRECT`, record `NOT APPLICABLE`.
7. **Assess commercial-model fit.** Define value, payer, revenue event, responsibilities, economics, capital/liability exposure, repeatability and first-revenue path.
8. **Score Evidence Quality and Match Score.** Use the selected mode only; do not mix columns.
9. **Decide and stop.** Record one `PROCEED`, `WATCH` or `DROP` decision and the exact next action.

## Hard gates

| Gate | PASS | WATCH | FAIL / decision |
|---|---|---|---|
| Accepted upstream records | Required records accepted and current | One record is `WATCH` or stale but recoverable | Decisive upstream `DROP` → stop |
| Entity identity | All applicable entities resolved | Resolvable ambiguity | False/unresolvable entity → `DROP` |
| Buyer demand | Current need and use case evidenced | Decisive need/timing fact missing | Demand disproven → `DROP` |
| Real manufacturing | Turkish manufacturer and relevant process verified | Capability evidence incomplete | Non-manufacturer/false claim → `DROP` |
| Mandatory requirements | No evidenced mandatory mismatch | Mandatory field `UNKNOWN` | Confirmed mismatch → `DROP` |
| Legal/sanctions eligibility | No known disqualifying conflict | Authoritative check required by signal | Confirmed prohibition → `DROP` |
| Intermediary mandate | Verified for `INTERMEDIARY`; N/A for `DIRECT` | Mandate/access unresolved | False mandate/access → `DROP` |
| Commercial model | Payer, revenue event and responsibilities plausible | One material model fact unresolved | No viable model → `DROP` |
| Evidence integrity | Sources traceable and correctly attributed | Material contradiction under review | Invented/misattributed evidence → `DROP` |

All applicable gates PASS for `PROCEED`. Numeric scores never override a failed gate.

## Manufacturer-buyer fit

Record every mandatory and material requirement in the assessment matrix. Evaluate:

- product/process, material, dimensions, tolerances and use-case compatibility;
- certification, regulatory and buyer-qualification requirements;
- capacity, MOQ, timing and scalability;
- quality control, traceability, testing and inspection evidence;
- export packaging, logistics and delivery readiness;
- order economics only where buyer and supplier evidence is comparable.

Generic portfolio overlap is insufficient. A missing mandatory requirement is `UNKNOWN` and blocks `PROCEED`; a confirmed mandatory mismatch triggers `DROP`.

## Sourcing-company fit

For `INTERMEDIARY`, score the resolved entity's verified buyer/procurement mandate, category and geography fit, decision access, supplier qualification/management capability, trust evidence, channel conflict and compensation compatibility. A website claim or contact list is weak evidence and cannot establish mandate.

For `DIRECT`, record `NOT APPLICABLE` and use the direct score and Evidence Quality columns; never assign a synthetic sourcing-company score.

## Commercial-model fit

Record who creates value, who pays, what event earns revenue, and who owns quotation, contracting, payment, quality, warranty, logistics and support. Assess fee/commission/margin assumptions, working capital, currency, tax/legal and liability risk, repeatability and elapsed gates to first revenue. Missing payer or revenue event blocks `PROCEED`.

## Evidence Quality — 0 to 100

| Component | Intermediary | Direct |
|---|---:|---:|
| Entity and upstream record integrity | 20 | 20 |
| Current, direct buyer-demand evidence | 20 | 25 |
| Manufacturer capability/capacity evidence | 25 | 30 |
| Intermediary mandate and access evidence | 15 | N/A |
| Commercial-model and economics evidence | 10 | 15 |
| Freshness, contradictions and limitations handled | 10 | 10 |
| **Total** | **100** | **100** |

Award points factor by factor with evidence references. Select one mode column. `PROCEED` requires Evidence Quality ≥70.

## Match Score — 0 to 100

| Factor | Intermediary | Direct | Evidence focus |
|---|---:|---:|---|
| Technical and specification fit | 25 | 30 | Verified compatibility with the same buyer use case |
| Capacity, quality and delivery fit | 15 | 20 | Readiness against quantity, timing, quality and logistics |
| Buyer need, timing and access | 20 | 20 | Current specific demand and plausible procurement route |
| Sourcing-company fit | 15 | N/A | Verified mandate, access, capability and conflict position |
| Commercial model fit | 15 | 20 | Payer/event, responsibilities, economics and repeatability |
| First-revenue probability | 10 | 10 | Credible bounded path with acceptable dependencies/risk |
| **Total** | **100** | **100** |  |

Use common anchors: 0 = mismatch/disproven/entirely `UNKNOWN`; 25 = weak indirect evidence; 50 = plausible with material gaps; 75 = strong current evidence; 100 = complete, verified fit without material contradiction. Intermediate scores require rationale.

`Match Score = Σ(factor score × selected-mode weight) / 100`

Round only the final score. Keep factors and weighted contributions unrounded. Do not score the intermediary factor in `DIRECT` mode.

## Decision

### PROCEED

Match Score ≥75; Evidence Quality ≥70; every applicable hard gate PASS; Technical and Specification Fit ≥70; Buyer Need/Timing/Access ≥60; Commercial Model Fit ≥60; Sourcing-Company Fit ≥60 in `INTERMEDIARY` mode; no critical `UNKNOWN`; and one deeper joint-commercial-validation action is named.

This authorizes only that validation action, never contact.

### WATCH

Use for Match Score 50–74; any upstream `WATCH`; Evidence Quality below 70; an unmet floor caused by incomplete evidence; or one realistically resolvable critical gap. Record missing fact, impact, smallest verification action, owner, due date and expiry. A score below 50 remains `WATCH` only when one bounded fact could plausibly reverse the decision.

### DROP

Use for Match Score below 50 without a credible reversal path; failed hard gate; disproven demand/capability fit; confirmed mandatory mismatch; false intermediary mandate/access; no viable commercial model; unacceptable risk; or verification cost exceeding expected value. Re-entry requires new dated evidence that changes the failed condition.

## Quality and stop rules

- Compare like-for-like units, standards, scope, dates, Incoterms and commercial bases.
- Do not infer outsourcing, mandate, quantity, price or access from generic public content.
- Record conflicts and alternative explanations, not only positive fit.
- Do not substitute a high aggregate score for mandatory-fit evidence.
- Stop when one defensible decision and next action exist.
