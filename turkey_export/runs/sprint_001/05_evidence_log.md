# Evidence Log — Sprint 001 (OEM Metal Components)

Evidence cutoff: 2026-07-06. Source records: [`database/turkish_manufacturers.csv`](../../database/turkish_manufacturers.csv), [`database/foreign_buyers.csv`](../../database/foreign_buyers.csv), [`database/opportunities.csv`](../../database/opportunities.csv). No new source was added in this run; this log consolidates existing per-record `source_urls`, `source_classes` and `signal_summary` fields for audit.

## Turkish manufacturers (6 evaluated)

| Manufacturer | Source class(es) | Evidence state | Decisive unknown |
|---|---|---|---|
| ERBAB Otomat | Official company website only | ESTIMATED | Independent institutional corroboration; available capacity; commercial openness |
| Pro-Mak Automotive | Official company website only | ESTIMATED | Certificate validity; open capacity; independent corroboration |
| Kurutlu Technologies | Official company website only | ESTIMATED | Named export customers/countries; independent corroboration |
| Ulus Metal | Official company website only | ESTIMATED | Certification detail; machine list; Poland-entity bypass risk |
| Girginer Oto Endüstri | Official company website only | ESTIMATED | Independent corroboration (per `reports/R002`) |
| Smartist Industrial Solutions | Official company website only | ESTIMATED / WATCH | Transaction/export evidence absent — weakest record in the set |

All six are single-source-class (company-controlled). None has cleared the two-independent-source-class bar defined in `discovery/discovery_engine.md`.

## Foreign buyers (10 evaluated, 5 carried into Top 20)

| Buyer | Source class(es) | Evidence state | Decisive unknown |
|---|---|---|---|
| CNH Industrial N.V. | Official company procurement/supplier source | ESTIMATED | Current commodity/category demand for this part family |
| KION Group AG | Official company procurement/supplier source | ESTIMATED | Current category demand; qualification burden |
| GEA Group AG | Official company procurement/supplier source | ESTIMATED | Category-specific demand behind general subcontract-manufacturing statement |
| Krones AG | Official company procurement/supplier source | ESTIMATED | Metal-component category demand |
| Lely Industries N.V. | Official company procurement/supplier source | ESTIMATED | No open commodity request found |
| Solaris Bus & Coach, Škoda Group, VDL Groep, Danieli & C., IMA S.p.A. | Official company procurement/supplier source | ESTIMATED | Category-specific demand and access route detail (see `database/foreign_buyers.csv`) |

All buyer signals are procurement-access evidence (supplier portal, registration route, published supplier need) — access architecture, not a confirmed open order, per `discovery/discovery_engine.md`.

## Opportunities (20 scored)

Every opportunity's `score_evidence_state` in `database/opportunities.csv` is `ESTIMATED`. No opportunity has a `VERIFIED` decisive claim. Common unresolved fields across all 20: estimated order potential, estimated commission potential, exact buyer mandate, incumbent supplier position, and current pricing — all `UNKNOWN`, none invented.

## Contradictions

One material contradiction is on record: Ulus Metal's own website lists a Polish contact address and email alongside its Turkey operation (`en.ulusmetal.com.tr`), which raises intermediary-bypass and channel-conflict risk for any Poland-market opportunity (ranks 7 and 12). This is unresolved and is carried forward as a `WATCH` factor, not a hard `DROP`, because no evidence yet confirms the Polish entity transacts the same product category directly with Solaris.

## Evidence expiry

Per `discovery/discovery_engine.md`, export-readiness and growth-need evidence should be reviewed within 24 months and business-development evidence within 18 months of its publication date. Exact publication dates for most cited pages are `UNKNOWN` (undated company web content); access date for all records is 2026-07-06. Re-verify freshness at the next review trigger (2026-08-05, per [`04_30day_action_plan.md`](04_30day_action_plan.md)) regardless of whether independent verification succeeds.

## Integrity statement

No company, contact, demand, order, RFQ, price, capacity, certification or buyer intent was invented in this run or in the underlying Sprint 001 records reused here. Every named entity in this log traces to a source URL recorded in `database/turkish_manufacturers.csv`, `database/foreign_buyers.csv` or `database/opportunities.csv`.
