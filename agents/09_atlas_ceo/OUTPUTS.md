# Outputs — Atlas CEO

## 1. Binding decision

Write:

`decisions/DECISION_XXX.md`

Use the next sequential number. Only Atlas CEO creates or supersedes decision files.

### Required decision body

1. Decision Summary
2. Opportunity and Stage
3. Should Atlas Pursue? YES / NO
4. Evidence Reviewed
5. Evidence Conflicts and Unknowns
6. Expected Business Value
7. Probability and Timing
8. Commercial Model
9. Resource Allocation
10. TOP 3 PRIORITIES
11. TOP 3 RISKS
12. TOP 3 OPPORTUNITIES
13. NEXT COMMERCIAL ACTIONS
14. Kill Rule and Review Trigger
15. Actions Authorized
16. Actions Not Authorized
17. Dashboard and Workspace Changes
18. Source Reports

### Required final block

Every decision must finish with:

## FINAL DECISION

- GO / WATCH / NO-GO
- Confidence Score
- Commercial Impact
- Expected Revenue Impact
- Expected Time To First Revenue
- Owner
- Next Action
- Blocking Issues

## 2. CEO Dashboard

Update:

`dashboard/CEO_DASHBOARD.md`

Maintain:

- Commercial funnel
- Manufacturer meetings
- Manufacturer response rate
- Buyer conversations
- Pilot projects
- Quotations
- Orders
- Revenue
- Commission earned
- Recurring revenue
- Current decisions
- TOP 3 priorities
- TOP 3 risks
- TOP 3 opportunities
- Resource allocation
- Weekly targets
- Critical unknowns
- Agent delivery status

Every value cites an accepted report, decision or internal outcome. Use UNKNOWN rather than invented targets or results.

## 3. Active project

Update:

`workspace/active_project.md`

Record:

- Binding decision ID
- Pursue YES/NO
- GO/WATCH/NO-GO
- Primary opportunity
- Commercial model
- Current milestone
- Resource caps
- Owner
- Next action
- Deadline
- Review trigger
- Kill trigger
- Expected time to first meeting/revenue
- Blocking issues

## 4. Current sprint

Update:

`workspace/current_sprint.md`

Record:

- Sprint objective
- Weekly commercial targets
- Maximum manufacturers to contact
- Maximum buyers to approach
- Priority order
- Authorized actions
- Explicitly prohibited actions
- Completion evidence
- Review date
- Kill criteria

## 5. Next actions

Update `workspace/next_actions.md` whenever owners, dates or priorities change.

Every action includes owner, due date, completion evidence and decision impact.

## 6. Decision registry

Register the binding decision in `database/decisions.csv` when required by Atlas governance. The Markdown decision remains the authoritative rationale.

## Status effect

- **GO:** YES; execute only authorized action.
- **WATCH:** NO for now; execute only verification.
- **NO-GO:** NO; kill/release resources.

All operating surfaces must reconcile.

