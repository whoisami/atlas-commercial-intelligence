# Top 20 Opportunities — OEM Metal Components

Per [`specs/06_daily_opportunity_feed.md`](../../specs/06_daily_opportunity_feed.md) ranking: decision class, then Atlas Opportunity Score, then Verification Confidence, then Accessibility, then Execution Speed, then stable ID. Source: [`database/opportunities.csv`](../../database/opportunities.csv), evidence cutoff 2026-07-06. Eligible: score ≥50 and status `PROCEED` or `WATCH` (read from `WAIT`); none excluded — 20 of 20 candidate records qualify, none is `DROP`.

| Rank | Turkish manufacturer | Foreign buyer | Country | Score | Verif. | Access. | Signal | Speed | Status |
|---:|---|---|---|---:|---:|---:|---:|---:|---|
| 1 | ERBAB Otomat | CNH Industrial N.V. | Italy | 77 | 65 | 80 | 55 | 65 | WATCH |
| 2 | ERBAB Otomat | KION Group AG | Germany | 75 | 62 | 78 | 45 | 70 | WATCH |
| 3 | Pro-Mak Automotive | CNH Industrial N.V. | Italy | 74 | 62 | 80 | 55 | 65 | WATCH |
| 4 | Pro-Mak Automotive | GEA Group AG | Germany | 73 | 60 | 82 | 50 | 70 | WATCH |
| 5 | Pro-Mak Automotive | KION Group AG | Germany | 73 | 60 | 78 | 45 | 70 | WATCH |
| 6 | Kurutlu Technologies | GEA Group AG | Germany | 71 | 60 | 82 | 50 | 70 | WATCH |
| 7 | ERBAB Otomat | Solaris Bus & Coach | Poland | 71 | 60 | 60 | 55 | 50 | WATCH |
| 8 | Ulus Metal | Škoda Group a.s. | Czechia | 69 | 55 | 55 | 80 | 45 | WATCH |
| 9 | Girginer Oto Endüstri | Škoda Group a.s. | Czechia | 69 | 52 | 55 | 80 | 45 | WATCH |
| 10 | Kurutlu Technologies | Krones AG | Germany | 68 | 60 | 75 | 45 | 65 | WATCH |
| 11 | Pro-Mak Automotive | Lely Industries N.V. | Netherlands | 68 | 58 | 65 | 50 | 55 | WATCH |
| 12 | Ulus Metal | Solaris Bus & Coach | Poland | 67 | 52 | 60 | 55 | 50 | WATCH |
| 13 | Kurutlu Technologies | Lely Industries N.V. | Netherlands | 65 | 58 | 65 | 50 | 55 | WATCH |
| 14 | ERBAB Otomat | VDL Groep B.V. | Netherlands | 64 | 58 | 45 | 40 | 40 | WATCH |
| 15 | Smartist Industrial Solutions | GEA Group AG | Germany | 64 | 55 | 82 | 50 | 70 | WATCH |
| 16 | Smartist Industrial Solutions | Krones AG | Germany | 63 | 55 | 75 | 45 | 65 | WATCH |
| 17 | Kurutlu Technologies | Danieli & C. | Italy | 62 | 58 | 65 | 40 | 45 | WATCH |
| 18 | Girginer Oto Endüstri | VDL Groep B.V. | Netherlands | 59 | 48 | 45 | 40 | 40 | WATCH |
| 19 | Kurutlu Technologies | IMA S.p.A. | Italy | 56 | 58 | 40 | 35 | 35 | WATCH |
| 20 | Smartist Industrial Solutions | IMA S.p.A. | Italy | 51 | 52 | 40 | 35 | 35 | WATCH |

## Reading notes

- Scores are `ESTIMATED` from Sprint 001 evidence per `database/opportunities.csv` and `reports/R003_Discovery_Engine_v2.md`; no score was recalculated in this run.
- Every row's `WATCH` status reflects manufacturer- and buyer-side evidence still concentrated in official/company-controlled sources, below the two-independent-source-class verification bar in `discovery/discovery_engine.md`.
- No row is `PROCEED`: none reaches Atlas Opportunity Score ≥80 with Verification Confidence ≥70 (`specs/04_opportunity_scoring.md`).
- No row is `DROP`: no manufacturer, buyer or match has been disproven.
- This is a maximum list, not a padded one — 20 of 20 candidate opportunity records in the sector qualify for the Top 20 by the score ≥50 floor.
