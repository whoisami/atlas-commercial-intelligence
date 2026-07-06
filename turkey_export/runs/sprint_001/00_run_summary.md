# Sprint 001 — Commercial Opportunity Workflow Run

- **Workflow:** [`workflows/commercial_opportunity_workflow.md`](../../workflows/commercial_opportunity_workflow.md)
- **Sector:** OEM Metal Components
- **Evidence cutoff:** 2026-07-06
- **Run scope:** `turkey_export/runs/sprint_001/` only. No architecture change, no new specification, no new engine.

## What this run is

This run executes steps 6–7 of the workflow (CEO Decision, Daily Opportunity Feed) against the accepted, already-evidenced steps 1–5 output of Sprint 001: discovery (`discovery/discovery_engine.md`), Export Need Analyzer-equivalent manufacturer screening, Demand Signal Engine-equivalent buyer screening, matching and Opportunity Scoring, recorded in [`database/turkish_manufacturers.csv`](../../database/turkish_manufacturers.csv), [`database/foreign_buyers.csv`](../../database/foreign_buyers.csv) and [`database/opportunities.csv`](../../database/opportunities.csv), and reasoned in [`reports/R002_sprint_001_opportunity_discovery.md`](../../reports/R002_sprint_001_opportunity_discovery.md) and [`reports/R003_Discovery_Engine_v2.md`](../../reports/R003_Discovery_Engine_v2.md).

No new manufacturer, buyer or signal was discovered for this run. This run does not re-score steps 1–5; it applies [`specs/06_daily_opportunity_feed.md`](../../specs/06_daily_opportunity_feed.md) ranking and CEO-decision logic to the 20 accepted opportunity records.

## Vocabulary mapping

The discovery-layer engine (`discovery/discovery_engine.md`) and current CSV `decision`/`legacy_decision` fields use `PROCEED / WAIT / DROP`. The workflow specifications (`specs/01`–`04`, `06`) use `PROCEED / WATCH / DROP`. No record in this sector is disproven, so no `WAIT` record is treated as `DROP`. For this run, `WAIT` is read as `WATCH`: plausible, evidenced, not yet meeting a `PROCEED` gate. This mapping is a reading convention for this run only; it does not rewrite the CSV `decision` field.

## Deliverables in this folder

| File | Content |
|---|---|
| [`01_top20_opportunities.md`](01_top20_opportunities.md) | All 20 accepted opportunities, ranked |
| [`02_top5_proceed.md`](02_top5_proceed.md) | `PROCEED` gate applied to the top 5; result and reasoning |
| [`03_top1_recommendation.md`](03_top1_recommendation.md) | CEO recommendation for the single top candidate |
| [`04_30day_action_plan.md`](04_30day_action_plan.md) | Bounded verification plan, 2026-07-06 to 2026-08-05 |
| [`05_evidence_log.md`](05_evidence_log.md) | Source classes, evidence states and unresolved gaps by opportunity |

## Headline result

0 of 20 opportunities meet the `specs/04_opportunity_scoring.md` `PROCEED` gate (score ≥80, Verification Confidence ≥70). The top-ranked opportunity, ERBAB → CNH Industrial (score 77), is closest but fails on Verification Confidence (65 <70). No opportunity is `DROP`. This run authorizes no outreach, CRM activity, quotation or commitment — only the named verification actions in the 30-day plan.

## Database and dashboard impact

No row in `database/turkish_manufacturers.csv`, `database/foreign_buyers.csv` or `database/opportunities.csv` changes: no new entity was discovered and no score changed. `dashboard/turkey_export_pipeline.md` gains one pointer line to this run; its decision, scores and next action are unchanged because this run reached the same conclusion by different means (formal feed ranking vs. discovery-engine migration).
