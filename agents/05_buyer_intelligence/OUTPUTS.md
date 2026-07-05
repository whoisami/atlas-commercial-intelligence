# Outputs — Buyer Intelligence

## 1. Buyer Intelligence report

Write:

`intelligence/buyers/RXXX.md`

Use the next sequential report number in the buyers domain.

### Required report body

1. Executive Demand Decision
2. Market and Product Intelligence Handoff
3. Ideal Customer Profile and Buyer Types
4. Search Scope, Sources and Coverage
5. Demand-Signal Method
6. Qualified Buyer Master Table
7. Buying-Center and Purchase-Route Analysis
8. Commercial Scorecard
9. Demand Concentration by Industry, City and Buyer Type
10. Verification Gaps, Risks and Unknowns
11. Rejected Patterns and Accounts
12. Sources

### Mandatory final sections

The report must end with these exact sections in order:

1. Top 100 Buyers
2. Top 25 Priority Buyers
3. Top 10 Immediate Targets
4. Recommended First Contact Strategy
5. Commercial Recommendation
6. Next Action

If fewer accounts qualify, state the verified count and reason. Do not pad.

## 2. Qualified buyer master table

For each evaluated account include:

- Company Name
- Industry
- City
- Website
- Buyer Type
- Potential Product Need
- Reason They May Buy
- Demand Classification
- Purchase Trigger
- Estimated Purchase Frequency
- Decision Maker Department
- Purchasing Contact, if public
- LinkedIn
- Email, if public
- Phone
- Need Score
- Buying Probability
- Repeat Purchase Potential
- Strategic Importance
- Ease of Contact
- Market Influence
- Priority Score
- Evidence Quality
- Status
- Source URLs
- Atlas Notes

## 3. Canonical buyer update

Update:

`database/buyers.csv`

Use a stable `buyer_id` for each legal entity or clearly identified facility, according to the database convention. Preserve unrelated records and source history.

Record all mandatory fields, demand classification, commercial scores, report ID, verification date and owner. Explain parent/facility relationships in notes.

## 4. Active-project update

Update:

`workspace/active_project.md`

Record:

- Product family
- Buyer Intelligence report ID
- Search coverage
- Qualified buyer count
- GO, WATCH and NO-GO counts
- Top 25
- Top 10
- Highest-confidence demand signals
- Critical buyer unknown
- Manufacturer-value narrative
- Next gate and owner

## 5. CEO Dashboard update

Update only Buyer Intelligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Qualified buyers
- GO buyers
- WATCH buyers
- NO-GO buyers
- Buyers by industry
- Buyers by city
- Buyers by buyer type
- Top 25 priority buyers
- Top 10 immediate targets
- Verified demand versus strong hypothesis counts
- Buying-center gaps
- Critical buyer unknown
- Source report and verification date

Do not modify another agent's metrics.

## 6. Contact-strategy handoff

For each Top 10 account provide:

- Company and facility
- Buyer type
- Need hypothesis and evidence
- Purchase trigger
- Department to approach
- Public contact route
- First-message problem/value angle
- Technical proof needed
- Unknowns and risk
- Exact next verification

Top 10 status does not authorize contact.

## Status effect

- **GO:** eligible for contact enrichment and message planning.
- **WATCH:** execute only the named verification.
- **NO-GO:** remove from active pipeline unless the review trigger occurs.

All outputs must cite the report ID and agree with the final account statuses.

