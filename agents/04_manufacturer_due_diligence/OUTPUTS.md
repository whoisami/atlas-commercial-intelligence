# Outputs — Manufacturer Due Diligence

## 1. Due-diligence report

Write:

`intelligence/manufacturers/RXXX.md`

Use the next sequential report number in the shared manufacturer-intelligence domain.

### Required sections

1. Executive Risk Decision
2. Scope, Candidate and Intended Contact Action
3. Manufacturer Hunter Handoff Audit
4. Corporate Identity, Ownership and Legal Existence
5. Manufacturing, Factory and Product Consistency
6. Export Capability and International Commercial Evidence
7. Financial Credibility and Commercial Stability
8. Certifications and Quality Systems
9. Contacts, Response Channels and Export Department
10. Turkey Presence and Channel Conflict
11. Sanctions, Trade Restrictions and Reputation
12. Nine-Risk Scorecard
13. Verification Gaps and Required Controls
14. Sources
15. Final GO/WATCH/NO-GO Decision

### Mandatory closing fields

Every report must finish with:

- **Commercial Recommendation**
- **Recommended Next Action**
- **Owner**
- **Priority**
- **Expected Business Impact**
- **Risk if Ignored**

No field may be omitted. Use `UNKNOWN` when necessary and explain why.

## 2. Evidence and risk tables

The report must include:

- Entity-resolution table
- Manufacturer/factory verification table
- Product-consistency table
- Certification register
- Export/customer/market evidence table
- Financial-credibility evidence and proxy table
- Contact and response-channel table
- Turkey-channel evidence table
- Sanctions/trade-screening log
- Adverse-reputation log
- Verification-gap register
- Risk-control register
- Nine raw risk scores
- Overall Due Diligence Risk
- Evidence Quality
- Final status

## 3. Canonical manufacturer update

Update:

`database/manufacturers.csv`

Preserve the Manufacturer Hunter record and add/update:

- Legal-existence status
- Ownership
- Financial credibility
- International customers
- Website quality
- LinkedIn presence
- Response channels
- Export department
- Contact quality
- Potential channel conflict
- Sanctions-screening status
- Trade restrictions
- Reputation evidence
- Product consistency
- Commercial stability
- Nine risk scores
- Overall Due Diligence Risk
- Evidence Quality
- Diligence status
- Diligence report ID
- Last diligence date
- Required controls and verification gaps in notes

Do not overwrite discovery scores with due-diligence risk scores.

## 4. Active-project update

Update:

`workspace/active_project.md`

Record:

- Manufacturer ID and company
- Due-diligence report ID
- GO/WATCH/NO-GO
- Overall Due Diligence Risk
- Evidence Quality
- Turkey-channel status
- Sanctions/trade status
- Required controls
- Verification gaps
- Contact-preparation status
- Next gate and owner

## 5. CEO Dashboard update

Update only Manufacturer Due Diligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Manufacturers due-diligence cleared
- WATCH cases
- NO-GO cases
- Average Overall Due Diligence Risk
- Critical diligence blockers
- Unresolved sanctions/trade checks
- Certificates requiring verification
- Channel status confirmations
- Contact-ready manufacturers
- Source report and verification date

Do not modify another agent's values.

## 6. Commercial-action effect

- **GO:** route to Atlas CEO and Outreach Intelligence for controlled contact preparation.
- **WATCH:** execute only the named verification plan.
- **NO-GO:** block contact and preserve the rejection evidence.

GO does not authorize contact by itself.

## Quality metadata

Every output includes project, sprint, candidate ID, legal entity, report ID, evidence cutoff, verification date, analyst/agent owner, sources, limitations and status.

