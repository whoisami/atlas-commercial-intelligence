# Demand Signal Engine

## Operating contract

This procedure implements [SPEC_002](../specs/02_demand_signal_engine.md). It evaluates whether a dated foreign industrial signal is strong enough to justify deeper demand and buyer validation before Turkish supply is selected.

It does not discover manufacturers, select Turkish supply, enrich contacts, create CRM activity, draft/send outreach, or authorize a purchase or commitment.

## Entry record

Open a [Demand Signal Assessment](demand_signal_assessment.md) for one signal and one resolved or explicitly unresolved foreign entity. Record:

- signal URL or stable record ID, publisher, publication/event date and access date;
- foreign entity, country, product/capability, apparent need and timing;
- public procurement/access route or `UNKNOWN`;
- commercial context, Turkish-supply relevance and first-revenue hypothesis;
- corroborating source, source classes and contradictions;
- analyst, evidence cutoff and review/expiry date.

Search snippets, AI summaries, undated directories, product pages, generic market growth and public email addresses are not sufficient final evidence.

## Signal taxonomy

Use exactly one primary type and optional secondary types:

1. `PROCUREMENT_OPENING` — published RFQ, tender, procurement notice or supplier-registration opening.
2. `BUYER_EXPANSION` — buyer announcement of capacity expansion, new plant, production line or product launch.
3. `SOURCING_CHANGE` — public localization, dual-sourcing or supply-chain diversification initiative.
4. `SUPPLY_DISRUPTION` — dated shortage, lead-time, quality or incumbent-supplier disruption with buyer relevance.
5. `PROCUREMENT_HIRING` — procurement or supplier-quality hiring tied to a defined category or expansion.
6. `REQUIREMENT_CHANGE` — new regulatory, certification or localization requirement creating a specific sourcing need.
7. `MARKET_ACCESS_EVENT` — trade-fair, association or market activity tied to a named buyer need or access event.

An event that cannot meet a taxonomy definition remains `UNKNOWN`; do not force classification.

## Evidence states and source independence

- **VERIFIED:** directly supported by current first-party, authoritative or accepted Atlas evidence.
- **ESTIMATED:** derived from disclosed evidence and assumptions.
- **HYPOTHESIS:** plausible interpretation requiring a named test.
- **UNKNOWN:** absent, stale beyond usefulness, inaccessible or materially contradictory.

Record source ownership. Multiple pages controlled by one entity count as one source class; copied directories are not independent. `PROCEED` requires at least two independent source classes and one source directly evidencing demand and timing.

## Workflow

1. **Capture.** Lock the signal, entity candidate, country, need, event date and source ownership.
2. **Resolve entity.** Match legal/trading name, domain, location and institutional identifiers; separate subsidiaries and namesakes.
3. **Classify.** Apply the signal taxonomy; distinguish access evidence from buying intent.
4. **Validate freshness.** Set a justified review/expiry event. Do not refresh a stale signal merely because its page remains online.
5. **Corroborate.** Seek an independent source and record contradictory evidence.
6. **Interpret.** State verified need, timing, access, Turkish-supply relevance, revenue path and at least one alternative explanation.
7. **Apply hard gates.** Record PASS, WATCH or FAIL before scoring.
8. **Score.** Award only evidence-backed points across six factors; `UNKNOWN` earns zero.
9. **Decide.** Apply thresholds without discretionary override and record one next action.
10. **Stop.** End when a decision is defensible or the next verification action is clear.

## Hard gates

| Gate | PASS | WATCH | FAIL / decision |
|---|---|---|---|
| Foreign entity | Correct entity resolved | Resolvable ambiguity | False/unresolvable entity → `DROP` |
| Demand evidence | Need and timing directly evidenced | Plausible but decisive fact missing | Demand disproven → `DROP` |
| Freshness | Inside justified action window | Expiry unclear but verifiable | Materially stale → `DROP` |
| Evidence integrity | Correct attribution and traceable source | Contradiction under review | Invented/fabricated/misattributed → `DROP` |
| Legal/critical risk | No known disqualifying signal | Authoritative check required by evidence | Confirmed sanctions/legal prohibition → `DROP` |
| Commercial relevance | Plausible Turkish-supply and Atlas revenue path | Fit/access needs one bounded check | Structurally irrelevant/inaccessible → `DROP` |

All gates PASS for `PROCEED`. Numeric scores cannot override a failed gate.

## Demand Signal Score — 0 to 100

| Factor | Weight | Evidence focus |
|---|---:|---|
| Demand directness | 25 | Explicit procurement need versus rumor or generic interest |
| Recency and timing | 20 | Current actionable window and credible urgency |
| Buyer and need specificity | 15 | Resolved buyer/entity, category and requirement |
| Commercial accessibility | 15 | Verified procurement pathway, mandate or relevant public route |
| Turkish supply and revenue relevance | 15 | Plausible capability fit and route to Atlas first revenue |
| Independent corroboration | 10 | Consistent evidence from independent source classes |
| **Total** | **100** |  |

Use common anchors: 0 = disproven/absent/entirely `UNKNOWN`; 25 = weak indirect signal; 50 = plausible with material gaps; 75 = strong current evidence; 100 = explicit, current, independently corroborated evidence. Intermediate scores need written rationale.

`Demand Signal Score = Σ(factor score × weight) / 100`

Round only the final score. Access routes do not prove intent. Turkish supply relevance must remain a capability hypothesis at this stage; do not name or discover a manufacturer.

## Decision

### PROCEED

Demand Signal Score ≥75; all hard gates PASS; foreign entity is resolved; demand and timing are directly evidenced; at least two independent source classes exist; commercial access and Turkish-supply/revenue relevance are plausible; and no critical `UNKNOWN` remains.

Authorizes only deeper demand and buyer validation. It does not authorize manufacturer discovery or contact.

### WATCH

Use for score 50–74 or one realistically resolvable critical gap. Record the missing fact, decision impact, smallest verification action, owner, due date and expiry. No outreach is authorized. Reassess at expiry rather than carrying the signal indefinitely.

### DROP

Use for score below 50 without a credible reversal path; disproven or stale demand; false/unresolvable entity; impractical access; failed hard gate; or verification cost exceeding plausible value. Record the decisive evidence. Re-entry requires a new dated signal that changes the failed condition.

## Quality and stop rules

- Do not treat a supplier portal, job post, fair appearance or product page alone as buyer demand.
- Do not create manufacturer candidates during demand evaluation.
- Do not infer order value, urgency, buyer intent or procurement authority without evidence.
- Record alternative explanations and adverse evidence.
- Stop when one decision and next action are defensible; do not collect sources to force `PROCEED`.
