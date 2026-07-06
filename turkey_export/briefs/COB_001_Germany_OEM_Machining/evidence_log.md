# Evidence Log — Commercial Opportunity Brief #001

Access date for all new sources: 2026-07-06. All URLs were retrieved via public web search/fetch during this brief; none required authentication.

## Manufacturer side (reused from existing Atlas records)

| Manufacturer | Source | Evidence state | Notes |
|---|---|---|---|
| Pro-Mak Automotive | `database/turkish_manufacturers.csv`; https://www.pro-mak.com/en/ | ESTIMATED | Single source class (company website); unchanged from Sprint 001 |
| Kurutlu Technologies | `database/turkish_manufacturers.csv`; https://www.kurutlu.com/ | ESTIMATED | Single source class; unchanged |
| ERBAB Otomat | `database/turkish_manufacturers.csv`; https://erbab.com.tr/en/ | ESTIMATED | Single source class; unchanged |

No new manufacturer-side evidence was gathered in this brief.

## Buyer side (new discovery, this brief)

### Xometry Europe GmbH / Xometry Türkiye

- Company sources: https://xometry.eu/en/partners/ ; https://xometry.com.tr/en/ ; https://xometry.com.tr/en/partner-ol/ — describe an open, free partner-network application (legal requirement: ability to issue invoices), 2,500+ partners across Europe and Türkiye, 300+ CNC lathes/machining centers in the Turkey network specifically.
- Independent source 1 (press wire): GlobeNewswire, "Xometry Launches In Turkey With The Acquisition Of Tridi," 2023-03-03 — https://www.globenewswire.com/news-release/2023/03/03/2619962/0/en/Xometry-Launches-In-Turkey-With-The-Acquisition-Of-Tridi-Turkey-s-Leading-On-Demand-Manufacturing-Marketplace.html
- Independent source 2 (government/institutional): Republic of Türkiye Investment Office, "US-Headquartered Xometry Extends Foothold in Türkiye by Acquiring Tridi" — https://www.invest.gov.tr/en/news/news-from-turkey/pages/us-headquartered-xometry-extends-foothold-in-turkiye-by-acquiring-tridi.aspx
- Independent source 3 (trade press): 3DPrint.com, "Xometry Buys Turkish On-Demand Marketplace Tridi" — https://3dprint.com/298573/xometry-buys-turkish-on-demand-marketplace-tridi/
- Evidence state: **VERIFIED** for the acquisition fact and date (three independent, non-company source classes agree). **ESTIMATED** for current partner counts and Turkey-specific machine counts (company-stated, not independently re-verified at 2026-07-06).
- Decisive unknown: whether any Atlas-tracked manufacturer (Pro-Mak, Kurutlu, ERBAB) is already in this network.

### Techpilot (DynamicMarkets GmbH)

- Company sources: https://www.techpilot.com/en ; https://www.techpilot.com/en/for-buyers ; https://www.techpilot.com/en/for-europe — state operation since 2000, 16,000+ registered buyers, 30,000+ parts requests/year, average order value €35,000, 24,000+ suppliers across 280 manufacturing technologies including CNC turning and milling.
- Independent corroboration: none obtained in this brief.
- Evidence state: ESTIMATED. Decisive unknown: Turkish-supplier eligibility (no eligibility statement found either way).

### CNC24 GmbH

- Company sources: https://www.cnc24.com/become-a-partner/ ; https://www.cnc24.com/about-us/ — describe a free, three-step partner application, ISO 9001 preferred (not stated mandatory), and reference the company's Berlin address and Amtsgericht Charlottenburg commercial-register entry directly on the company's own page.
- Independent corroboration: the Handelsregister/commercial-register reference is cited on the company's own page, not independently re-verified against the register itself in this brief — treated as company-controlled evidence pending direct registry confirmation.
- Evidence state: ESTIMATED. Decisive unknowns: geographic eligibility for Turkish partners; any dated commercial signal.

### Spanflug Technologies GmbH

- Company source: https://spanflug.de/en/become-manufacturing-partner/ — explicitly states four eligibility criteria including "production facility located in the EU," alongside turning/milling specialization and ISO 9001:2015 (or equivalent) certification. ~400 partners, ~95% in Germany/Austria.
- Evidence state: VERIFIED for the eligibility statement (direct quote from the company's own published partner criteria — a first-party claim about the company's own policy, which is the correct evidence class for a policy fact).
- Effect: hard-gate disqualification for any Turkish manufacturer without a separate EU-based facility. This is why Spanflug is `DROP` in this brief rather than `WATCH`.

## Contradictions

None identified between sources for the same claim. Xometry's own site and third-party press/government sources agree on the Tridi acquisition and its timing.

## Stop rule applied

Research stopped once one defensible `WATCH` decision (Pro-Mak/Kurutlu → Xometry) and one defensible `DROP` (Spanflug) were supported by evidence, per `ATLAS_RULES.md`: "Stop research when one defensible commercial decision or next verification action is ready." Additional buyer types explicitly requested (medium-sized German OEMs, dedicated procurement companies distinct from sourcing platforms) were searched but no candidate met this brief's evidence bar within the research bound applied; this gap is named in `top_targets.md` rather than filled with weak or invented candidates.

## Integrity statement

No company, contact, demand, order, RFQ, price, capacity, certification or buyer intent was invented in this brief. Every named buyer traces to a source URL listed above; every named manufacturer traces to `database/turkish_manufacturers.csv`.
