# Outputs — Market Opportunity

## 1. Decision report

Write:

`intelligence/market/RXXX.md`

Use the next sequential report number. The report is the audit trail for the product-family selection.

### Required report sections

1. Executive Decision
2. Scope, Constraints and Evidence Cutoff
3. Candidate Universe and Fast Rejections
4. Scoring Method
5. Product-Family Scorecard
6. Evidence by Criterion
7. Contradictions, Risks and Unknowns
8. GO/WATCH/NO-GO Decision
9. Execution Plan
10. Sources

### Required scorecard columns

- Product family
- Turkey Import Dependency
- Repeat Purchase Potential
- Technical Barrier
- Margin Potential
- Stock-Free Feasibility
- Manufacturer Availability
- Buyer Availability in Turkey
- Competition Opportunity
- Trust / Fraud Safety
- Speed to First Meeting
- Speed to First Revenue
- Atlas Score
- Evidence Quality
- Status

## 2. Canonical product updates

Update:

`database/products.csv`

Create or update one row per scored product family. Use stable product IDs, source URLs, verification date, owner and notes. The notes field must preserve criterion evidence or link to the report.

Until the canonical schema contains every criterion as a dedicated column:

- Map repeated purchase to `repeated_purchase_potential`.
- Map technical barrier to `technical_barrier_0_100`.
- Map import dependency and buyer availability into `turkey_market_relevance_0_100` with the component values stated in notes.
- Map margin to `margin_potential_0_100`.
- Store the complete 11-factor scorecard, Stock-Free score and Evidence Quality in the report and summarize them in notes.
- Store the weighted result in `atlas_score_0_100`.
- Use GO, WATCH or NO-GO in `status`.

Do not erase existing source history or unrelated records.

## 3. Active-project update

Update:

`workspace/active_project.md`

Record:

- Selected product family or leading WATCH candidate.
- Decision status.
- Atlas Score.
- Evidence Quality.
- Source report ID.
- Next execution gate.
- Assigned downstream agents.

Preserve the project objective and unrelated project history.

## 4. CEO Dashboard update

Update only Market Opportunity-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- GO product opportunities.
- Selected product family.
- Atlas Score.
- Evidence Quality.
- Primary import-dependency evidence.
- Critical unknown.
- Source report.
- Date verified.

Do not modify metrics owned by another agent.

## 5. Status meaning

- **GO:** begin manufacturer hunting, buyer mapping and pricing validation.
- **WATCH:** perform only the named verification action.
- **NO-GO:** stop work on the family unless the stated review trigger occurs.

## Quality metadata

Every output must identify project, sprint, report ID, evidence cutoff, verification date, source URLs, owner and status. All three controlled surfaces must reconcile to the report.

