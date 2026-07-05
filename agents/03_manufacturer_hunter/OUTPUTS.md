# Outputs — Manufacturer Hunter

## 1. Manufacturer discovery report

Write:

`intelligence/manufacturers/RXXX.md`

Use the next sequential report number in the manufacturers domain.

### Required report body

1. Executive Commercial Decision
2. Product Intelligence Handoff
3. Search Scope and Regional Coverage
4. Discovery Funnel and Rejection Summary
5. Verification Method
6. Manufacturer Master Table
7. Commercial Scorecard
8. Turkey Channel Findings
9. Risks, Unknowns and Verification Plan
10. Rejected Patterns and Companies
11. Sources

### Mandatory final sections

The report must end with these exact sections in this order:

1. Top 10 Manufacturers
2. Top 5 Priority Targets
3. Top 3 Immediate Outreach Candidates
4. Commercial Recommendation
5. Next Action

## 2. Manufacturer master table

For every evaluated company include:

- Company
- Country
- Website
- Products
- Product Families
- Manufacturer Evidence
- Factory Evidence
- Estimated Employees
- Year Founded
- Export Evidence
- Export Countries
- ISO / CE / API Certifications
- LinkedIn Company
- Export Contact
- Export Email
- Sales Email
- General Email
- Phone
- Source URLs
- Turkey Presence
- Existing Turkey Distributor
- Export Readiness
- Turkey Expansion Potential
- Communication Quality
- Technical Strength
- Commercial Fit
- Representation Potential
- Risk
- Trust
- Overall Atlas Score
- Status
- Atlas Notes

## 3. Canonical manufacturer update

Update:

`database/manufacturers.csv`

Use one stable `manufacturer_id` per legal entity. Preserve unrelated rows and prior source history. Record all mandatory fields, commercial scores, report ID, verification date and owner.

If evidence changes an existing record, update it rather than creating a duplicate. If an entity uses multiple brands, explain the relationship in notes.

## 4. Active-project update

Update:

`workspace/active_project.md`

Record:

- Product family.
- Manufacturer Hunter report ID.
- Search countries covered.
- Number evaluated.
- GO, WATCH and NO-GO counts.
- Top 10.
- Top 5.
- Top 3.
- Critical channel or trust risk.
- Next gate: Manufacturer Due Diligence.

## 5. CEO Dashboard update

Update only Manufacturer Hunter-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- GO manufacturers.
- WATCH manufacturers.
- NO-GO manufacturers.
- Manufacturers by country.
- Top 5 priority targets.
- Top 3 immediate outreach candidates.
- Visible Turkey-channel conflicts.
- Median Trust score of GO candidates.
- Median Representation Potential of GO candidates.
- Critical unknown.
- Source report and verification date.

Do not modify another agent's metrics.

## 6. Due-diligence handoff

For each Top 3 candidate provide:

- Evidence packet.
- Legal/company identity.
- Product and factory proof.
- Certification list and verification gaps.
- Export proof.
- Turkey-channel finding.
- Official contact route.
- Atlas partnership hypothesis.
- First-message angle.
- Objection hypothesis.
- Risk note.
- Exact diligence questions.

## Status effect

- **GO:** advance to Manufacturer Due Diligence and contact verification.
- **WATCH:** perform only the named verification.
- **NO-GO:** reject from priority portfolio unless the review trigger occurs.

“Immediate Outreach Candidate” is a readiness tier, not authorization to send.

