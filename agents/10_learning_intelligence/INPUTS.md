# Inputs — Learning Intelligence

## Activity and outcome inputs

- manufacturer outreach records, replies and verified non-replies;
- meeting records and approved notes;
- buyer conversations and objections;
- negotiation and quotation records;
- pilot, order, commission and repeat-order records;
- closed-lost and stopped-opportunity reasons;
- accepted intelligence reports and commercial research;
- prior decisions, predictions, scores and action plans;
- current and previous sprint records;
- current knowledge registers and playbooks.

## Canonical repository inputs

- `database/outreach.csv`
- `database/meetings.csv`
- `database/decisions.csv`
- other relevant `database/*.csv` files
- `intelligence/**/RXXX.md`
- `decisions/DECISION_XXX.md`
- `workspace/active_project.md`
- `workspace/current_sprint.md`
- `dashboard/CEO_DASHBOARD.md`
- `knowledge/*.md`
- `playbooks/*.md`

## Minimum review packet

A valid review needs:

- a stable activity or cohort identifier;
- an activity date and evidence cutoff;
- the original action or prediction;
- the observed outcome or explicit `UNKNOWN`;
- source record references;
- enough denominator data for any reported conversion metric.

## Input validation

- Confirm records belong to the same entity, campaign and period.
- Deduplicate people, activities and outcomes.
- Separate sent, delivered, bounced, replied and qualified events.
- Separate scheduled from held meetings.
- Separate draft quotations from issued quotations and issued quotations from orders.
- Confirm monetary values, currency and tax treatment before comparing pricing.
- Exclude open opportunities from closed-outcome claims unless explicitly described.
- Treat recollection as HYPOTHESIS until corroborated.
- Record inaccessible, stale or contradictory inputs as limitations.

## Privacy and integrity

Use only authorized records and public information. Prefer stable IDs and sanitized summaries over copying personal messages. Never infer protected traits, motives or country stereotypes from commercial behavior.

