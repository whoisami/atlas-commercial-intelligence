# Opportunity Scoring

## Operating contract

This procedure implements [SPEC_004](../specs/04_opportunity_scoring.md). It scores one verified, post-match Turkey → World opportunity by evidence-backed probability of first revenue.

It consumes accepted upstream records and does not discover demand, manufacturers, buyers or intermediaries; create CRM activity; draft/send outreach; quote, order or authorize a commitment.

## Entry gate

Open an [Opportunity Scorecard](opportunity_scorecard.md) only with:

- accepted demand assessment with signal ID, buyer/segment, need, timing, access route and status;
- accepted manufacturer assessment with Turkish manufacturer ID, capability, export need/readiness and status;
- accepted match assessment with technical, access and commercial-model fit and status;
- revenue hypothesis naming model, payer, revenue event, value range or `UNKNOWN`, and repeatability;
- execution plan naming next gates, owners, dependencies, elapsed-time assumptions and capital exposure;
- evidence register with sources, dates, states, contradictions and expiries.

An upstream `WATCH` caps the result at `WATCH`; a decisive upstream `DROP` prevents scoring. Deduplicate by stable demand, manufacturer and match IDs and apply the earliest evidence expiry.

## Evidence states and award caps

Every subfactor has a source reference, evidence state and rationale:

| State | Maximum award |
|---|---:|
| VERIFIED | 100% of subfactor maximum |
| ESTIMATED | 50% of subfactor maximum |
| HYPOTHESIS | 25% of subfactor maximum |
| UNKNOWN | 0 |

The cap is not an automatic award. Weak evidence may score lower. Same-owner repetition does not improve confidence. Keep subfactor points unrounded.

## Workflow

1. Lock stable IDs, upstream statuses, owner, cutoff and earliest expiry.
2. Confirm all entities and the same buyer-manufacturer use case across records.
3. Apply hard gates before scoring.
4. Score each listed subfactor from evidence; `UNKNOWN` earns zero.
5. Sum subfactors into five 0–100 dimensions.
6. Calculate the weighted Atlas Opportunity Score and apply dimension floors.
7. Record one `PROCEED`, `WATCH` or `DROP` decision and exact next action.
8. Stop when the decision is defensible; never research to force a threshold.

## Hard gates

| Gate | PASS | WATCH | FAIL / decision |
|---|---|---|---|
| Upstream records | Required assessments accepted/current | One assessment `WATCH` or recoverably stale | Decisive upstream `DROP` → stop |
| Entity identity | Buyer, manufacturer and applicable intermediary resolved | Resolvable ambiguity | False/unresolvable identity → `DROP` |
| Verified demand | Current relevant demand evidenced | One demand/timing fact unresolved | Stale/disproven demand → `DROP` |
| Real manufacturing | Relevant Turkish manufacturing verified | Decisive capability fact unresolved | Non-manufacturer/false claim → `DROP` |
| Match viability | Mandatory fit and applicable mandate pass | One mandatory fact unresolved | Confirmed mandatory mismatch/false mandate → `DROP` |
| Legal/sanctions eligibility | No known disqualifying conflict | Authoritative check required by signal | Confirmed prohibition → `DROP` |
| Evidence integrity | Sources traceable/correctly attributed | Material contradiction under review | Invented/misattributed evidence → `DROP` |

All gates PASS for `PROCEED`. Scores cannot override a failed gate.

## Accessibility — 0 to 100

| Subfactor | Maximum | Evidence focus |
|---|---:|---|
| Verified procurement or authorized channel | 30 | Buyer pathway, mandate, tender, portal or relevant intermediary access |
| Stakeholder and decision-role specificity | 20 | Identified function/role and decision relevance; no private-data inference |
| Channel conflict and trust barriers | 15 | Manageable incumbent, exclusivity, credibility and qualification barriers |
| Controllability of next commercial gates | 20 | Named, feasible steps from validation to qualified conversation |
| Access evidence quality and recency | 15 | Direct, current, independently supported route evidence |
| **Accessibility** | **100** | Sum of awarded points |

A public email or supplier portal alone is weak access evidence and never proves buyer intent.

## Signal Strength — 0 to 100

| Subfactor | Maximum | Evidence focus |
|---|---:|---|
| Demand directness | 30 | Explicit procurement need versus generic market/product interest |
| Buyer and requirement specificity | 20 | Resolved entity/segment, category, use case and mandatory requirements |
| Recency and remaining action window | 20 | Current dated signal and justified expiry |
| Commercial urgency | 15 | Evidence-backed timing, disruption, project or sourcing event |
| Independent corroboration | 15 | Consistent evidence from independent source classes |
| **Signal Strength** | **100** | Sum of awarded points |

Generic growth, undated directories and product-page overlap are not demand signals.

## Revenue Potential — 0 to 100

| Subfactor | Maximum | Evidence focus |
|---|---:|---|
| Payer and revenue-event clarity | 20 | Identifiable payer, compensation basis and earning event |
| Economics and margin/fee plausibility | 20 | Comparable price/value/cost inputs or explicit `UNKNOWN` |
| Repeatability and account value | 20 | Recurring requirement or sufficient evidence-backed one-off value |
| Atlas value contribution | 15 | Specific access, qualification, representation or transaction value |
| Capital, cash-flow and liability fit | 15 | Acceptable working capital, payment, quality, logistics and legal risk |
| Demand value evidence | 10 | Order/project scope, volume or value only where supported |
| **Revenue Potential** | **100** | Sum of awarded points |

Never invent prices, volumes, commissions or order values.

## Execution Speed — 0 to 100

| Subfactor | Maximum | Evidence focus |
|---|---:|---|
| Next-gate ownership and readiness | 20 | Named owner, action, completion evidence and due date |
| Time to qualified commercial conversation | 20 | Evidence-backed route and elapsed-time range |
| Qualification and quotation path | 20 | Known requirements, dependencies and decision sequence |
| Time to first revenue | 25 | Bounded path from current state to revenue event |
| Dependency, capital and reversibility fit | 15 | Few external blockers, stock-free/reversible path where practical |
| **Execution Speed** | **100** | Sum of awarded points |

Fast but unsupported activity does not score highly; an `UNKNOWN` timeline earns zero.

## Verification Confidence — 0 to 100

| Subfactor | Maximum | Evidence focus |
|---|---:|---|
| Entity and upstream record integrity | 20 | Stable IDs and consistent accepted assessments |
| Directness of decisive evidence | 25 | First-party/authoritative evidence for demand, capability and access |
| Independent corroboration | 20 | Independent source classes support decisive claims |
| Freshness and expiry control | 15 | Current evidence and earliest-expiry review |
| Completeness of decision-critical facts | 10 | No hidden mandatory fields or unsupported substitutions |
| Contradiction and limitation handling | 10 | Adverse evidence and alternative explanations resolved/disclosed |
| **Verification Confidence** | **100** | Sum of awarded points |

A polished single-source claim is insufficient. `PROCEED` requires Verification Confidence ≥70.

## Atlas Opportunity Score

| Dimension | Weight | `PROCEED` floor |
|---|---:|---:|
| Accessibility | 25 | 65 |
| Signal Strength | 25 | 65 |
| Revenue Potential | 20 | 60 |
| Execution Speed | 15 | 50 |
| Verification Confidence | 15 | 70 |
| **Total** | **100** |  |

`Atlas Opportunity Score = Σ(dimension score × weight) / 100`

Round only the final score. Do not round dimensions or contributions. This is the final post-match score; never copy or convert the upstream seven-factor discovery-screening score.

## Decision

### PROCEED

Atlas Opportunity Score ≥80; every hard gate PASS; every dimension floor passes; no critical `UNKNOWN`; and one commercial-validation action with owner and due date is named.

This authorizes only that next validation action, never contact.

### WATCH

Use for score 50–79; any upstream `WATCH`; a floor missed because evidence is incomplete; or one realistically resolvable critical gap. Record missing fact, impact, smallest verification action, owner, due date and expiry. A score below 50 remains `WATCH` only when one bounded fact could plausibly reverse the decision.

### DROP

Use for score below 50 without a credible reversal path; failed hard gate; stale/disproven demand; impractical access; structurally absent revenue capture; unacceptable risk; or verification effort exceeding plausible value. Re-entry requires new dated evidence that changes the failed condition.

## Validation and stop rules

- Every dimension equals its subfactor sum and remains 0–100.
- Every point has an evidence state, source and rationale; award caps are respected.
- Five final weights total 100; only the final score is rounded.
- Hard gates, upstream status caps and dimension floors override the aggregate.
- Missing data stays `UNKNOWN`; no price, volume, contact, intent or timeline is invented.
- Stop after one decision and next action; no output authorizes outreach or commitment.
