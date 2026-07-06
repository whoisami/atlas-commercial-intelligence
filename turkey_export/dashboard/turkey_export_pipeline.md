# Turkey Export Pipeline

Minimal decision view for the OEM Metal Components export module. Values must be supported by module records; use `UNKNOWN` when not verified.

## Discovery Engine

| Metric | Current | Target ceiling | Source / last update |
|---|---:|---:|---|
| Discovered manufacturers | 6 | 100 | `reports/R002_sprint_001_opportunity_discovery.md` |
| Validated manufacturer records | 6 | 100 | `database/turkish_manufacturers.csv` |
| PROCEED manufacturers | 5 | 20 | `database/turkish_manufacturers.csv` |
| Immediate candidates | 5 | 5 | `reports/R002_sprint_001_opportunity_discovery.md` |
| WAIT manufacturers | 1 | UNKNOWN | `database/turkish_manufacturers.csv` |
| DROP manufacturers | 0 | UNKNOWN | UNKNOWN |

- **Active vertical:** OEM Metal Components
- **Discovery decision:** PROCEED
- **Reason:** Five manufacturers pass preliminary discovery gates and 20 buyer-match opportunities were scored.
- **Next action:** Qualify Pro-Mak's mandate; capacity; certificates; export references and KION channel conflict before any buyer action.

## Current Opportunity

| Field | Value |
|---|---|
| Turkish manufacturer | Pro-Mak Automotive |
| Product category | Precision-machined serial drivetrain and industrial components |
| Export Readiness Score | 86 |
| Best target country | Germany |
| Commercial owner | UNKNOWN |
| Evidence cutoff | 2026-07-06 |
| Decision | PROCEED |

## Buyer Pipeline

| Stage | Count | Source / last update |
|---|---:|---|
| Potential foreign buyers | 10 | `database/foreign_buyers.csv` |
| Scored buyers | 10 | `database/foreign_buyers.csv` |
| Priority buyers | 5 | `reports/R002_sprint_001_opportunity_discovery.md` |
| Outreach drafts ready | 0 | UNKNOWN |
| Outreach authorized | 0 | UNKNOWN |
| Buyers contacted | 0 | UNKNOWN |
| Replies | 0 | UNKNOWN |
| Meetings booked | 0 | UNKNOWN |
| Meetings held | 0 | UNKNOWN |

## Top 5 Priority Buyers

| Priority | Buyer | Country | Buyer Fit Score | Bypass Risk | Status | Next action | Owner | Due date |
|---:|---|---|---:|---:|---|---|---|---|
| 1 | KION Group | Germany | 92 | 55 | PROCEED | Qualify Pro-Mak mandate and conflict before buyer action | UNKNOWN | UNKNOWN |
| 2 | CNH Industrial | Italy | 94 | 55 | PROCEED | Qualify ERBAB mandate; DUNS; certificates and target parts | UNKNOWN | UNKNOWN |
| 3 | GEA Group | Germany | 90 | 45 | PROCEED | Verify Kurutlu exports; capacity and tolerance envelope | UNKNOWN | UNKNOWN |
| 4 | Solaris Bus & Coach | Poland | 84 | 80 | PROCEED | Verify Ulus Poland channel conflict | UNKNOWN | UNKNOWN |
| 5 | Škoda Group | Czechia | 82 | 55 | PROCEED | Verify Girginer certificates and rail-applicable parts | UNKNOWN | UNKNOWN |

## Decision Summary

- **Turkish manufacturer summary:** Pro-Mak has 37 CNC machines plus broaching; gear; robotic feeding and European export-readiness evidence.
- **Export readiness score:** 86
- **Best target country:** Germany
- **Top 20 potential foreign buyers:** 20 manufacturer–buyer opportunities ranked in R002
- **Top 5 priority buyers:** KION; CNH Industrial; GEA; Solaris; Škoda Group
- **Outreach email drafts:** 0 — prohibited at this stage
- **Key risks:** No exact RFQ; mandate; price; capacity confirmation or protected commission terms; channel conflicts UNKNOWN
- **Next best action:** Manufacturer-side qualification of Pro-Mak for KION; no buyer contact
- **Decision:** PROCEED
