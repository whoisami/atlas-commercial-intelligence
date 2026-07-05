# Outputs — Pricing Intelligence

## 1. Pricing Intelligence report

Write:

`intelligence/pricing/RXXX.md`

Use the next sequential report number in the pricing domain.

### Required body

1. Executive Financial Decision
2. Opportunity and Scope
3. Product, Quantity and Commercial Basis
4. Price Evidence Register
5. Price Normalization
6. GTIP/HS, Customs and Import Assumptions
7. Landed-Cost Bridge
8. Turkey Market, Distributor and Competitor Prices
9. Project and Repeat-Order Economics
10. Operating-Cost and Net-Margin Analysis
11. Cash Flow, Inventory and Working Capital
12. Currency and Price-Volatility Analysis
13. Five Commercial Model Comparisons
14. Base, Downside and Upside Scenarios
15. Commercial Scorecard and Atlas Score
16. Evidence Gaps and Verification Plan
17. GO/WATCH/NO-GO Decision
18. Sources

### Mandatory final sections

The report must finish with:

1. Recommended Commercial Model
2. Expected First Revenue Timeline
3. Estimated Margin Range
4. Major Risks
5. Recommended Next Action

## 2. Required financial tables

- Evidence-status register
- Original and normalized price table
- MOQ and price-break table
- Landed-cost bridge
- Customs/GTIP assumption table
- Market/distributor/competitor comparison
- Project and repeat-order economics
- Operating-cost bridge
- Gross-to-net margin bridge
- Cash-flow timeline
- Inventory and working-capital table
- FX and price-volatility table
- Five-model comparison
- Base/downside/upside scenarios
- Sensitivity and break-even table
- Commercial scorecard
- Verification-gap register

## 3. Canonical pricing update

Update:

`database/pricing.csv`

Preserve original observations. Do not overwrite a historical quote with a newer value; create a new observation or scenario ID when appropriate.

Record:

- Evidence state
- Specification and quantity
- Original price, currency, date, validity and Incoterm
- MOQ
- Freight and import assumptions
- GTIP/HS and customs treatment
- Market, distributor and competitor prices
- Project and repeat-order values
- Commission opportunity
- Gross and net margins
- Operating costs
- Inventory and working capital
- Currency and volatility
- Five-model viability
- Recommended commercial model
- Raw and derived scores
- Evidence Quality
- Status
- Source URLs
- Report ID and verification date

## 4. Active-project update

Update:

`workspace/active_project.md`

Record:

- Opportunity and pricing report ID
- GO/WATCH/NO-GO
- Recommended commercial model
- Expected first-revenue timeline
- Estimated margin range
- Capital and working-capital requirement
- Cash-flow risk
- Currency risk
- Major assumptions
- Critical UNKNOWN
- Next gate and owner

## 5. CEO Dashboard update

Update only Pricing Intelligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Validated pricing opportunities
- Recommended commercial model
- Expected gross-margin range
- Expected net-margin range
- Commission potential
- Capital requirement
- Working-capital requirement
- Cash Flow Strength
- Speed to Revenue
- Risk
- Atlas Score
- Evidence Quality
- Largest sensitivity
- Critical UNKNOWN
- Source report and verification date

Do not modify another agent's metrics.

## Status effect

- **GO:** eligible for controlled commercial validation and model negotiation preparation.
- **WATCH:** execute only the named quote/cost/term verification.
- **NO-GO:** stop commercial work unless the review trigger occurs.

No output authorizes a quote, purchase, inventory or commitment.

