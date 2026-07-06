# SPEC_003 — Matching Engine

## Purpose

Define how Atlas evaluates a proposed match among a verified foreign buyer need, a discovered Turkish manufacturer, and—when applicable—a sourcing company or commercial intermediary. The specification is Turkey → World only and ranks commercial fit after demand and supply evidence exist. It discovers nothing, implements nothing, and authorizes no outreach, CRM activity, quotation, order or commitment.

## Inputs

| Input | Required content | Evidence rule |
|---|---|---|
| Demand record | Buyer ID, country, product/capability need, specification, quantity/timing when public, access route, status | Accepted demand assessment; `PROCEED` preferred, `WATCH` cannot yield final `PROCEED` |
| Manufacturer record | Manufacturer ID, capability, materials, capacity evidence, certifications, export readiness, status | Accepted discovery and need assessment with traceable sources |
| Sourcing-company record | Entity ID, mandate, category/geography coverage, buyer/supplier access, conflicts, compensation route | Required only when an intermediary is part of the proposed match; claims must be verified |
| Commercial-model hypothesis | Representation, commission, sourcing fee, back-to-back or hybrid; payer, revenue event, responsibilities | Assumptions labeled; model must be lawful and understandable |
| Risk and contradiction record | Sanctions/legal flags, channel conflict, exclusivity, quality/logistics gaps, stale evidence | Material unresolved contradiction blocks `PROCEED` |

Resolve all entities and use only public or authorized evidence. Unsupported facts are `UNKNOWN` and earn no points.

## Outputs

- Match card: buyer, manufacturer, optional sourcing company, demand context, evidence cutoff and source records.
- Three fit assessments: manufacturer-buyer, sourcing-company and commercial-model fit.
- Weighted Match Score, hard-gate results, constraints, contradictions and evidence limitations.
- Decision: `PROCEED`, `WATCH` or `DROP`, with exact authorized next validation action.
- Expiry or review trigger for demand, pricing, capacity and access evidence.

Outputs distinguish `VERIFIED`, `ESTIMATED`, `HYPOTHESIS` and `UNKNOWN`; they do not authorize external contact.

## Manufacturer-buyer fit

Evaluate product/process and material compatibility, technical specifications, certification requirements, capacity and timing, quality evidence, export/logistics readiness, order economics and buyer qualification requirements. Buyer need and manufacturer capability must refer to the same use case; generic portfolio overlap is insufficient. Identity, real manufacturing, verified demand, legal/sanctions eligibility and mandatory technical requirements are hard gates.

## Sourcing-company fit

When a sourcing company or intermediary is proposed, evaluate its verified mandate, category and geography relevance, access to the buyer or procurement route, ability to qualify/manage suppliers, trust evidence, channel conflict and compensation compatibility. A website claim, contact list or broad network statement does not prove access. If no intermediary is required, mark this fit `NOT APPLICABLE` and redistribute no points; use the direct-match scoring rule below.

## Commercial model fit

Evaluate who creates value, who pays, what event earns revenue, responsibility for quotation/order/payment/quality/logistics, margin or fee plausibility, working-capital exposure, currency and liability risk, repeatability and time to first revenue. A model with no identifiable payer, revenue event or accessible next step cannot `PROCEED`.

## Scoring

| Factor | With intermediary | Direct match | 0–100 evidence meaning |
|---|---:|---:|---|
| Technical and specification fit | 25 | 30 | Unknown/mismatch to verified complete fit |
| Capacity, quality and delivery fit | 15 | 20 | Unsupported to verified readiness for the need |
| Buyer need, timing and access | 20 | 20 | Generic/stale to current accessible demand |
| Sourcing-company fit | 15 | N/A | No mandate/access to verified relevant intermediary |
| Commercial model fit | 15 | 20 | No payer/revenue event to viable repeatable model |
| First-revenue probability | 10 | 10 | Remote/undefined to credible near-term path |
| **Total** | **100** | **100** | Weighted Match Score |

Use the applicable weight column: `Match Score = Σ(score × weight) / 100`, rounded only at the end. `UNKNOWN` scores zero. Report Evidence Quality separately; `PROCEED` requires ≥70. Hard gates override scores, and upstream `WATCH` status caps the match at `WATCH`.

## Decision

- **PROCEED:** Match Score ≥75, Evidence Quality ≥70, all hard gates pass, Technical and Specification Fit ≥70, Buyer Need/Timing/Access ≥60, Commercial Model Fit ≥60, applicable Sourcing-Company Fit ≥60, and no critical `UNKNOWN`. Authorizes deeper joint commercial validation only.
- **WATCH:** Match Score 50–74, an upstream record is `WATCH`, or one decision-critical gap is plausibly resolvable. Record missing fact, owner, verification action and expiry; no outreach is authorized.
- **DROP:** Match Score <50 with no credible reversal path, or a hard gate fails, demand/capability fit is disproven, intermediary access is false, mandatory requirements conflict, no viable commercial model exists, or expected value does not justify further work.

Stop when one decision and next action are defensible. Never use a high score to override identity, demand, manufacturing, sanctions/legal, mandatory specification, authorization or evidence-integrity failure.
