# Reporting and Naming Standard

## Sequential names

Each intelligence domain uses an independent report sequence:

- `R001.md`
- `R002.md`
- `R003.md`

Never reuse or overwrite a completed report number. Corrections are a new report that references the superseded report.

## Required report front matter

Every report starts with:

- Report ID
- Agent
- Project
- Sprint
- Date
- Decision requested
- Status: DRAFT / READY_FOR_CEO / ACCEPTED / SUPERSEDED
- Evidence cutoff

## Required body

1. Executive Summary
2. Scope and Question
3. Evidence and Findings
4. Commercial Interpretation
5. Risks and Unknowns
6. GO/WATCH/NO-GO Recommendation
7. Next Actions
8. Sources

## CSV delta names

Use `R###_<table>_delta.csv`, stored beside the report. A delta must use the canonical database schema plus:

- `change_type`: INSERT / UPDATE / NO_CHANGE
- `changed_fields`
- `report_id`

## Source format

Use direct URLs or repository-relative file links. Record source owner, page title, evidence level, accessed date and the claim supported. Search-result pages are not sources.

