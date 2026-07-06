# Commercial Signal Scoring Model v2

> **Scope:** This is the upstream discovery-screening model. It must not be used as the final post-match Atlas Opportunity Score. After accepted demand, manufacturer and match assessments exist, use [Opportunity Scoring](opportunity_scoring.md). Preserve historical v2 values; do not translate them into the five-dimension score.

## Evidence discipline

Scores rank evidence-backed commercial probability. `UNKNOWN` earns zero until verified. `ESTIMATED` inputs are allowed only when method and limitation are stated. No score can turn a one-source claim into a verified fact.

## Component scores — 0 to 100

### Manufacturing Score

Measures direct evidence of real production, relevant processes, machinery/factory, technical complexity, quality control and repeatable OEM capability.

### Export Readiness

Measures verified exports, export documentation, quality requirements, language/logistics capability, international references and readiness to serve foreign accounts. English content alone is insufficient.

### Commercial Accessibility Score

Measures the probability Atlas can establish a commercial relationship within 90 days.

| Factor | Weight |
|---|---:|
| Company size fit for external market development | 15 |
| Export department maturity without being closed to partners | 15 |
| Existing distributor/channel openness | 15 |
| Decision-maker or category-owner accessibility | 15 |
| Website/contact-channel usability | 10 |
| Public openness: portal, partner notice or supplier registration | 15 |
| Growth/capacity signal | 10 |
| Explicit partnership signal | 5 |
| **Total** | **100** |

Large mature networks may score lower when they reduce Atlas access. Weak websites reduce only the digital-contact factor; verified industrial access can compensate.

### Commercial Signal Score

Measures whether now is the right time to approach.

| Signal dimension | Weight |
|---|---:|
| Signal strength and commercial relevance | 30 |
| Recency against the defined freshness window | 20 |
| Independent corroboration | 15 |
| Evidence of investment/capacity/new line | 15 |
| Evidence of new market, export hiring, fair or partnership search | 15 |
| Actionability within 90 days | 5 |
| **Total** | **100** |

No current signal means `0`, not a guessed neutral score. A supplier portal without a dated need is primarily Accessibility evidence and only a weak Signal input.

### Revenue Potential

Measures repeat-order economics, likely project/order scale, commission or margin fit and long-term account value. When price, volume or commercial terms are absent, score conservatively and label the estimate.

### Execution Speed

Measures whether Atlas can complete verification, obtain a mandate, reach the relevant party and secure a commercial conversation within 90 days.

### Verification Score

Measures evidence confidence across independent source classes.

| Verification factor | Weight |
|---|---:|
| Entity identity and legal/operating consistency | 15 |
| Factory or relevant operating-address verification | 15 |
| Public business phone/contact verification | 10 |
| Manufacturing or buyer-function evidence | 20 |
| Institutional evidence: chamber/OSB/export/government/fair | 15 |
| Certification evidence and scope | 10 |
| LinkedIn/team/current-activity corroboration | 5 |
| Source independence, recency and contradiction resolution | 10 |
| **Total** | **100** |

Source absence earns no points. A website can contribute to several supported facts but remains one source class.

## Atlas Opportunity Score

| Component | Weight |
|---|---:|
| Manufacturing Score | 20 |
| Export Readiness | 15 |
| Commercial Accessibility | 15 |
| Commercial Signals | 15 |
| Revenue Potential | 15 |
| Execution Speed | 10 |
| Verification Confidence | 10 |
| **Total** | **100** |

`Atlas Opportunity Score = Σ(component score × component weight) / 100`

Round only the final score. Every component requires an evidence state and rationale.

## Decision rules

### PROCEED

- Atlas Opportunity Score at least 75;
- Verification Score at least 70;
- Commercial Accessibility at least 60;
- Commercial Signal Score at least 50;
- real manufacturing evidence for a named manufacturer;
- no unresolved hard risk or channel conflict;
- one executable next action within 90 days.

### WAIT

Atlas Opportunity Score 50–74, a threshold component is missing, the signal is uncorroborated/stale, or the entity/opportunity is commercially plausible but requires a named verification action.

### DROP

Atlas Opportunity Score below 50; false/stale signal; disproven operating identity; no relevant manufacturing/buyer fit; inaccessible commercial route; unacceptable conflict or risk.

## Existing-data migration rule

Legacy v1 scores are not silently reinterpreted. Until every v2 component is recalculated from multi-source evidence, new fields are `UNKNOWN` and the opportunity cannot be promoted by the v2 engine.
