# R005 — External Export Office Sector Selection Sprint 001

- **Scope:** Turkey → World only. Foreign → Turkey untouched. No architecture change.
- **Objective:** Determine which industrial sector offers the highest probability of Atlas successfully selling its External Export Office services (`ATLAS_SERVICE_STANDARD.md`) — not which manufacturer or opportunity to pursue.
- **Method:** Sector-level comparison first, manufacturer-level work deliberately excluded from this sprint. Combines (a) fresh public market research on all 11 candidate sectors and (b) Atlas's own accumulated evidence from prior work in this repository — six existing manufacturer records (`database/turkish_manufacturers.csv`), nineteen freshly discovered prospects (`prospects/EEO_Prospect_Sprint_001.md`), and two buyer-side briefs (`briefs/COB_001_Germany_OEM_Machining/`, `briefs/COB_001/`) — all of which sit inside the CNC Machining / Precision Machining / Sheet Metal / Metal Fabrication cluster.
- **Evidence cutoff:** 2026-07-06.

## Methodology

Each sector is scored 0–100 on four equally weighted (25 points each) categories, each averaging several 0–100 sub-scores per the brief's required dimensions:

- **MARKET** (European demand, Middle East demand, growth trend, nearshoring potential)
- **MANUFACTURERS** (number of Turkish medium-sized manufacturers, export maturity, export growth potential)
- **BUSINESS** (repeat order potential, average order value, sales cycle, buyer accessibility)
- **ATLAS FIT** (need for external export office, need for international BD, need for buyer discovery, need for market-entry strategy, representation potential, success-fee potential, long-term relationship potential)

All sub-scores are `ESTIMATED` — derived from the public market data and dated sources cited per sector, not from company-level verification (that remains scoped to manufacturer-level briefs). Where Atlas has direct, prior evidence (CNC/Precision Machining, Sheet Metal, Metal Fabrication), sub-scores also draw on that accepted evidence, which materially raises confidence relative to the other eight sectors.

## Sector scorecard

| # | Sector | Market /25 | Manufacturers /25 | Business /25 | Atlas Fit /25 | **Total /100** | Rank |
|---|---|---:|---:|---:|---:|---:|---:|
| 1 | CNC Machining | 19.4 | 18.8 | 15.9 | 19.1 | **73.2** | 1 |
| 2 | Precision Machining | 19.5 | 16.7 | 16.4 | 19.5 | **72.1** | 2 |
| 3 | Industrial Valves | 18.4 | 16.3 | 15.3 | 15.9 | **65.9** | 3 |
| 4 | Sheet Metal Fabrication | 15.6 | 16.3 | 15.6 | 17.5 | **65.0** | 4 |
| 5 | Metal Fabrication | 15.0 | 15.5 | 15.0 | 17.5 | **63.0** | 5 |
| 6 | Plastic Injection Molding | 16.6 | 14.2 | 14.7 | 15.5 | **61.0** | 6 |
| 7 | Rubber Components | 13.8 | 11.3 | 12.5 | 12.9 | **50.4** | 7 |
| 8 | Industrial Fasteners | 12.2 | 12.5 | 13.1 | 11.4 | **49.2** | 8 |
| 9 | Aluminum Extrusion | 15.0 | 10.8 | 12.2 | 10.7 | **48.7** | 9 |
| 10 | Automation Components | 9.7 | 8.8 | 11.3 | 9.3 | **39.0** | 10 |
| 11 | Industrial Electronics | 8.8 | 8.3 | 9.1 | 8.0 | **34.2** | 11 |

**Top 10** = all sectors above except Industrial Electronics (rank 11), which scored lowest across every category.

**Top 3** = CNC Machining, Precision Machining, Industrial Valves.

## Sector notes (why each scored as it did)

**CNC Machining / Precision Machining (ranks 1–2, treated as one cluster in practice).** These two are nearly the same population in Turkey — most Atlas-tracked manufacturers carry both tags simultaneously (`database/turkish_manufacturers.csv`). This is the only cluster with direct Atlas evidence: 6 existing manufacturer records, 19 freshly verified/partially-verified prospects, and real buyer-side demand signals already found (CNH Industrial's live supplier application, KION/GEA/Krones supplier registration, and — most materially — Xometry's 2023 acquisition of Istanbul's Tridi and its active Turkish-manufacturer recruitment page, per `briefs/COB_001_Germany_OEM_Machining/evidence_log.md`). Turkey's machinery exports also grew from an estimated $26B (2025) toward a $29B (2026) target (Invest in Türkiye / trade press). Manufacturer maturity is mixed — most prospects are single-source `WATCH`-level, not yet independently verified — which is the honest reason this scores 73/72, not higher.

**Industrial Valves (rank 3).** Real, dated export activity (4,854 valve export shipments from Turkey as of November 2025, per Volza trade data) and an established manufacturer base (Şensoylar/TÜRKOGLU since 1978, VARNASAN since 1976, Proval) with genuine Middle East export relevance — valves connect naturally to oil/gas and water infrastructure, a stronger Middle East thesis than most other candidates. Scores lower than the machining cluster only because Atlas has no direct manufacturer-level evidence yet — this sector's score is built entirely from today's market research, not from verified company records.

**Sheet Metal Fabrication / Metal Fabrication (ranks 4–5).** Real Atlas evidence exists here too (Ulus Metal, LD PRES, Alsa Çözüm Metal, Simer Sac, SKP from `prospects/EEO_Prospect_Sprint_001.md`), and repeat-order potential is high (serial production for bus/rail/appliance OEMs, e.g. Solaris, Škoda in `database/foreign_buyers.csv`). Scores below the machining cluster mainly on Business — heavier, bulkier parts carry lower per-unit value and a bulkier accessibility problem, and one existing record (Ulus Metal) already shows a possible direct-presence/channel-conflict complication in its best market (Poland).

**Plastic Injection Molding (rank 6).** Real European demand and growth (EU injection-molded plastics market ~$121B in 2025, 4.09% CAGR) and a genuine Turkish cost advantage (20–30% vs. Western Europe, per Freshdi/industry sources), but most of what surfaced in research was Turkish *machine-builders* exporting injection-molding machinery, not a clearly sized population of medium *contract molders* — Atlas's actual target client type. This is a real, structural evidence gap, not a low score on demand.

**Rubber Components, Industrial Fasteners, Aluminum Extrusion (ranks 7–9).** Each has a real, large end-market (Turkey's $17.95B auto-parts exports include rubber/plastic; Europe's fastener market is ~$25.8B; Europe's aluminum extrusion market is projected to reach ~$50.8B by 2033), but each has a structural mismatch with Atlas's target client: rubber components and fasteners are dominated at the top by already-export-mature Tier-1s (Standard Profil, ELPA) with a thin, poorly evidenced medium tier beneath them; aluminum extrusion in Turkey is dominated by large secondary-smelting/recycling mills serving construction and white goods, not a broad population of medium export-ready component subcontractors. Aluminum extrusion also carries a 2026 EU CBAM (Carbon Border Adjustment Mechanism) complication — one source alleges Turkish exporters currently benefit from a loophole that undercuts EU recyclers, which is a real regulatory/reputational risk for a new long-term Atlas client relationship in this sector, not a tailwind.

**Automation Components, Industrial Electronics (ranks 10–11).** Turkey's own automation and electronics figures found in this research (a $1.8B domestic industrial-automation market, a $6.7B electronic-components market) describe Turkey as a *growing consumer/importer* of these categories, not an export-manufacturing base — the opposite of what an External Export Office needs. The one large named player in electronics (Vestel) is already a mature, large-scale exporter, not Atlas's target client. No credible medium-sized, export-curious manufacturer population was identified for either sector within this sprint's research bound.

## Recommended first sector

**CNC Machining and Precision Machining, treated as one combined go-to-market focus.**

This is the only sector where "why this sector" rests on accepted Atlas evidence rather than today's market research alone: a verified prospect list already exists (`prospects/EEO_Prospect_Sprint_001.md`), buyer-side demand channels are already identified and partially evidenced (`briefs/COB_001_Germany_OEM_Machining/`), and the target client profile in `ATLAS_SERVICE_STANDARD.md` (medium-sized, growth-oriented, export-ready or export-curious, no strong BD function) matches this sector's population almost exactly.

## Recommended client profile

A Turkish CNC/precision machining or sheet-metal manufacturer with: 20–150 employees; at least one ISO 9001-class certification (held or in progress); some existing but undeveloped export activity or explicit growth ambition; no dedicated export-sales or BD hire; and a real, verifiable operating identity (own site plus at least one independent source — OSB registry, chamber, or trade directory). This matches the profile of the strongest entries in `prospects/EEO_Prospect_Sprint_001.md` (Alsa Çözüm Metal, Seç Kama, Triga Metal, Simer Sac).

## Recommended revenue model

A **manufacturer-paid advisory/retainer model**, optionally layered with a success fee tied to a confirmed, named buyer introduction (not a completed order). This is the only model consistently supported across every prior brief in this repository: every buyer-side channel found so far (CNH, KION, GEA, Krones supplier portals; Xometry, Techpilot, CNC24 sourcing platforms) is self-service or distributor-mediated, with no natural payer-side role for Atlas as a commission-earning intermediary. The manufacturer, not the buyer, is the only party with an identifiable reason to pay Atlas directly. This matches service #9 ("Fractional Export Director") and #1–8 in `ATLAS_SERVICE_STANDARD.md`'s service portfolio more than a pure commission/representation model.

## Expected time to first revenue

- **First advisory/retainer revenue:** 4–8 weeks — bounded by closing one services agreement with a prospect already identified in `prospects/EEO_Prospect_Sprint_001.md`; no new discovery work is required to start this conversation.
- **First commission or success-fee revenue:** 6–12 months at the earliest — bounded by manufacturer qualification cycles (certification checks, PPAP-style buyer qualification) observed consistently across `database/opportunities.csv` and both prior briefs, and by the fact that no confirmed buyer order exists yet for any tracked opportunity.

## Expected implementation difficulty

**Low to moderate.** No new specification, engine, agent or workflow is required — `specs/01`–`06` and `workflows/commercial_opportunity_workflow.md` already cover every step from discovery to CEO decision. The remaining work is commercial execution (manufacturer conversations, retainer proposals), not tooling or research capacity.

## CEO Review

**Why this sector?** It is the only one of the eleven where Atlas already has a real, partially-verified manufacturer pipeline, a matched target-client profile, and at least one strong, independently corroborated buyer-side channel (Xometry Türkiye). Every other sector's score in this report rests on public market data alone, not on Atlas's own accepted evidence.

**Why not the others?** Industrial Valves (rank 3) is a legitimate second candidate — real export activity and a strong Middle East thesis — but has zero Atlas manufacturer-level evidence yet; it is the recommended second sector to open, not a reason to delay the first. Sheet Metal and Metal Fabrication (ranks 4–5) are close behind and already share manufacturers with the machining cluster — treat them as adjacent, not separate, go-to-market work. Plastic Injection Molding, Rubber Components, Industrial Fasteners and Aluminum Extrusion each have a real end-market but a structural mismatch with Atlas's target client (machine-builders instead of molders; Tier-1-dominated barbell populations; large-mill-dominated populations). Automation Components and Industrial Electronics show Turkey as a net importer/consumer in the categories researched, not an export base — the opposite of what an export office needs.

**Fastest path to first paying client:** Open advisory/retainer conversations with the highest-confidence, best-verified names in `prospects/EEO_Prospect_Sprint_001.md`'s Top 10 — Alsa Çözüm Metal, Seç Kama and Triga Metal are the strongest combination of verified identity and evidenced BD gap.

**Fastest path to first commission:** Not realistic in the short term on current evidence. The most plausible route is a success fee tied to a confirmed introduction into the Xometry Türkiye network (`briefs/COB_001_Germany_OEM_Machining/`), contingent on first resolving Atlas's own commercial-model hypothesis there — this is not yet validated and should not be treated as a near-term revenue line.

**GO / WATCH / DROP: GO** — on sector selection only. This confirms CNC Machining / Precision Machining as Atlas's primary go-to-market focus and Industrial Valves as the recommended second sector to research at manufacturer level. It does not authorize outreach to any specific company; contact with any manufacturer named in `prospects/EEO_Prospect_Sprint_001.md` still requires the authorization gates already defined in that document and in `briefs/COB_001_Germany_OEM_Machining/first_contact_strategy.md`.
