# Commercial Opportunity Brief — Turkey → Germany, CNC / Precision Machining

Applies [`workflows/commercial_opportunity_workflow.md`](../../workflows/commercial_opportunity_workflow.md) steps 1–6. No new specification, engine or architecture change. Evidence cutoff 2026-07-06.

## Step 1 — Discover company

**Manufacturer side (reused):** Five Atlas-recorded manufacturers carry the CNC Machining / Precision Machining tag in `database/turkish_manufacturers.csv`: ERBAB Otomat, Pro-Mak Automotive, Kurutlu Technologies, Girginer Oto Endüstri, Smartist Industrial Solutions. Ulus Metal is excluded — it is tagged Sheet Metal / Fabrication, not this subsector. Of the five, Pro-Mak (56 employees, company-stated) and Kurutlu (25 employees, company-stated) most clearly match the "medium-sized, evidenced BD gap" target profile; ERBAB's scale (50 CNC machines, 4,800 m² facility) reads larger; Girginer and Smartist carry weaker existing evidence per `reports/R002_sprint_001_opportunity_discovery.md`.

**Buyer side (new discovery, this brief):** `database/foreign_buyers.csv` has no German sourcing company, contract-manufacturing buyer or procurement company — only three large Foreign OEMs (KION, GEA, Krones). Bounded public-source search for this brief identified four candidates matching the requested buyer profile:

1. **Xometry Europe GmbH / Xometry Türkiye** — German-headquartered (Hohenbrunn) manufacturing-sourcing network; acquired Istanbul-based Tridi (2023-03-03) and operates an active Turkish CNC-manufacturer recruitment page.
2. **Techpilot (DynamicMarkets GmbH)** — German e-sourcing platform live since 2000; 16,000+ registered buyers post drawing-part RFQs (avg. order value €35,000) matched to a supplier database by capability, certification and location.
3. **CNC24 GmbH** (Berlin) — CNC contract-manufacturing platform; open, free partner-application process; ~500 manufacturers in its network.
4. **Spanflug Technologies GmbH** — German CNC procurement platform; ~400 partners, but its own partner page requires the production facility to be located in the EU.

Full source list in [`evidence_log.md`](evidence_log.md).

## Step 2 — Export Need Analyzer (manufacturer screening)

Reuses existing Atlas Export Need Score-equivalent evidence (`reports/R002`), not recalculated here. Pro-Mak and Kurutlu both carry `PROCEED`-level manufacturing/export-readiness evidence at the discovery-engine layer but remain single-source (company website only) — no independent industrial source class has corroborated either. Per `specs/01_export_need_analyzer.md`, Evidence Quality below 70 caps both at `WATCH`, unchanged from Sprint 001.

## Step 3 — Demand Signal Engine (buyer screening)

| Buyer | Signal type | Date | Independent corroboration | Signal read |
|---|---|---|---|---|
| Xometry Europe/Türkiye | Acquisition + active Turkish supplier-registration page | 2023-03-03 (acquisition); page current at 2026-07-06 access | GlobeNewswire press wire; Turkish government invest agency (invest.gov.tr); 3DPrint.com trade press | Strong — explicit, dated, multi-class corroborated |
| Techpilot | Established RFQ marketplace; no single dated event | UNKNOWN (platform ongoing since 2000) | Company site only, at access date | Moderate — real and large, but undated as a signal and Turkish-supplier eligibility unconfirmed |
| CNC24 | Open partner-recruitment page | UNKNOWN | Company site; Handelsregister reference (Berlin, Amtsgericht Charlottenburg) named on page | Weak-moderate — real entity, no dated event, geography unconfirmed |
| Spanflug | Partner-recruitment page, explicit EU-only eligibility | UNKNOWN | Company site only | Disqualifying for this opportunity — hard gate fails on eligibility, not on demand |

Per `specs/02_demand_signal_engine.md`, Xometry is the only candidate combining demand directness, recency, buyer specificity and independent corroboration strongly enough to score in the `PROCEED`-adjacent range (~75) on the demand-signal dimension alone. Spanflug fails the eligibility hard gate outright: its own site states "production facility located in the EU," which no Turkish manufacturer meets without a separate EU entity.

## Step 4 — Matching Engine

**Manufacturer–buyer technical fit:** Pro-Mak's and Kurutlu's CNC turning/milling capability is a direct match to Xometry's, Techpilot's and CNC24's stated categories (CNC machining, turning, milling). No mandatory-specification gate fails.

**Commercial-model fit — the decisive weak dimension.** Xometry, Techpilot and CNC24 are all self-service platforms: a Turkish manufacturer can register directly, free of charge (Xometry requires only invoicing capability; CNC24 is free with no long-term commitment). None of the three creates a natural payer, revenue event or role for Atlas as an intermediary in the buyer-manufacturer transaction itself. The only plausible Atlas commercial model is an advisory/business-development engagement paid by the Turkish manufacturer (e.g., preparing the capability pack, application, or utilization strategy for faster/better acceptance and order flow) — this is a `HYPOTHESIS`, not an accepted model, and it changes Atlas's payer from the buyer side to the manufacturer side.

Per `specs/03_matching_engine.md`: "A model with no identifiable payer, revenue event or accessible next step cannot PROCEED." The manufacturer-side advisory hypothesis is not structurally absent (a payer and service exist in principle), so this does not fail the hard gate outright — but it is unverified and caps the match at `WATCH`.

## Step 5 — Opportunity Scoring (top pairing: Pro-Mak / Kurutlu → Xometry Europe/Türkiye)

| Dimension | Weight | Score | Rationale |
|---|---:|---:|---|
| Accessibility | 25 | 70 | Self-service registration is low-friction, but low-friction also means Atlas has no controllable gate into the relationship |
| Signal Strength | 25 | 72 | Dated, multi-source-corroborated buyer-side signal; manufacturer side still single-source |
| Revenue Potential | 20 | 30 | No verified payer/revenue event for Atlas; manufacturer-paid advisory model is `HYPOTHESIS`, order/commission values `UNKNOWN` |
| Execution Speed | 15 | 55 | Manufacturer self-registration is fast; an Atlas-billable engagement requires a sales/negotiation step of unknown length |
| Verification Confidence | 15 | 55 | Buyer-side evidence is strong; manufacturer identity/manufacturing evidence remains uncorroborated by an independent source class |

`Atlas Opportunity Score ≈ (70×25 + 72×25 + 30×20 + 55×15 + 55×15) / 100 ≈ 59` (ESTIMATED). Below the `PROCEED` floor of 80, and Verification Confidence (55) is below the required 70. No hard gate is failed; the opportunity is not disproven.

## Step 6 — CEO Decision

**WATCH.** Rationale:

- No hard gate fails for the Pro-Mak/Kurutlu → Xometry pairing.
- The buyer-side signal is unusually strong for this module — stronger than any existing Sprint 001 record — but Atlas's own revenue-capture role is the unresolved, decision-critical gap, not buyer or manufacturer credibility.
- Spanflug is `DROP` for this opportunity specifically: its EU-only eligibility requirement is a disproven-fit hard gate for any Turkish manufacturer without an EU facility.
- Techpilot and CNC24 remain `WATCH` pending Turkish-supplier eligibility confirmation and a dated commercial signal.

**Authorized next action:** the verification plan in `top_targets.md` and `first_contact_strategy.md`. **Not authorized:** contacting Pro-Mak, Kurutlu, Xometry, Techpilot or CNC24; registering any manufacturer on any platform; drafting outreach; any commercial commitment.
