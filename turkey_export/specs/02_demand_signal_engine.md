# SPEC_002 — Demand Signal Engine

## Purpose

Define how Atlas evaluates evidence of foreign industrial demand before matching Turkish supply. The specification converts a dated signal into `PROCEED`, `WATCH` or `DROP` for further commercial validation. It applies only to Turkey → World, implements nothing, and authorizes no outreach, CRM activity, purchase or commercial commitment.

## Inputs

| Input | Required content | Evidence rule |
|---|---|---|
| Signal source | URL or stable record ID, publisher, publication date, access date | Public or authorized; search snippets alone are insufficient |
| Foreign demand context | Buyer/entity, country, product or capability, need, timing | Buyer and need must be explicit or labeled `UNKNOWN` |
| Access context | Procurement route, supplier portal, tender, named function or public channel | A contact route does not prove buying intent |
| Commercial context | Likely order pattern, urgency, Turkish supply relevance, first-revenue path | Estimates labeled; unsupported values are `UNKNOWN` |
| Corroboration | Independent source and contradiction check | Same-owner pages count as one source class |

Reject invented, private, misattributed, duplicate or materially stale inputs. Resolve entity identity before scoring.

## Outputs

- Signal record: ID, type, entity, country, product/capability, dates, evidence state and sources.
- Commercial interpretation: verified need, timing, accessibility, Turkish-supply relevance and alternative explanation.
- Scores: six factor scores, weighted Demand Signal Score and evidence limitations.
- Decision: `PROCEED`, `WATCH` or `DROP`, with rationale and exact next verification action.
- Expiry: review date or event that makes the signal stale.

Outputs distinguish `VERIFIED`, `ESTIMATED`, `HYPOTHESIS` and `UNKNOWN`. They do not discover manufacturers or authorize contact.

## Signal types

- Published RFQ, tender, procurement notice or supplier-registration opening.
- Buyer announcement of capacity expansion, new plant, production line or product launch.
- Public sourcing, localization, dual-sourcing or supply-chain diversification initiative.
- Dated shortage, lead-time, quality or incumbent-supplier disruption with buyer relevance.
- Procurement or supplier-quality hiring linked to a defined category or expansion.
- New regulatory, certification or localization requirement creating a specific sourcing need.
- Trade-fair, association or market activity only when tied to a named buyer need or access event.

Generic market growth, website product lists, undated directories and public email addresses are not demand signals by themselves.

## Scoring

| Factor | Weight | 0–100 meaning |
|---|---:|---|
| Demand directness | 25 | Rumor/unknown to explicit buyer procurement need |
| Recency and timing | 20 | Stale/unknown to current actionable window |
| Buyer and need specificity | 15 | Generic market to resolved buyer, category and requirement |
| Commercial accessibility | 15 | No route to verified procurement pathway |
| Turkish supply and revenue relevance | 15 | No plausible fit to credible route to Atlas first revenue |
| Independent corroboration | 10 | Single weak claim to consistent independent evidence |
| **Total** | **100** | Weighted score |

`Demand Signal Score = Σ(score × weight) / 100`, rounded only at the end. `UNKNOWN` earns zero. Identity, evidence integrity, legal/sanctions risk and disproven demand are hard gates that scores cannot override.

## Decision

- **PROCEED:** score ≥75; resolved foreign entity; demand and timing directly evidenced; at least two independent source classes; commercial access and Turkish-supply relevance are plausible; no failed hard gate. Authorizes deeper demand and buyer validation only.
- **WATCH:** score 50–74, or a potentially strong signal has one resolvable critical gap. Record the missing fact, owner, verification action and expiry; no outreach is authorized.
- **DROP:** score <50, demand is disproven or stale, entity is unresolved beyond practical verification, access is commercially impractical, a hard gate fails, or expected value does not justify more work.

## Acceptance criteria

- [ ] Only Turkey → World foreign-demand signals are evaluated.
- [ ] Demand is evaluated before Turkish manufacturer selection.
- [ ] Every material claim has a source and date; missing facts are `UNKNOWN`.
- [ ] All seven signal types and explicit non-signals are handled.
- [ ] Six scoring weights total 100 and hard gates override scores.
- [ ] `PROCEED`, `WATCH` and `DROP` have testable thresholds and authorized actions.
- [ ] Commercial accessibility and first-revenue relevance affect the decision.
- [ ] Stale, duplicate, contradictory and same-owner evidence is controlled.
- [ ] The output does not discover manufacturers or authorize outreach.
- [ ] No engine, CRM, email automation or executable behavior is implemented.
