# SPEC_001 — Export Need Analyzer

## Specification control

| Field | Value |
|---|---|
| Specification ID | SPEC_001 |
| Version | 0.1 |
| Status | DRAFT |
| Owner | Turkey Export Commercial Intelligence |
| Created | 2026-07-06 |
| Last updated | 2026-07-06 |
| Evidence cutoff | Set at analysis time |
| Related opportunity | Discovered Turkish manufacturer with a defined foreign-demand context |
| Supersedes | NONE |

## Purpose

### Commercial problem

Atlas needs to distinguish Turkish manufacturers that can export independently from manufacturers that are technically credible but likely to benefit from external business development support. Manufacturer quality alone does not establish a partnership opportunity. Atlas must find evidence of both export capability and a commercially addressable need.

The Export Need Analyzer evaluates an already-discovered Turkish manufacturer. It does not discover manufacturers, buyers, contacts or demand signals.

### Decision supported

Determine whether Atlas should advance a discovered Turkish manufacturer for deeper partnership validation based on:

- credible manufacturing capability;
- readiness to serve foreign customers;
- evidence of growth ambition or underdeveloped export access;
- a specific external business-development gap;
- evidence that the manufacturer may work with an external partner;
- a plausible, accessible route to Atlas revenue.

The commercial user is the Turkey Export opportunity owner. The output supports `PROCEED`, `WATCH` or `DROP`; it does not authorize contact.

### Expected commercial value

The analyzer should reduce time spent on manufacturers that are too weak to export, have no evidence of needing support, are inaccessible to an external partner or offer no plausible Atlas revenue path. It should prioritize manufacturers where Atlas can credibly shorten the path to a qualified foreign opportunity and first revenue.

### In scope

- Turkish manufacturers already discovered and identity-resolved by an upstream process.
- Manufacturer-level evidence of production, export readiness, growth need and business-development gaps.
- Public evidence of partnership openness and commercial accessibility.
- Opportunity-specific Atlas revenue potential under a disclosed commercial model.
- Evidence quality, contradictions, unknowns and next verification actions.

### Out of scope

- Manufacturer discovery or lead-list generation.
- Foreign-buyer discovery.
- Foreign-demand creation or validation.
- Contact enrichment, CRM functionality or pipeline automation.
- Email drafting, sending, sequencing or outreach automation.
- Financial, legal, sanctions or full manufacturer due diligence.
- Automatic outreach, quotation, purchasing, representation or exclusivity.
- Foreign → Turkey changes.
- Executable engine implementation.

## Inputs

| Input | Purpose | Required fields | Accepted evidence | Freshness | Required / Optional | Unknown handling |
|---|---|---|---|---|---|---|
| Manufacturer identity record | Confirm the entity being evaluated | Legal or trading name, website, Turkey location, stable record ID | Official website plus an independent institutional or corporate source | Verify at analysis date | Required | Unresolved identity triggers `WATCH` or `DROP`; do not score |
| Discovery record | Prove the manufacturer was discovered upstream | Discovery source, discovery date, rationale, source URLs | Accepted Turkey Export discovery record | Normally within 12 months | Required | Missing record triggers `WATCH`; analyzer must not perform discovery |
| Foreign-demand context | Keep analysis demand-first | Target product/capability, country or buyer segment, demand evidence, source, date | Accepted demand/opportunity record or directly cited credible evidence | Appropriate to demand type; stale evidence must be flagged | Required | Missing demand context triggers `WATCH`; no supply-first `PROCEED` |
| Manufacturing evidence | Assess real production strength | Products, processes, facility/factory evidence, equipment or capacity indicators, quality evidence | First-party technical pages/catalogues plus independent industrial, certification or institutional corroboration | Current or reviewed for continued validity | Required | `UNKNOWN` receives no points; inability to verify manufacturing triggers `DROP` |
| Export-readiness evidence | Assess ability to serve foreign customers | Export activity, foreign markets/customers when public, certifications, languages, logistics or documentation capability | Official export pages, dated trade-fair/export records, certification registries, public customs/trade evidence where lawful | Prefer within 24 months; certification validity checked | Required | Missing decisive evidence caps decision at `WATCH` |
| Growth-need evidence | Assess evidence of a current growth objective or underused export opportunity | Expansion, investment, hiring, new line/product, target markets, capacity utilization signal, export gap | Dated first-party announcements, public job posts, institutional news, trade-fair participation, accepted interview notes | Normally within 24 months | Required for `PROCEED` | Absence is `UNKNOWN`, not proof of no need |
| Business-development evidence | Identify a specific gap Atlas could address | Export-sales coverage, target-market access, lead-generation gap, distributor/partner search, buyer-access challenge | Public organization/team evidence, job posts, partnership calls, accepted meeting/interview records | Normally within 18 months | Required for `PROCEED` | Generic inference from company size is insufficient; cap at `WATCH` |
| Partnership-openness evidence | Assess willingness and route to work with an external partner | Partner/distributor/agent language, prior channel model, public international-sales route, authorized conversation evidence | Official partner pages, announcements, public role descriptions, accepted direct records | Normally within 24 months | Required for `PROCEED` | Public contact data alone does not prove openness; score conservatively |
| Atlas commercial-model hypothesis | Test revenue feasibility | Proposed model, value event, payer, compensation basis, expected path to first revenue, key assumptions | Accepted opportunity record and evidence-backed model assumptions | Current opportunity | Required | Missing or purely speculative model triggers `WATCH` |
| Contradiction and risk evidence | Prevent false positives | Conflicting identity, capacity, export, channel, reputation or accessibility evidence | Same evidence classes used for positive claims, including authoritative risk sources | Verify at analysis date | Required | Unresolved material contradiction prevents `PROCEED` |

### Input validation

1. Match name, domain, city, factory location and institutional identifiers to the same operating entity.
2. Confirm the entity is a Turkish manufacturer, not a distributor, trader, broker, marketplace or service-only business.
3. Confirm the upstream discovery record and demand context exist; do not discover substitutes.
4. Separate company-controlled claims from independent corroboration. Repeated pages controlled by one entity count as one source class.
5. Verify certification scope, holder and validity before using it.
6. Record source URL or repository record, publication date when available, access date and evidence state for every scored claim.
7. Flag stale, duplicated or contradictory inputs. Never silently select the more favorable claim.
8. Use only public or authorized evidence. Do not scrape private data or infer private financial distress.

## Outputs

| Output | Commercial user | Required fields | Evidence traceability | Authorized next action |
|---|---|---|---|---|
| Export Need Assessment | Turkey Export opportunity owner | Manufacturer ID, demand context, evidence cutoff, six dimension scores, weighted score, evidence quality, hard-gate results, decision, rationale, unknowns | Source or repository record for every decisive claim | Apply the decision logic below |
| Evidence Register | Analyst and reviewer | Claim, evidence state, source, date, access date, contradiction, affected score | Direct URL or stable record ID | Verify or audit the assessment |
| Need Hypothesis | Commercial reviewer | Specific business-development need, observed signal, alternative explanation, Atlas capability match | Linked evidence and confidence | Validate the hypothesis; no contact authorized |
| Verification Plan | Opportunity owner | Missing fact, decision impact, verification action, owner, due date, review trigger | Linked to `WATCH` reason | Resolve only decision-critical gaps |
| Commercial Model Summary | Commercial reviewer | Proposed model, payer, revenue event, accessibility, time-to-first-revenue range or `UNKNOWN`, assumptions | Evidence-linked inputs; estimates labeled | Determine whether deeper commercial validation is justified |

### Output states

- **VERIFIED:** directly supported by current first-party, authoritative or accepted Atlas evidence.
- **ESTIMATED:** calculated or inferred from disclosed evidence and assumptions; never presented as fact.
- **HYPOTHESIS:** plausible explanation requiring a named verification action.
- **UNKNOWN:** evidence is absent, inaccessible, stale beyond usefulness or contradictory.

Every output must state evidence quality, limitations and the action authorized by the decision.

### Non-authorization statement

The assessment does not authorize manufacturer discovery, contact enrichment, CRM entry, email or LinkedIn activity, outreach automation, a quotation, a purchase, representation, exclusivity, an agreement or any external commitment.

## Required evidence

### Minimum evidence packet

Before a scored decision, the assessment must contain:

- resolved manufacturer identity;
- at least one first-party source proving relevant products or processes;
- at least one independent source corroborating manufacturing, certification or industrial existence;
- a dated upstream discovery record;
- an evidence-backed foreign-demand context;
- evidence addressing export readiness;
- evidence addressing growth need and business-development need;
- evidence addressing partnership openness or an explicit `UNKNOWN`;
- a stated Atlas commercial-model hypothesis;
- a contradiction check.

### Evidence quality score

Score evidence quality separately from commercial dimensions:

| Component | Points |
|---|---:|
| Entity identity and source ownership resolved | 20 |
| Manufacturing claims directly evidenced and independently corroborated | 25 |
| Export-readiness evidence current and verifiable | 15 |
| Growth and business-development need supported by dated evidence | 20 |
| Partnership and commercial-model evidence traceable | 10 |
| Contradictions, freshness and limitations explicitly handled | 10 |
| **Total** | **100** |

Unavailable points score zero. `PROCEED` requires Evidence Quality of at least 70. A high commercial score cannot compensate for weak evidence.

## Rules

### Governing rules

- Comply with [`ATLAS_RULES.md`](../ATLAS_RULES.md).
- Turkey → World only; Foreign → Turkey remains untouched.
- Evaluate only a manufacturer supplied by an upstream discovery record.
- Demand first; the relevant foreign-demand context must exist before `PROCEED`.
- Supply follows demand; score the manufacturer's fit to that context, not generic export attractiveness.
- No invented data. Unsupported fields are `UNKNOWN` and receive no points.
- Commercial accessibility and first-revenue probability are decision-critical.
- Need means an evidence-backed capability or access gap, not assumed financial weakness.
- Strong manufacturing without demonstrated business-development need is not an Atlas opportunity.

### Hard gates

| Gate | Pass condition | Failure decision | Evidence required |
|---|---|---|---|
| Upstream discovery | Stable manufacturer record and discovery rationale exist | `WATCH`; do not discover within this module | Accepted discovery record |
| Entity and manufacturer status | Correct Turkish operating entity and real manufacturing are verified | `DROP` when disproven; `WATCH` when resolvable | First-party plus independent evidence |
| Demand context | Defined foreign product/capability need and target context exist | `WATCH`; no supply-first progression | Accepted demand or opportunity evidence |
| Relevant manufacturing fit | Manufacturer can plausibly supply the defined demand context | `DROP` when fit is absent | Technical product/process evidence |
| Evidence integrity | No invented, fabricated or materially misattributed evidence | `DROP` | Traceable evidence register |
| Legal and critical risk screen | No known disqualifying legal, sanctions, fraud or safety conflict in reviewed evidence | `DROP` when confirmed; `WATCH` while unresolved | Appropriate authoritative evidence when a risk signal exists |
| Commercial model plausibility | A lawful, understandable route exists for Atlas to create and capture value | `WATCH` if unverified; `DROP` if structurally absent | Commercial-model hypothesis and evidence |
| Material contradiction | No unresolved contradiction that could reverse the decision | `WATCH` or `DROP` depending on severity | Contradiction log |

### Exclusion rules

Exclude or stop analysis for:

- distributors, traders, marketplaces, brokers or service-only firms presented as manufacturers;
- manufacturers unrelated to the defined demand context;
- duplicate or unresolved entities;
- companies included solely because they have an English website or public email;
- cases built on invented buyer demand, export activity, capacity or partnership interest;
- companies whose accessible evidence shows no plausible role for external business development;
- cases requiring changes outside Turkey Export to complete the specification.

### Stop rules

Stop when:

- all `PROCEED` gates are satisfied and one specific next validation action is ready;
- one decision-critical missing fact creates `WATCH` and a bounded verification plan is recorded;
- a hard failure or commercially decisive weakness creates `DROP`;
- additional research is unlikely to change the decision;
- the evidence cost exceeds the plausible first-revenue value.

Do not continue collecting sources merely to increase document length or score confidence cosmetically.

## Scoring

### Scoring dimensions

| Factor | Definition | Score range | Weight | Evidence requirement |
|---|---|---:|---:|---|
| Manufacturing Strength | Verified relevance, process capability, quality control, factory evidence and delivery credibility for the demand context | 0–100 | 15 | First-party technical evidence plus independent corroboration |
| Export Readiness | Demonstrated ability to serve foreign buyers through certifications, documentation, communication, logistics and export experience | 0–100 | 15 | Current export, certification or operational evidence; English content alone is insufficient |
| Growth Need | Dated evidence that the manufacturer seeks new markets, customers, capacity utilization or growth that external support could accelerate | 0–100 | 20 | Expansion, hiring, new capacity/product, market-entry or similar dated signals |
| Business Development Need | Specific evidence of insufficient target-market coverage, buyer access, export-sales capacity or partner capability that Atlas could address | 0–100 | 20 | Organization, role, channel, hiring, partner-search or accepted direct evidence |
| Partnership Openness | Evidence that the company uses or is receptive to agents, representatives, market-development partners or comparable external channels | 0–100 | 15 | Official partner/channel evidence or accepted authorized interaction; contact details alone are weak evidence |
| Atlas Revenue Potential | Evidence-backed feasibility that Atlas can create and capture value with acceptable access, timing, repeatability and capital risk | 0–100 | 15 | Named model, payer/revenue event, demand context, accessibility and time-to-first-revenue rationale |
| **Total** |  |  | **100** |  |

### Dimension anchors

Apply the following common anchors, then document dimension-specific evidence:

| Score | Interpretation |
|---:|---|
| 0 | Disproven, absent or entirely `UNKNOWN` |
| 25 | Weak indirect signal; decisive facts missing |
| 50 | Plausible and partly evidenced, but important gaps or contradictions remain |
| 75 | Strong, current and mostly direct evidence with manageable limitations |
| 100 | Exceptional, current, multi-source evidence with no material contradiction |

Scores between anchors require written justification. Do not award the same generic score across dimensions without dimension-specific evidence.

### Calculation

Calculate:

`Atlas Export Need Score = Σ (dimension score × dimension weight) / 100`

Round only the final result to the nearest whole number. Keep source values unrounded.

Rules:

- `UNKNOWN` evidence contributes zero to the affected dimension; it is not a neutral 50.
- If a dimension cannot be assessed because the required input is missing, show both the zero score and the decision-critical unknown.
- Do not subtract risk twice. Hard-gate failures determine the decision; evidenced weaknesses affect the relevant dimension score.
- Report Evidence Quality separately. It is a gate, not a weighted commercial dimension.

### Score interpretation

| Range | Meaning | Permitted action |
|---:|---|---|
| 75–100 | Strong candidate, subject to all floors and gates | `PROCEED` to deeper partnership validation |
| 50–74 | Plausible but incomplete or uneven case | `WATCH` with one bounded verification plan |
| 0–49 | Weak, inaccessible or commercially unjustified case | `DROP`, unless a clearly resolvable hard-gate unknown requires `WATCH` |

## Decision logic

### PROCEED

All conditions are mandatory:

- every hard gate passes;
- Atlas Export Need Score is at least 75;
- Evidence Quality is at least 70;
- Manufacturing Strength is at least 60;
- Export Readiness is at least 50;
- Growth Need is at least 55;
- Business Development Need is at least 60;
- Partnership Openness is at least 50;
- Atlas Revenue Potential is at least 60;
- no decision-critical field is `UNKNOWN`;
- one specific deeper partnership-validation action is defined.

`PROCEED` authorizes only deeper verification of manufacturer need, decision-makers, commercial model and partnership fit. It does not authorize contact, discovery, CRM activity or a commercial commitment.

### WATCH

Use `WATCH` when the opportunity is plausible but:

- the weighted score is 50–74;
- a required input or hard gate is unresolved but realistically verifiable;
- Evidence Quality is below 70 but the case is not disproven;
- one or more `PROCEED` dimension floors is not met because evidence is incomplete;
- a material contradiction requires resolution;
- partnership openness or the Atlas revenue path remains a hypothesis.

Every `WATCH` decision must name the missing fact, its decision impact, the smallest verification action, owner, due date and review trigger. No outreach is authorized while waiting. If the review deadline passes without new evidence, reassess using available evidence; do not leave the case indefinitely open.

### DROP

Use `DROP` when:

- a hard gate is conclusively failed;
- the Atlas Export Need Score is below 50 and no narrow verification could plausibly reverse the decision;
- real manufacturing or relevant capability is disproven;
- there is no defined foreign-demand fit;
- the company appears fully covered for the target market and no external business-development gap is evidenced;
- partnership access is structurally unavailable;
- no lawful or plausible Atlas revenue model exists;
- material integrity, sanctions, legal or fraud risk is confirmed;
- expected commercial value no longer justifies verification effort.

Record the decisive reason and evidence. A dropped case may re-enter only after a new, dated signal materially changes the failed condition.

### Decision precedence

1. Confirm scope and upstream discovery.
2. Apply entity, manufacturing, demand, evidence-integrity, legal/risk and commercial-model hard gates.
3. Calculate Evidence Quality.
4. Score the six commercial dimensions.
5. Apply the weighted threshold and dimension floors.
6. Check contradictions and decision-critical unknowns.
7. Issue `PROCEED`, `WATCH` or `DROP` with the exact authorized action.

Hard identity, manufacturing, demand, evidence, legal, sanctions, authorization and commercial-access failures override numeric scores.

## Acceptance criteria

- [ ] The document is a specification only and contains no executable engine.
- [ ] The analyzer accepts only an already-discovered Turkish manufacturer.
- [ ] The analyzer does not discover manufacturers, buyers, contacts or demand.
- [ ] The specification applies only to Turkey → World and requires no Foreign → Turkey modification.
- [ ] A defined foreign-demand context is required before `PROCEED`.
- [ ] Purpose, inputs, outputs, required evidence, scoring, decision logic and acceptance criteria are explicit.
- [ ] Every material claim is traceable to a source URL or stable repository record.
- [ ] Manufacturer identity and real manufacturing are hard gates.
- [ ] Required evidence separates first-party claims from independent corroboration.
- [ ] `UNKNOWN` receives no invented or default-positive score.
- [ ] The six required scoring dimensions are present exactly once.
- [ ] Scoring weights total 100.
- [ ] Evidence Quality is calculated separately and gates `PROCEED`.
- [ ] `PROCEED` requires the total threshold, all dimension floors and all hard gates.
- [ ] `WATCH` requires one bounded verification plan with owner and review trigger.
- [ ] `DROP` records a decisive reason and evidence.
- [ ] Business Development Need is based on a specific capability or access gap, not assumed company weakness.
- [ ] Partnership Openness is not inferred from public contact details alone.
- [ ] Atlas Revenue Potential evaluates model, payer/revenue event, accessibility, timing and capital risk.
- [ ] Commercial accessibility and first-revenue probability affect the decision.
- [ ] Every decision states what it authorizes and does not authorize.
- [ ] The specification implements no CRM or email automation.
- [ ] Privacy, authorization, contradiction and source-freshness rules are testable.
- [ ] Stop rules prevent indefinite evidence collection.

## Open questions

| Question | Decision impact | Verification owner | Due date |
|---|---|---|---|
| Should sector-specific certification floors supplement the generic Export Readiness floor? | May create product-family-specific hard gates | Turkey Export specification owner | Before APPROVED status |
| What review period should automatically expire an unresolved `WATCH` case? | Controls stale opportunity accumulation | Turkey Export commercial owner | Before APPROVED status |
| Which commercial models may be used without additional legal review? | Defines permitted Atlas Revenue Potential assumptions | Atlas CEO or authorized legal reviewer | Before implementation authorization |

## Change history

| Version | Date | Change | Reason | Owner |
|---|---|---|---|---|
| 0.1 | 2026-07-06 | Initial specification | Define evidence and decision requirements for Export Need Analyzer | Turkey Export Commercial Intelligence |
