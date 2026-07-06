# SPEC_XXX — Specification Title

## Specification control

| Field | Value |
|---|---|
| Specification ID | SPEC_XXX |
| Version | 0.1 |
| Status | DRAFT |
| Owner | UNKNOWN |
| Created | YYYY-MM-DD |
| Last updated | YYYY-MM-DD |
| Evidence cutoff | UNKNOWN |
| Related opportunity | UNKNOWN |
| Supersedes | NONE |

## Purpose

### Commercial problem

Describe the single Turkey → World commercial problem this specification addresses.

### Decision supported

State the exact decision the capability must support and who uses that decision.

### Expected commercial value

Explain how the capability could improve commercial accessibility, speed to first revenue or first-revenue probability. Do not use unsupported market values.

### In scope

- UNKNOWN

### Out of scope

- Foreign → Turkey changes
- CRM functionality
- Email sending or outreach automation
- Executable engine implementation
- UNKNOWN

## Inputs

Define each required input and its evidence standard.

| Input | Purpose | Required fields | Accepted evidence | Freshness | Required / Optional | Unknown handling |
|---|---|---|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | Write `UNKNOWN`; define verification action |

### Input validation

- Define identity and entity-resolution checks.
- Define duplicate, stale and contradictory-data handling.
- Define the minimum evidence required before processing.
- Define prohibited or unauthorized inputs.

## Outputs

Define decision-ready outputs, not document volume.

| Output | Commercial user | Required fields | Evidence traceability | Authorized next action |
|---|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | Source or record ID required | UNKNOWN |

### Output states

State how VERIFIED, ESTIMATED, HYPOTHESIS and UNKNOWN values are represented when applicable.

### Non-authorization statement

State what the output does not authorize, including automatic contact, email sending, purchasing, quotation, representation, exclusivity or other commercial commitment.

## Rules

### Governing rules

- Comply with [`ATLAS_RULES.md`](../ATLAS_RULES.md).
- Turkey → World only.
- Demand first; supply follows verified demand.
- No invented data.
- Commercial accessibility and first-revenue probability must be evaluated.

### Hard gates

List mandatory conditions that no numeric score may override.

| Gate | Pass condition | Failure decision | Evidence required |
|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

### Exclusion rules

- UNKNOWN

### Stop rules

Define when research or processing must stop because a decision is ready, evidence is insufficient, risk is unacceptable or expected commercial value no longer justifies work.

## Scoring

Use scoring only when it improves the commercial decision. If weighted scoring is used, weights must total 100.

| Factor | Definition | Score range | Weight | Evidence requirement |
|---|---|---:|---:|---|
| Demand strength and timing | UNKNOWN | 0–100 | UNKNOWN | UNKNOWN |
| Turkish supply fit | UNKNOWN | 0–100 | UNKNOWN | UNKNOWN |
| Commercial accessibility | UNKNOWN | 0–100 | UNKNOWN | UNKNOWN |
| First-revenue probability | UNKNOWN | 0–100 | UNKNOWN | UNKNOWN |

### Calculation

Define the formula, rounding, missing-value treatment and whether any risk scores are inverted. Never award points for `UNKNOWN` evidence unless the specification explicitly defines and justifies a conservative rule.

### Score interpretation

| Range | Meaning | Permitted action |
|---:|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN |

## Decision logic

Define the exact decision vocabulary used by this specification.

### Positive decision

- Required hard gates: UNKNOWN
- Minimum score or evidence: UNKNOWN
- Action authorized: UNKNOWN
- Action not authorized: UNKNOWN

### Conditional decision

- Missing or contradictory evidence: UNKNOWN
- Verification owner: UNKNOWN
- Review trigger and deadline: UNKNOWN
- Action authorized while waiting: UNKNOWN

### Negative decision

- Rejection conditions: UNKNOWN
- Closure record required: UNKNOWN
- Re-entry condition, if any: UNKNOWN

### Decision precedence

State that hard identity, evidence, legal, sanctions, authorization and commercial-access failures override numeric scores.

## Acceptance criteria

Write observable pass/fail criteria. Replace or extend the examples below.

- [ ] The specification applies only to Turkey → World.
- [ ] Foreign → Turkey requires no modification.
- [ ] The commercial decision and user are explicit.
- [ ] Demand evidence is required before supply selection.
- [ ] Every material output is traceable to evidence.
- [ ] Missing evidence produces `UNKNOWN`, not an invented value.
- [ ] Hard gates cannot be overridden by scoring.
- [ ] Scoring weights total 100, or the specification explains why no weighted score is used.
- [ ] Commercial accessibility is explicitly evaluated.
- [ ] First-revenue probability is explicitly evaluated.
- [ ] Every decision states the next action it authorizes.
- [ ] The capability does not implement CRM or email automation.
- [ ] No executable engine is included.
- [ ] Privacy, authorization and source restrictions are testable.
- [ ] Stop conditions prevent indefinite research.

## Open questions

| Question | Decision impact | Verification owner | Due date |
|---|---|---|---|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Change history

| Version | Date | Change | Reason | Owner |
|---|---|---|---|---|
| 0.1 | YYYY-MM-DD | Initial draft | UNKNOWN | UNKNOWN |
