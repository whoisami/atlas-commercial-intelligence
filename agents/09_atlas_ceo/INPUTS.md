# Inputs — Atlas CEO

## Accepted intelligence reports

Read relevant accepted outputs from:

1. `intelligence/market/` — Market Opportunity
2. `intelligence/products/` — Product Intelligence
3. `intelligence/manufacturers/` — Manufacturer Hunter
4. `intelligence/manufacturers/` — Manufacturer Due Diligence
5. `intelligence/buyers/` — Buyer Intelligence
6. `intelligence/pricing/` — Pricing Intelligence
7. `intelligence/competition/` — Competition Intelligence
8. `intelligence/outreach/` — Outreach Intelligence

Do not read external sources to supplement them. Return evidence gaps to the responsible agent.

## Canonical databases

Read all relevant CSVs:

- `database/products.csv`
- `database/manufacturers.csv`
- `database/buyers.csv`
- `database/pricing.csv`
- `database/contacts.csv`
- `database/outreach.csv`
- `database/meetings.csv`
- `database/decisions.csv`

Canonical tables support decision consistency; accepted reports remain the evidence narrative.

## Operating state

Read:

- `dashboard/CEO_DASHBOARD.md`
- `workspace/active_project.md`
- `workspace/current_sprint.md`
- `workspace/next_actions.md`
- Existing `decisions/DECISION_XXX.md`
- Relevant `knowledge/lessons_learned.md`
- Relevant `knowledge/commercial_patterns.md`

## Mandatory decision inputs

Obtain from accepted internal evidence or mark UNKNOWN:

- Opportunity and stage
- Product family
- Manufacturer target
- Buyer demand
- Commercial model
- Margin/commission economics
- Capital and working-capital need
- Competition and differentiation
- Manufacturer meeting probability
- Time to first meeting
- First-revenue probability
- Time to first revenue
- Major risks and blockers
- Resource capacity
- Current authorizations
- Kill trigger

## Input acceptance rules

- DRAFT reports are not decision evidence.
- Conflicting accepted outputs must be reconciled or cause WATCH.
- Stale evidence must be returned for refresh; CEO does not refresh it.
- Missing probability/revenue/timing is UNKNOWN, never invented.
- External facts not saved by an agent are out of scope.
- Prior decisions remain binding until superseded.

## No-research control

Before deciding, confirm:

- No web search was performed.
- No external source was opened.
- No new market/company/contact fact was created.
- Every factual statement traces to an accepted report, canonical record or internal outcome.

