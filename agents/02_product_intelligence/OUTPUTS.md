# Outputs — Product Intelligence

## 1. Product Intelligence report

Write:

`intelligence/products/RXXX.md`

Use the next sequential report number in the products domain.

### Required sections

1. Executive Product Decision
2. Market Opportunity Handoff
3. Product Definition and Structure
4. Variant and Specification Matrix
5. Applications and Industry Map
6. Certification, Regulation and GTIP/HS
7. Buying Center and Purchase Journey
8. OEM, Project and Aftermarket Model
9. Maintenance, Replacement and Repeat Purchase
10. Order Size, MOQ, Stock and Logistics
11. Installation, Training and Remote Support
12. Complementary and Competing Technologies
13. Product Lifecycle and Value Proposition
14. Nine-Dimension Scorecard and Commercial Product Fit
15. Technical Risks, Unknowns and Verification Plan
16. Manufacturer Research Requirements
17. Sources
18. Final Decision and Commercial Recommendation

The report must end with exactly one of:

- GO
- WATCH
- NO-GO

followed by a direct commercial recommendation.

## 2. Required product artifacts inside the report

- Product architecture.
- Terminology and boundary table.
- Variant matrix.
- Minimum specification/datasheet fields.
- Application-to-variant map.
- Certification and regulatory matrix.
- GTIP/HS candidate table with confidence and verification route.
- Buying-center map.
- OEM versus aftermarket comparison.
- Maintenance and repeat-purchase model.
- Order, MOQ and stock logic.
- Installation and support model.
- Complementary and competing-technology map.
- Lifecycle and value-proposition map.
- Nine raw scores and Commercial Product Fit.
- Manufacturer-search inclusion and exclusion criteria.

## 3. Canonical product update

Update:

`database/products.csv`

Preserve stable IDs and unrelated records. Update the selected product-family row with:

- Technical description.
- GTIP/HS candidate and uncertainty.
- Applications.
- Target industries.
- Repeat-purchase assessment.
- Technical-barrier score.
- Margin-potential score.
- Product-readiness status.
- Source URLs.
- Verification date.
- Owner.
- Notes linking to the full nine-factor scorecard and report ID.

Do not force details into unsuitable columns. Keep the complete model in the report and summarize only traceable values in the canonical row.

## 4. Active-project update

Update:

`workspace/active_project.md`

Record:

- Selected product family.
- Product Intelligence report ID.
- Product-readiness status.
- Commercial Product Fit.
- Stock-free conclusion.
- Remote-support conclusion.
- Critical unknown.
- Next gate.
- Manufacturer Hunter handoff status.

## 5. CEO Dashboard update

Update only Product Intelligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Qualified products.
- Selected product family.
- Product-readiness status.
- Commercial Product Fit.
- Technical Complexity.
- Repeat Purchase.
- Stock Requirement.
- Certification Requirement.
- GTIP/HS confidence.
- Critical product unknown.
- Source report and verification date.

Do not change another agent's metrics.

## 6. Manufacturer Hunter handoff

A GO report must provide:

- Product scope.
- Required variants.
- Must-have specification capabilities.
- Required certifications and documentation.
- Application sectors.
- OEM/aftermarket priority.
- Stock and lead-time requirements.
- Remote-support expectations.
- Excluded product types.
- Open verification questions.

Manufacturer Hunter must not need to infer these requirements.

## Status effect

- **GO:** manufacturer research may begin.
- **WATCH:** only the named product-verification tasks may continue.
- **NO-GO:** manufacturer research stops unless the review trigger occurs.

All outputs must cite the report ID and agree with the final status.

