# SPEC_004 — Opportunity Scoring

## Purpose

Define how Atlas ranks a verified Turkey → World commercial opportunity by its probability of reaching first revenue. The specification consumes accepted upstream evidence; it does not discover demand, manufacturers, buyers or intermediaries. It implements nothing and authorizes no outreach, CRM activity, quotation, order or commitment.

## Inputs

| Input | Required content | Evidence rule |
|---|---|---|
| Demand assessment | Signal ID, foreign buyer/segment, need, timing, access route, decision | Accepted record with dated sources; upstream `WATCH` caps the result at `WATCH` |
| Manufacturer assessment | Turkish manufacturer ID, capability, export need/readiness, decision | Accepted record with identity and manufacturing evidence |
| Match assessment | Buyer-manufacturer fit, intermediary fit when applicable, model fit, decision | Accepted matching record; failed hard gate cannot be rescored away |
| Revenue hypothesis | Commercial model, payer, revenue event, value range or `UNKNOWN`, repeatability | Estimates and assumptions explicitly labeled |
| Execution plan | Next gates, owners, dependencies, expected elapsed time, capital exposure | Unowned or indefinite work scores conservatively |
| Evidence register | Sources, dates, evidence states, contradictions, expiry | Public or authorized evidence only; unsupported facts are `UNKNOWN` |

Resolve all entities, deduplicate inputs and apply the earliest evidence expiry. Invented, misattributed or materially contradictory evidence fails the integrity gate.

## Outputs

- Opportunity scorecard: stable IDs, evidence cutoff, five dimension scores, weights and weighted Atlas Opportunity Score.
- Gate result: identity, verified demand, real manufacturing, match viability, legal/sanctions eligibility and evidence integrity.
- Decision: `PROCEED`, `WATCH` or `DROP`, rationale, authorized next action and action not authorized.
- Verification plan for `WATCH`: missing fact, owner, deadline, review trigger and expiry.

Outputs distinguish `VERIFIED`, `ESTIMATED`, `HYPOTHESIS` and `UNKNOWN`; scores never replace source evidence.

## Score weights

| Dimension | Weight | 0–100 meaning |
|---|---:|---|
| Accessibility | 25 | No practical route to verified decision/procurement pathway |
| Signal Strength | 25 | Generic/stale hypothesis to direct current demand evidence |
| Revenue Potential | 20 | No capture model to credible repeatable Atlas revenue |
| Execution Speed | 15 | Indefinite/high-dependency path to bounded near-term next gates |
| Verification Confidence | 15 | Unresolved/weak evidence to current independent corroboration |
| **Total** | **100** | Weighted score |

`Atlas Opportunity Score = Σ(dimension score × weight) / 100`, rounded only at the end. `UNKNOWN` earns zero. Identity, demand, manufacturing, sanctions/legal, mandatory fit and evidence-integrity gates override scores.

## Accessibility

Score verified access to the relevant buyer, procurement process, sourcing company or authorized commercial channel; stakeholder specificity; channel conflict; trust barrier; and the number of controllable gates to a commercial conversation. A public email or supplier portal alone is weak access evidence.

## Signal Strength

Score demand directness, buyer and requirement specificity, recency, urgency, source independence and expiry. Product-page overlap, generic market growth and undated directory presence do not prove demand.

## Revenue Potential

Score the clarity of payer and revenue event, plausible commission/margin or fee range, repeat purchase, addressable order value, capital/cash exposure and Atlas value contribution. Never invent price or order value; unresolved economics remain `UNKNOWN`.

## Execution Speed

Score evidence-backed time and dependencies from the current state to validation, qualified conversation, quotation and first revenue. Prefer reversible, stock-free paths with named owners. Fast but unverified activity does not earn a high score.

## Verification Confidence

Score entity resolution, source directness, independent corroboration, freshness, completeness and contradiction handling. `PROCEED` requires this dimension ≥70; a polished single-source claim is insufficient.

## Decision

- **PROCEED:** score ≥80; all hard gates pass; Accessibility and Signal Strength ≥65; Revenue Potential ≥60; Execution Speed ≥50; Verification Confidence ≥70; no critical `UNKNOWN`. Authorizes the next named commercial-validation step only.
- **WATCH:** score 50–79, any upstream record is `WATCH`, or one decision-critical gap is plausibly resolvable. Record owner, verification action, deadline and expiry; no outreach is authorized.
- **DROP:** score <50 with no credible reversal path, or a hard gate fails, demand is stale/disproven, access is impractical, revenue capture is structurally absent, or expected value no longer justifies effort.

Stop when one defensible decision and next action exist. A high score never overrides a failed hard gate, and no output authorizes contact or implementation.
