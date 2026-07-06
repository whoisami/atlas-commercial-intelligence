# Manufacturer Scoring Model

## Principles

Scores measure suitability for export business development, not general company quality. No evidence means no points. Every manufacturer record must include a short rationale citing decisive evidence, deductions and unknowns.

## Export Potential Score — 0 to 100

| Criterion | Weight | What earns points |
|---|---:|---|
| Manufacturing evidence | 15 | Verified factory, production processes, machinery or technical capability evidence |
| Export readiness | 15 | Verified exports or credible export-readiness signals beyond translation alone |
| Quality certifications | 10 | Relevant, credible and preferably verifiable quality systems or certifications |
| Product complexity | 10 | Technical processes, tolerances, engineering content and non-commodity capability |
| Repeat order potential | 10 | Components or assemblies likely to support recurring OEM demand |
| Foreign buyer fit | 10 | Capabilities map to identifiable foreign OEM or industrial buyer needs |
| Website credibility | 8 | Consistent identity, current technical content and credible company information |
| Communication readiness | 8 | Foreign-language content and usable public business contact channel |
| Sector attractiveness | 7 | Attractive Sprint 001 subsector with defensible technical demand |
| Commission potential | 7 | Opportunity can plausibly support intermediary-led export development and repeat value |
| **Total** | **100** | |

Score every criterion from 0–100, multiply by its weight and divide the sum by 100. Round only the final result to the nearest whole number.

## Discovery Confidence — 0 to 100

| Confidence factor | Weight |
|---|---:|
| Correct company identity and active website | 25 |
| Direct manufacturing evidence | 30 |
| Source diversity and corroboration | 20 |
| Evidence recency and consistency | 15 |
| Contact and company-presence verification | 10 |
| **Total** | **100** |

Discovery confidence measures evidence reliability, not commercial attractiveness.

## Atlas Score — 0 to 100

`Atlas Score = (Export Potential Score × 0.70) + (Discovery Confidence × 0.30)`

This prevents a commercially appealing but weakly verified company from outranking well-evidenced candidates without making source volume the primary commercial criterion.

## Status rules

### PROCEED

All hard gates pass, `export_potential_score >= 70`, `discovery_confidence >= 70` and `atlas_score >= 70`.

Hard gates:

- real manufacturing evidence;
- export activity or a credible export-readiness signal;
- clear fit with an allowed product capability;
- enough public data for later outreach preparation;
- at least one usable public business contact channel;
- source URLs supporting the decision.

### WAIT

The company appears relevant but has a missing or contradictory decision-critical fact, or any principal score is 50–69. The record must name the verification action that could move it to `PROCEED` or `DROP`.

### DROP

Any principal score is below 50, a hard disqualifier is verified, the entity is not a real manufacturer, capability fit is absent, sources are unverifiable, or material trust risk remains.

## Score explanation format

Use one concise rationale:

`Positive evidence: [facts and sources]. Deductions: [missing or weak factors]. Unknowns: [decision-relevant gaps]. Status reason: [why the gates pass or fail].`
