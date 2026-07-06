# Turkey Export Pipeline

Minimal decision view for the OEM Metal Components export module. Values must be supported by module records; use `UNKNOWN` when not verified.

## Commercial Signal Discovery Engine v2

| Metric | Current | Target ceiling | Source / last update |
|---|---:|---:|---|
| Discovered manufacturers | 6 | 100 | `reports/R002_sprint_001_opportunity_discovery.md` |
| Multi-source validated manufacturers | 0 | UNKNOWN | `reports/R003_Discovery_Engine_v2.md` |
| PROCEED manufacturers | 0 | 20 | `database/turkish_manufacturers.csv` |
| PROCEED opportunities | 0 | 5 | `database/opportunities.csv` |
| WAIT manufacturers | 6 | UNKNOWN | `database/turkish_manufacturers.csv` |
| WAIT opportunities | 20 | UNKNOWN | `database/opportunities.csv` |
| DROP manufacturers | 0 | UNKNOWN | UNKNOWN |

- **Active vertical:** OEM Metal Components
- **Discovery decision:** WAIT
- **Reason:** v2 migration is complete; independent multi-source verification is below the 70 threshold for all current opportunities.
- **Next action:** Verify ERBAB factory/entity and certificate scope through at least two independent industrial source classes.

## v2 Opportunity Snapshot

| Rank | Opportunity | Accessibility | Signal | Verification | Atlas Opportunity | Decision | First action |
|---:|---|---:|---:|---:|---:|---|---|
| 1 | ERBAB → CNH | 80 | 55 | 65 | 77 | WAIT | Independent factory/entity and certificate verification |
| 2 | ERBAB → KION | 78 | 45 | 62 | 75 | WAIT | Reuse manufacturer verification; confirm category access |
| 3 | Pro-Mak → CNH | 80 | 55 | 62 | 74 | WAIT | Verify industrial registration; IATF scope and dated signal |
| 4 | Pro-Mak → KION | 78 | 45 | 60 | 73 | WAIT | Verify manufacturer and current commercial signal |
| 5 | Pro-Mak → GEA | 82 | 50 | 60 | 73 | WAIT | Verify manufacturer and category-specific need |

## Current Opportunity

| Field | Value |
|---|---|
| Turkish manufacturer | ERBAB Otomat Yedek Parça Sanayi Ticaret A.Ş. |
| Product category | Precision-machined automotive and machinery components |
| Export Readiness Score | 90 (ESTIMATED) |
| Best target country | Italy |
| Commercial owner | UNKNOWN |
| Evidence cutoff | 2026-07-06; v2 migration |
| Decision | WAIT |

## Buyer Pipeline

| Stage | Count | Source / last update |
|---|---:|---|
| Potential foreign buyers | 10 | `database/foreign_buyers.csv` |
| Scored buyers | 10 | `database/foreign_buyers.csv` |
| Priority buyers | 0 | `reports/R003_Discovery_Engine_v2.md` |
| Outreach drafts ready | 0 | UNKNOWN |
| Outreach authorized | 0 | UNKNOWN |
| Buyers contacted | 0 | UNKNOWN |
| Replies | 0 | UNKNOWN |
| Meetings booked | 0 | UNKNOWN |
| Meetings held | 0 | UNKNOWN |

## Top 5 Priority Buyers

| Priority | Buyer | Country | Buyer Fit Score | Bypass Risk | Status | Next action | Owner | Due date |
|---:|---|---|---:|---:|---|---|---|---|
| 1 | CNH Industrial | Italy | 94 (legacy) | UNKNOWN | WAIT | Independently verify ERBAB; then category access | UNKNOWN | UNKNOWN |
| 2 | KION Group | Germany | 92 (legacy) | UNKNOWN | WAIT | Independently verify ERBAB; then category access | UNKNOWN | UNKNOWN |
| 3 | CNH Industrial | Italy | 94 (legacy) | UNKNOWN | WAIT | Independently verify Pro-Mak; then category access | UNKNOWN | UNKNOWN |
| 4 | KION Group | Germany | 92 (legacy) | UNKNOWN | WAIT | Independently verify Pro-Mak and current signal | UNKNOWN | UNKNOWN |
| 5 | GEA Group | Germany | 90 (legacy) | UNKNOWN | WAIT | Independently verify Pro-Mak and category need | UNKNOWN | UNKNOWN |

## Decision Summary

- **Turkish manufacturer summary:** ERBAB has strong company-stated CNC; certification and European export evidence; independent institutional verification is pending.
- **Export readiness score:** 90 (ESTIMATED)
- **Best target country:** Italy
- **Top 20 potential foreign buyers:** 20 legacy opportunities migrated to v2; all currently WAIT
- **Top 5 priority buyers:** None approved under v2; top verification candidates are CNH; KION and GEA
- **Outreach email drafts:** 0 — prohibited at this stage
- **Key risks:** Single-source manufacturer claims; no exact RFQ; mandate; price; capacity confirmation or protected commission terms
- **Next best action:** Independent ERBAB factory/entity and certificate verification; no company contact
- **Decision:** WAIT
