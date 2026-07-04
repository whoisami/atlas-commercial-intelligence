# Inputs — Atlas CEO

## Required inputs

- all intelligence domain reports and deltas
- all database CSVs
- dashboard/CEO_DASHBOARD.md
- workspace files
- knowledge files
- existing decisions

## Upstream agents

Read accepted reports from the agents that own the required inputs. Do not treat a DRAFT report as canonical.

## Input checks

- Confirm project and sprint scope.
- Confirm report IDs and evidence cutoff.
- Confirm canonical IDs before creating updates.
- Confirm sources are accessible and current enough for the decision.
- Record missing inputs as blockers or `UNKNOWN`; do not silently fill gaps.

