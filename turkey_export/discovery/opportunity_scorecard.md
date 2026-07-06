# Opportunity Scorecard

Copy this controlled record for one verified post-match opportunity. Replace every placeholder with evidence or `UNKNOWN`.

## Control

| Field | Value |
|---|---|
| Opportunity ID | OPP-XXX |
| Demand assessment / status | UNKNOWN |
| Manufacturer assessment / status | UNKNOWN |
| Match assessment / status | UNKNOWN |
| Commercial model | UNKNOWN |
| Owner / assessment date | UNKNOWN |
| Evidence cutoff / earliest expiry | UNKNOWN |

## Entry validation

- [ ] Demand, manufacturer and match assessments are accepted and refer to the same use case.
- [ ] Revenue hypothesis and execution plan exist.
- [ ] Evidence register includes dates, states, contradictions and expiry.
- [ ] Upstream status cap and duplicate check are recorded.

## Hard gates

| Gate | PASS / WATCH / FAIL | Evidence | Decision impact |
|---|---|---|---|
| Upstream records | UNKNOWN | UNKNOWN | UNKNOWN |
| Entity identity | UNKNOWN | UNKNOWN | UNKNOWN |
| Verified demand | UNKNOWN | UNKNOWN | UNKNOWN |
| Real manufacturing | UNKNOWN | UNKNOWN | UNKNOWN |
| Match viability | UNKNOWN | UNKNOWN | UNKNOWN |
| Legal/sanctions eligibility | UNKNOWN | UNKNOWN | UNKNOWN |
| Evidence integrity | UNKNOWN | UNKNOWN | UNKNOWN |

## Evidence ledger

| Claim / dimension | Evidence state | Source URL / record | Event date | Access date | Source owner/class | Contradiction / limitation |
|---|---|---|---|---|---|---|
| Demand and signal | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Manufacturer and match | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Commercial access | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Revenue model/economics | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Execution timing/dependencies | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Verification/adverse evidence | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

Allowed states: VERIFIED / ESTIMATED / HYPOTHESIS / UNKNOWN. Award caps: 100% / 50% / 25% / 0%.

## Detailed scoring worksheet

| Dimension | Subfactor | Maximum | Awarded | Evidence state | Evidence reference / rationale |
|---|---|---:|---:|---|---|
| Accessibility | Verified procurement or authorized channel | 30 | 0 | UNKNOWN | UNKNOWN |
| Accessibility | Stakeholder and decision-role specificity | 20 | 0 | UNKNOWN | UNKNOWN |
| Accessibility | Channel conflict and trust barriers | 15 | 0 | UNKNOWN | UNKNOWN |
| Accessibility | Controllability of next commercial gates | 20 | 0 | UNKNOWN | UNKNOWN |
| Accessibility | Access evidence quality and recency | 15 | 0 | UNKNOWN | UNKNOWN |
| Signal Strength | Demand directness | 30 | 0 | UNKNOWN | UNKNOWN |
| Signal Strength | Buyer and requirement specificity | 20 | 0 | UNKNOWN | UNKNOWN |
| Signal Strength | Recency and remaining action window | 20 | 0 | UNKNOWN | UNKNOWN |
| Signal Strength | Commercial urgency | 15 | 0 | UNKNOWN | UNKNOWN |
| Signal Strength | Independent corroboration | 15 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Payer and revenue-event clarity | 20 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Economics and margin/fee plausibility | 20 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Repeatability and account value | 20 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Atlas value contribution | 15 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Capital, cash-flow and liability fit | 15 | 0 | UNKNOWN | UNKNOWN |
| Revenue Potential | Demand value evidence | 10 | 0 | UNKNOWN | UNKNOWN |
| Execution Speed | Next-gate ownership and readiness | 20 | 0 | UNKNOWN | UNKNOWN |
| Execution Speed | Time to qualified commercial conversation | 20 | 0 | UNKNOWN | UNKNOWN |
| Execution Speed | Qualification and quotation path | 20 | 0 | UNKNOWN | UNKNOWN |
| Execution Speed | Time to first revenue | 25 | 0 | UNKNOWN | UNKNOWN |
| Execution Speed | Dependency, capital and reversibility fit | 15 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Entity and upstream record integrity | 20 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Directness of decisive evidence | 25 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Independent corroboration | 20 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Freshness and expiry control | 15 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Completeness of decision-critical facts | 10 | 0 | UNKNOWN | UNKNOWN |
| Verification Confidence | Contradiction and limitation handling | 10 | 0 | UNKNOWN | UNKNOWN |

## Atlas Opportunity Score

| Dimension | Weight | Score | Weighted contribution | `PROCEED` floor | Result |
|---|---:|---:|---:|---:|---|
| Accessibility | 25 | 0 | 0 | 65 | UNKNOWN |
| Signal Strength | 25 | 0 | 0 | 65 | UNKNOWN |
| Revenue Potential | 20 | 0 | 0 | 60 | UNKNOWN |
| Execution Speed | 15 | 0 | 0 | 50 | UNKNOWN |
| Verification Confidence | 15 | 0 | 0 | 70 | UNKNOWN |
| **Atlas Opportunity Score** | **100** |  | **0** |  |  |

Formula check: sum of `(dimension score × weight) / 100`; round only the final total.

## Decision

- **Decision:** PROCEED / WATCH / DROP
- **Rationale:** UNKNOWN
- **Action authorized:** UNKNOWN
- **Owner / due date / completion evidence:** UNKNOWN
- **Action not authorized:** Discovery, contact, outreach, CRM activity, quotation, order or commitment

## Verification plan

Required for `WATCH`; otherwise write `NOT APPLICABLE`.

| Missing fact | Decision impact | Smallest verification action | Owner | Due date | Expiry / review trigger |
|---|---|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Final validation

- [ ] Upstream records and status cap are recorded.
- [ ] Every hard gate is recorded and cannot be overridden by score.
- [ ] Every dimension equals its subfactor sum.
- [ ] Evidence-state caps are respected and `UNKNOWN` earns zero.
- [ ] Five weights total 100 and the final score recalculates.
- [ ] Only the final score is rounded.
- [ ] `PROCEED` passes score ≥80, every floor and every hard gate.
- [ ] `WATCH` has one bounded verification plan and expiry.
- [ ] `DROP` has a decisive evidence-backed reason.
- [ ] No upstream discovery-screening score was copied or converted.
- [ ] No discovery, contact, outreach, CRM activity or commitment occurred.
