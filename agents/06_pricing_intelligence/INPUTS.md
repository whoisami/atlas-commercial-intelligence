# Inputs — Pricing Intelligence

## Required inputs

- database/products.csv
- database/manufacturers.csv
- database/buyers.csv
- database/pricing.csv
- accepted quotes and public price evidence
- workspace/current_sprint.md

## Upstream agents

Read accepted reports from the agents that own the required inputs. Do not treat a DRAFT report as canonical.

## Input checks

- Confirm project and sprint scope.
- Confirm report IDs and evidence cutoff.
- Confirm canonical IDs before creating updates.
- Confirm sources are accessible and current enough for the decision.
- Record missing inputs as blockers or `UNKNOWN`; do not silently fill gaps.

