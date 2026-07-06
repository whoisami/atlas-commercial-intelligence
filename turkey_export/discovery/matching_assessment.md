# Matching Assessment

Copy this controlled record for one proposed match. Replace every placeholder with evidence or `UNKNOWN`.

## Control

| Field | Value |
|---|---|
| Match ID | MAT-XXX |
| Mode | DIRECT / INTERMEDIARY |
| Buyer / demand record and status | UNKNOWN |
| Turkish manufacturer record and status | UNKNOWN |
| Sourcing-company record and status | NOT APPLICABLE / UNKNOWN |
| Commercial model | UNKNOWN |
| Owner / assessment date | UNKNOWN |
| Evidence cutoff / earliest expiry | UNKNOWN |

## Entry validation

- [ ] Demand record is accepted and use case is defined.
- [ ] Manufacturer record is accepted and relevant capability is evidenced.
- [ ] Intermediary record exists for `INTERMEDIARY`; it is `NOT APPLICABLE` for `DIRECT`.
- [ ] Commercial-model and risk/contradiction records exist.
- [ ] Upstream status cap is recorded.

## Evidence ledger

| Claim | Evidence state | Source URL / record | Event date | Access date | Source owner/class | Contradiction / limitation |
|---|---|---|---|---|---|---|
| Buyer identity and demand | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Requirement and timing | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Manufacturer identity/capability | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Capacity, quality and delivery | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Intermediary mandate/access | NOT APPLICABLE / UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Commercial model/economics | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Critical risk/adverse evidence | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

Allowed states: VERIFIED / ESTIMATED / HYPOTHESIS / UNKNOWN / NOT APPLICABLE where permitted.

## Hard gates

| Gate | PASS / WATCH / FAIL / N/A | Evidence | Decision impact |
|---|---|---|---|
| Accepted upstream records | UNKNOWN | UNKNOWN | UNKNOWN |
| Entity identity | UNKNOWN | UNKNOWN | UNKNOWN |
| Buyer demand | UNKNOWN | UNKNOWN | UNKNOWN |
| Real manufacturing | UNKNOWN | UNKNOWN | UNKNOWN |
| Mandatory requirements | UNKNOWN | UNKNOWN | UNKNOWN |
| Legal/sanctions eligibility | UNKNOWN | UNKNOWN | UNKNOWN |
| Intermediary mandate | UNKNOWN | UNKNOWN | UNKNOWN |
| Commercial model | UNKNOWN | UNKNOWN | UNKNOWN |
| Evidence integrity | UNKNOWN | UNKNOWN | UNKNOWN |

## Manufacturer-buyer requirement matrix

| Requirement | Mandatory? | Buyer need/evidence | Manufacturer capability/evidence | FIT / GAP / UNKNOWN | Limitation / verification |
|---|---|---|---|---|---|
| Product/process and use case | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Material/specification/tolerance | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Certification/regulatory | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Capacity/MOQ/timing | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Quality/testing/traceability | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Packaging/logistics/delivery | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Qualification/order economics | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Sourcing-company fit

For `DIRECT`, mark every row `NOT APPLICABLE`.

| Factor | Evidence state | Evidence | Fit / conflict | Rationale |
|---|---|---|---|---|
| Mandate and buyer/procurement access | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Category and geography relevance | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Supplier qualification/management ability | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Trust and operating evidence | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Channel conflict and compensation compatibility | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Commercial-model fit

| Field | Value / evidence | State / risk |
|---|---|---|
| Atlas role and created value | UNKNOWN | UNKNOWN |
| Payer and revenue event | UNKNOWN | UNKNOWN |
| Quotation/contract/payment ownership | UNKNOWN | UNKNOWN |
| Quality/warranty/logistics/support ownership | UNKNOWN | UNKNOWN |
| Fee/commission/margin basis | UNKNOWN | UNKNOWN |
| Working capital/currency/tax/liability | UNKNOWN | UNKNOWN |
| Repeatability and first-revenue path | UNKNOWN | UNKNOWN |

## Evidence Quality

Use one mode column from [Matching Engine](matching_engine.md).

| Component | Intermediary max | Direct max | Awarded | Evidence / rationale |
|---|---:|---:|---:|---|
| Entity and upstream record integrity | 20 | 20 | 0 | UNKNOWN |
| Current, direct buyer-demand evidence | 20 | 25 | 0 | UNKNOWN |
| Manufacturer capability/capacity evidence | 25 | 30 | 0 | UNKNOWN |
| Intermediary mandate and access evidence | 15 | N/A | 0 / N/A | UNKNOWN |
| Commercial-model and economics evidence | 10 | 15 | 0 | UNKNOWN |
| Freshness, contradictions and limitations | 10 | 10 | 0 | UNKNOWN |
| **Evidence Quality** | **100** | **100** | **0** |  |

## Match Score

| Factor | Intermediary weight | Direct weight | Score | Weighted contribution | Evidence state / rationale |
|---|---:|---:|---:|---:|---|
| Technical and specification fit | 25 | 30 | 0 | 0 | UNKNOWN |
| Capacity, quality and delivery fit | 15 | 20 | 0 | 0 | UNKNOWN |
| Buyer need, timing and access | 20 | 20 | 0 | 0 | UNKNOWN |
| Sourcing-company fit | 15 | N/A | 0 / N/A | 0 / N/A | UNKNOWN |
| Commercial model fit | 15 | 20 | 0 | 0 | UNKNOWN |
| First-revenue probability | 10 | 10 | 0 | 0 | UNKNOWN |
| **Match Score** | **100** | **100** |  | **0** |  |

Formula check: sum of `(factor score × selected-mode weight) / 100`; round only the final total.

## Decision

- **Decision:** PROCEED / WATCH / DROP
- **Rationale:** UNKNOWN
- **Action authorized:** UNKNOWN
- **Action not authorized:** Discovery, contact, outreach, CRM activity, quotation, order or commitment

## Verification plan

Required for `WATCH`; otherwise write `NOT APPLICABLE`.

| Missing fact | Decision impact | Smallest verification action | Owner | Due date | Expiry / review trigger |
|---|---|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Final validation

- [ ] Mode is locked and only that weight column was used.
- [ ] Upstream statuses and cap are recorded.
- [ ] Every applicable hard gate is recorded.
- [ ] Buyer and manufacturer evidence refers to the same use case.
- [ ] Every mandatory requirement is FIT for `PROCEED`.
- [ ] Intermediary mandate/access is verified or mode is `DIRECT`.
- [ ] Payer, revenue event and responsibilities are explicit for `PROCEED`.
- [ ] Evidence Quality and Match Score recalculate to the selected mode.
- [ ] `UNKNOWN` earned no points and critical unknowns block `PROCEED`.
- [ ] `PROCEED` passes total, quality, floors and hard gates.
- [ ] `WATCH` has one bounded verification plan and expiry.
- [ ] `DROP` has a decisive evidence-backed reason.
- [ ] No entity was discovered and no contact or commitment occurred.
