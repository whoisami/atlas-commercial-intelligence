# SOP — Learning Intelligence

## 1. Establish the learning review

1. Select a completed action, cohort, sprint or commercial milestone.
2. Define the evidence cutoff, review question and decision the learning may change.
3. Identify the original prediction, intended audience, owner and expected outcome.
4. Confirm that an outcome was actually recorded. If not, classify it `UNKNOWN`; do not infer success or failure.

## 2. Build the evidence ledger

For every input, record source path or URL, record ID, activity date, verification date, evidence state and limitation. Prefer CRM/outreach records, meeting notes, quotations, order records, accepted reports and dated decisions over recollection.

Reconcile duplicate events, bounced messages, test records, reopened opportunities and missing timestamps before calculating metrics.

## 3. Reconstruct expected versus observed

Document:

- action and commercial hypothesis;
- expected response, meeting, proposal, order, commission or repeat outcome;
- observed outcome and elapsed time;
- audience, country, industry, product family, channel, message version and commercial model;
- deviations from the intended process.

Do not backfill an expectation after the outcome is known.

## 4. Calculate funnel and speed metrics

Use cohort-consistent definitions:

- **Response rate:** unique contacts with a human reply / unique valid contacts reached.
- **Meeting conversion:** held qualified meetings / unique valid contacts reached. Also disclose scheduled meetings separately.
- **Proposal conversion:** issued proposals or quotations / held qualified meetings.
- **Order conversion:** confirmed orders / issued proposals or quotations.
- **Commission conversion:** commission-bearing orders / confirmed orders eligible for commission.
- **Repeat business:** customers with a subsequent paid order / customers eligible to reorder during the observation window.
- **Average sales cycle:** mean days from first authorized contact to confirmed order, closed-won records only; disclose median when sample permits.
- **Average response time:** mean elapsed business time from first valid contact to first human response among responders.

Always disclose numerator, denominator, cohort dates, exclusions and open-record treatment. Use `UNKNOWN` when the denominator is not reliable.

## 5. Diagnose the outcome

1. Identify candidate drivers across message, channel, timing, fit, stakeholder, offer, objection, price, trust, technical support and process execution.
2. Seek contradictory cases and alternative explanations.
3. Separate controllable process defects from market signals.
4. Scope country and industry observations to the actual cohort; never convert them into stereotypes.
5. Distinguish correlation from demonstrated causation.

## 6. Create and score lessons

Create one lesson per actionable observation using the mandatory schema in `PROMPT.md`. Score confidence factor by factor. Assign maturity: ONE-CASE, EMERGING, VALIDATED or RETIRED.

Merge duplicates by stable Lesson ID. Preserve prior wording and append a dated revision trail when confidence, scope or status changes.

## 7. Update knowledge registers

- Put durable lessons in `knowledge/lessons_learned.md`.
- Put repeatable cross-case signals in `knowledge/commercial_patterns.md`.
- Put evidenced winning outreach in `knowledge/successful_outreach.md`.
- Put evidenced failed outreach in `knowledge/failed_outreach.md`.
- Put price, margin, quotation and negotiation signals in `knowledge/pricing_patterns.md`.

Do not duplicate full personal correspondence. Store a sanitized observation and canonical evidence reference.

## 8. Decide playbook changes

For each candidate change define current rule, proposed rule, evidence, affected scope, expected impact, owner, test window, success metric, review trigger and rollback condition.

- GO: update the relevant playbook and its change log.
- WATCH: record a bounded experiment; do not replace the current standard.
- NO-GO: retain the current standard and record why.

Changes to another agent's mandate, schema, authority or scoring remain recommendations for Atlas CEO.

## 9. Write and synchronize outputs

1. Write `intelligence/learning/RXXX.md`.
2. Update the relevant knowledge registers.
3. Update only Learning-owned values in `dashboard/CEO_DASHBOARD.md`, citing the report.
4. Append the execution summary to `workspace/current_sprint.md` without overwriting sprint scope.
5. Confirm all required closing sections and the final `COMMERCIAL ACTION` block exist.

## 10. Validate

- Validate Markdown structure and internal links.
- Recalculate every rate and score.
- Confirm every material lesson has evidence and a date.
- Confirm `UNKNOWN` replaces unsupported values.
- Confirm no private data was copied unnecessarily.
- Confirm no other agent was modified.

## Stop and escalation rules

Stop and escalate when evidence indicates legal, sanctions, privacy, fraud or material reputation risk; when records conflict on a decisive outcome; or when the requested change exceeds Learning authority.

Stop analysis once one evidence-backed improvement is ready for action or one bounded test can resolve the decisive uncertainty.

