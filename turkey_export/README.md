# Turkey Export Intelligence

Independent export business-development decision module for Turkish manufacturers seeking qualified foreign buyers.

## Scope

- **Initial vertical:** OEM Metal Components only
- **Included categories:** CNC machining, sheet metal, precision machining, metal fabrication and welded assemblies
- **Initial countries:** Germany, Netherlands, Poland, Italy and Czechia
- **Purpose:** determine whether a specific Turkish manufacturer should pursue a specific foreign market and buyer set

This is not a lead-list tool. Buyer volume never substitutes for verified fit, export readiness or a clear next action.

## Workflow

1. Detect a commercial or industrial signal.
2. Resolve and multi-source verify the organization behind it.
3. Check manufacturing and export readiness.
4. Select the best target country and potential foreign buyer type.
5. Discover qualified foreign buyers or supply-chain partners.
6. Score accessibility, timing, verification and commercial value.
7. Draft outreach only after discovery authorization.
8. Track meetings and outcomes.
9. Recommend the next action and decide `PROCEED`, `WAIT` or `DROP`.

Discovery rules are in [discovery/README.md](discovery/README.md). The broader operating rules are in [playbook.md](playbook.md).

## Opportunity output

Every completed opportunity must contain:

- Turkish manufacturer summary
- Export readiness score
- Best target country
- Top 20 potential foreign buyers
- Top 5 priority buyers
- Buyer fit score
- Outreach email draft
- Key risks
- Next best action
- Decision: `PROCEED` / `WAIT` / `DROP`

## Module boundaries

- The module reads only evidence provided to it or collected for the current export opportunity.
- Unknown facts are written as `UNKNOWN`.
- No contact is sent automatically.
- No existing import-to-Turkey module or core Atlas logic is changed by this module.
## Files

- `agents/` — narrowly scoped analysis instructions
- `templates/` — reusable opportunity records
- `dashboard/turkey_export_pipeline.md` — minimal pipeline view
