# Commercial Opportunity Brief — Demand-First Analysis (SPEC_002 Implementation)

Implements [`specs/02_demand_signal_engine.md`](../../specs/02_demand_signal_engine.md). Evidence cutoff 2026-07-06. Region: Europe and Middle East. No new specification, engine or workflow.

## Step 1 — Establish demand before selecting a manufacturer

Per `ATLAS_RULES.md`'s demand-first doctrine, research began with sectoral and policy-level evidence of demand, not a manufacturer list.

| Signal | Type | Date | Source class | Evidence state |
|---|---|---|---|---|
| Gulf states (Kuwait, UAE, Qatar, Saudi Arabia) face ammunition shortages amid rising regional threats; Gulf states pursuing defense localization/diversification with Turkey | Dated policy/trade-press reporting | 2026-05 to 2026-07 | Independent trade/policy press (Breaking Defense, Gulf International Forum, Middle East Eye) | VERIFIED (reporting exists); ESTIMATED (implied component-level demand) |
| Roketsan (Turkish missile/ammunition prime) received Gulf-state requests for Cirit missile systems | Dated procurement-interest report | 2026 | Gulf International Forum | VERIFIED (report); UNKNOWN (whether this creates subcontract demand) |
| Turkey's 2025 defense exports: $5.6B (56%) to EU/NATO/US; $4.3B to Europe alone; exports to 185 countries | Dated trade statistic | 2025 (reported 2026) | Daily Sabah / Breaking Defense | VERIFIED |
| SSB (Turkish Secretariat of Defense Industries) led 130 Turkish companies to World Defense Show 2026, Riyadh, 2026-02-08 to 2026-02-12 | Government-organized trade delegation | 2026-02 (past relative to this cutoff) | Gulf International Forum / event coverage | VERIFIED; STALE as a forward action — this specific edition has already occurred |
| SAHA İstanbul (Turkey's largest defense/aerospace cluster; state-industry joint initiative with SSB and İTO) runs SAHA EXPO with 1,700+ exhibitors from 120+ countries and 25,000+ planned B2B/G2B/G2G meetings, aligned with NATO DIANA/NATO Innovation Fund | Recurring trade cluster/exhibition infrastructure | SAHA 2026 held 2026-05 (past relative to this cutoff); cluster membership and matchmaking are ongoing, not date-bound | SAHA İstanbul / SAHA EXPO organizers; IAF membership listing | VERIFIED for the infrastructure's existence; next-edition date UNKNOWN |
| European NATO allies increasingly view Turkish defense firms as useful partners (unmanned systems, electronic warfare, battlefield autonomy) amid reduced reliance on US supply | Policy analysis | 2026 | Brookings | VERIFIED (analysis); ESTIMATED (component-level read-through) |

**Reading discipline:** the two named 2026 events (World Defense Show Riyadh, SAHA EXPO Istanbul) have already occurred as of this evidence cutoff. They are treated here as evidence that active, recurring Gulf/NATO-facing access infrastructure exists for Turkish defense-industrial suppliers — not as open, actionable dates. Next-edition dates are `UNKNOWN` and are the first verification item in `commercial_action_plan.md`. The underlying demand narrative (Gulf shortages, NATO-ally diversification) is current through at least 2026-07 reporting and is not itself event-bound.

## Step 2 — Work backward to a manufacturer

The demand narrative requires: CNC/precision-machined defense-adjacent components (ammunition components, ground-systems parts), relevant certifications (AS9100, facility security clearance), and either an existing prime relationship or cluster-level access. Cross-checking Atlas's existing CNC/Precision Machining manufacturer records (`database/turkish_manufacturers.csv`) against this profile surfaces **ERBAB Otomat Yedek Parça Sanayi Ticaret A.Ş.** as the only candidate with independently corroborated defense-relevant certification and cluster membership. Full profile and verification classification in [`target_company.md`](target_company.md).

## Step 3 — Demand Signal Score (SPEC_002, applied to the ERBAB-relevant signal set)

| Factor | Weight | Score | Rationale |
|---|---:|---:|---|
| Demand directness | 25 | 55 | Sectoral/policy-level shortage and diversification evidence is real and dated, but no named buyer has requested ERBAB-specific components |
| Recency and timing | 20 | 70 | Reporting is current through 2026-05/07; underlying shortage and diversification dynamic is active, not historical |
| Buyer and need specificity | 15 | 40 | Gulf states and NATO allies are named; no specific buyer, RFQ or category request naming ERBAB's product family exists |
| Commercial accessibility | 15 | 60 | SAHA İstanbul membership is a real, standing access route to primes and procurement authorities |
| Turkish supply and revenue relevance | 15 | 65 | ERBAB's certified capability (AS9100, NATO facility security, ammunition-component experience per SAHA profile) is directly relevant |
| Independent corroboration | 10 | 75 | Demand narrative is corroborated across trade press, policy analysis and government-program reporting; ERBAB's fit is corroborated by SAHA İstanbul and HOSAB, independent of ERBAB's own site |
| **Weighted Demand Signal Score** | 100 | **≈58** | `Σ(score×weight)/100`, ESTIMATED |

Per `specs/02_demand_signal_engine.md`: score 50–74 is `WATCH` — plausible, with one resolvable critical gap (buyer/need specificity). No hard gate fails; demand is not disproven or stale.

## Decision

**WATCH.** See [`executive_summary.md`](executive_summary.md) for the full CEO Review and [`commercial_action_plan.md`](commercial_action_plan.md) for the authorized next action. This brief authorizes no outreach, CRM activity, quotation, order or commercial commitment.
