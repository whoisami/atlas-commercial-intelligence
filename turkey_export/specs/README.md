# Turkey Export Specifications

## Purpose

This directory is the specification layer for Atlas **Turkey → World** commercial intelligence. It defines what a future Turkey Export capability must accomplish before any implementation is considered.

Specifications are commercial contracts, not engines. They describe inputs, outputs, evidence rules, scoring, decision logic and testable acceptance criteria. They must comply with [`ATLAS_RULES.md`](../ATLAS_RULES.md).

## Scope boundary

- Work here applies only to Turkey → World.
- Foreign → Turkey is stable and outside scope.
- Specifications must not implement CRM, email automation or executable engines.
- Unknown facts remain `UNKNOWN`.
- Demand is established before Turkish supply is selected.
- First-revenue probability takes priority over theoretical market size or record volume.

## Creating a specification

1. Copy [`SPEC_TEMPLATE.md`](SPEC_TEMPLATE.md).
2. Name the file `SPEC_XXX_short_name.md`, using the next unused three-digit ID.
3. Define one bounded commercial decision or capability.
4. Cite the governing demand signal, evidence inputs and commercial user.
5. Define hard gates before numeric scoring.
6. State how unknown, stale and contradictory data are handled.
7. Define what each decision authorizes and explicitly does not authorize.
8. Write observable acceptance criteria.
9. Review compliance with `ATLAS_RULES.md` before approval.

## Specification lifecycle

Use one status:

- **DRAFT:** incomplete and not approved for implementation planning.
- **REVIEW:** complete enough for commercial and evidence review.
- **APPROVED:** accepted as the authoritative requirement; implementation still requires separate authorization.
- **SUPERSEDED:** replaced by a named later specification.
- **REJECTED:** not commercially justified or incompatible with Atlas rules.

Every specification records owner, version, status, date, evidence cutoff and superseded document when applicable. Revisions must preserve decision history rather than silently changing prior requirements.

## Quality gate

A specification is ready for approval only when:

- its Purpose, Inputs, Outputs, Rules, Scoring, Decision logic and Acceptance criteria are complete;
- the demand-first logic and commercial user are explicit;
- source requirements and `UNKNOWN` handling are testable;
- scoring weights total 100 when weighted scoring is used;
- hard rejection gates cannot be bypassed by a high score;
- first-revenue probability and commercial accessibility are evaluated;
- no engine, CRM or email automation is implemented;
- no file outside `turkey_export/` must change to satisfy it.

## Current specifications

No capability specifications have been created yet.
