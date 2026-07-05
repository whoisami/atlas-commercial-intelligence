# Outputs — Outreach Intelligence

## 1. Outreach Intelligence report

Write:

`intelligence/outreach/RXXX.md`

Use the next sequential report number in the outreach domain.

### Required body

1. Executive Meeting-Conversion Decision
2. Manufacturer, Contact and Authorization Scope
3. Evidence Classification Register
4. Manufacturer-Specific Commercial Diagnosis
5. Why Atlas / Why Türkiye / Why Now
6. Manufacturer Value Proposition
7. Turkish Customer Sales Strategy
8. Risk-Reduction and ROI Angles
9. Channel and Timing Strategy
10. Personalized Communication Assets
11. Objection Library and FAQ
12. 90-Day Pilot Proposal
13. Communication Timeline and CRM Schedule
14. Response/Meeting Probability Basis
15. Risks, Blocking Issues and Verification Gaps
16. Sources

## 2. Mandatory communication assets

Include:

- Personalized first email
- LinkedIn connection request
- LinkedIn first message
- Follow-up emails #1, #2 and #3
- Phone call script
- Meeting request
- Meeting agenda
- 90-day pilot proposal
- Manufacturer value proposition
- Customer sales strategy
- Risk-reduction message
- ROI/business-impact angle
- Manufacturer-specific positioning
- Objection handling
- FAQ
- Communication timeline
- CRM follow-up schedule

## 3. Mandatory final section

The report must finish exactly with:

## COMMERCIAL ACTION

- Recommended Next Communication
- Best Communication Channel
- Best Timing
- Expected Response Rate
- Expected Meeting Probability
- Commercial Recommendation
- Decision: GO / WATCH / NO-GO
- Confidence Score: 0–100
- Owner: Atlas
- Next Agent
- Expected Business Impact
- Blocking Issues
- Next Verification Required

## 4. Outreach database update

Update:

`database/outreach.csv`

Record:

- Manufacturer/contact/project IDs
- Relationship stage
- Personalization evidence
- Market-entry pain and motivation hypotheses
- Value proposition
- All communication assets or controlled file references
- Channel and timing
- Sequence and CRM schedule
- Objection/FAQ references
- Pilot proposal reference
- Expected response and meeting probability with evidence state
- Authorization status by step
- Sent/response dates only after authorized execution
- Response classification
- Meeting status
- Next action and due date
- Decision, confidence, blockers and verification
- Report ID and source URLs

Never mark a draft as sent.

## 5. Active-project update

Update:

`workspace/active_project.md`

Record:

- Manufacturer and contact
- Outreach report ID
- Decision and Confidence Score
- Recommended next communication
- Best channel and timing
- Authorization status
- Expected response and meeting ranges
- Blocking issues
- Next verification
- Next gate and owner

## 6. CEO Dashboard update

Update only Outreach Intelligence-owned values in:

`dashboard/CEO_DASHBOARD.md`

Required values:

- Outreach-ready contacts
- Messages awaiting authorization
- Authorized next actions
- Expected response-rate range
- Expected meeting-probability range
- Positive replies
- Meetings requested
- Meetings scheduled
- Follow-ups due
- Paused/do-not-contact accounts
- Critical blocker
- Source report and verification date

Do not modify another agent's metrics.

## Status effect

- **GO:** ready for explicit CEO/human send authorization.
- **WATCH:** perform only the named verification.
- **NO-GO:** do not contact unless the review trigger occurs.

No report or database update constitutes send authorization.

