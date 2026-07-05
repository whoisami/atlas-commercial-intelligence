# Outputs — Competition Intelligence

## 1. Competition Intelligence report

Write:

`intelligence/competition/RXXX.md`

Use the next sequential report number in the competition domain.

### Required body

1. Executive Market-Entry Decision
2. Opportunity and Competitive Arena
3. Evidence Register and Method
4. Market Size, Imports and Local Production
5. Competitor, Brand and Substitute Map
6. Distributor and Representation Map
7. Pricing Pressure and Profit Pool
8. Concentration, Loyalty and Buying Behavior
9. Regional Demand
10. Barriers, Sales Cycle and Switching Costs
11. Service and Technical Support Expectations
12. Six Market-Entry Model Comparisons
13. SWOT
14. Commercial Scorecard and Atlas Score
15. Evidence Gaps, Risks and Monitoring Triggers
16. GO/WATCH/NO-GO Decision
17. Sources

### Mandatory final sections

The report must finish with:

1. Recommended Market Entry Strategy
2. Key Risks
3. Quick Wins
4. Expected Time to First Customer
5. Commercial Recommendation
6. GO / WATCH / NO-GO

## 2. Required analytical tables

- Evidence-state register
- Market-size/import/local-production bridge
- Competitor taxonomy
- Major-brand map
- Authorized distributor/representation map
- Substitute and buyer-alternative matrix
- Price-pressure and profit-pool analysis
- Concentration and loyalty evidence
- Regional demand map
- Barrier and mitigation register
- Sales-cycle and switching-cost table
- Service/support expectation table
- Six-entry-model comparison
- Evidence-linked SWOT
- Commercial scorecard
- Monitoring-trigger register

## 3. Product database update

Update:

`database/products.csv`

Preserve existing opportunity and Product Intelligence fields. Add/update competition-specific fields:

- Market-size basis and evidence state
- Import dependency
- Local manufacturing
- Major international brands
- Pricing pressure
- Market concentration
- Customer loyalty
- Typical buying behavior
- Regional demand
- Market and entry barriers
- Sales cycle
- Switching costs
- Service and technical-support expectations
- Raw and inverse burden scores
- Opportunity scores
- Competition Atlas Score
- Evidence Quality
- Recommended entry strategy
- Competition status
- Competition report ID and verification date

## 4. Manufacturer database update

Update:

`database/manufacturers.csv`

Preserve discovery and diligence fields. Add/update only competitive-market fields:

- Competitor role
- Turkey competitive presence
- Turkey channel type
- Authorized Turkey partners
- Turkey market position
- Key competitive strength
- Key competitive weakness
- Competition source report ID
- Competition verification date

Do not overwrite Manufacturer Hunter or Due Diligence scores.

## 5. Active-project update

Update:

`workspace/active_project.md`

Record:

- Product family and competition report ID
- GO/WATCH/NO-GO
- Recommended market-entry strategy
- Atlas Score and Evidence Quality
- First-entry region
- Quick wins
- Key risks
- Expected time to first customer
- Critical UNKNOWN
- Next gate and owner

## 6. CEO Dashboard update

Update only Competition Intelligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Open competitive gaps
- Strong incumbent threats
- Authorized channel conflicts
- Competition Intensity
- Entry Difficulty
- Market Attractiveness
- Differentiation Opportunity
- Profitability
- Competition Atlas Score
- Recommended Market Entry Strategy
- Quick wins
- Expected time to first customer
- Critical UNKNOWN
- Source report and verification date

Do not modify another agent's metrics.

## Status effect

- **GO:** eligible for controlled market-entry planning.
- **WATCH:** execute only the named market validation.
- **NO-GO:** stop entry work unless the review trigger occurs.

No output authorizes contact, inventory, spending, exclusivity or agreement.

