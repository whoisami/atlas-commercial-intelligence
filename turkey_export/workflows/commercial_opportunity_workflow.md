# Commercial Opportunity Workflow

## Purpose

Define the fixed execution order that carries a Turkey → World commercial opportunity from discovery to the CEO's daily feed. This document sequences existing specifications; it defines no new logic, engine, scoring or automation. Each step is governed by its own specification and must satisfy that specification's gates before the next step may consume its output.

## Scope

Applies only to Turkey → World. Foreign → Turkey is out of scope. This workflow implements nothing: no scheduler, no CRM, no email automation, no dashboard logic. It states order and hand-off conditions only.

## Execution order

### 1. Discover company

Source: [`discovery/discovery_engine.md`](../discovery/discovery_engine.md)

Identify a candidate Turkish manufacturer or foreign buyer signal from public and industrial sources. Output is an unverified candidate entity with source references — not a demand claim, not a match, not a score.

**Hand-off condition:** candidate has a resolvable identity and at least one traceable source. Otherwise it does not proceed.

### 2. Export Need Analyzer

Source: [`specs/01_export_need_analyzer.md`](../specs/01_export_need_analyzer.md)

Evaluate whether the discovered entity has a genuine, evidenced export need or export capability, applying hard gates before any scoring.

**Hand-off condition:** `PROCEED` or `WATCH`. `DROP` ends the workflow for this candidate.

### 3. Demand Signal Engine

Source: [`specs/02_demand_signal_engine.md`](../specs/02_demand_signal_engine.md)

Evaluate evidence of foreign industrial demand independent of any specific Turkish supplier. Demand is established before supply is selected.

**Hand-off condition:** `PROCEED` or `WATCH` demand signal, dated and sourced. `DROP` ends the workflow for this signal.

### 4. Matching Engine

Source: [`specs/03_matching_engine.md`](../specs/03_matching_engine.md)

Evaluate proposed fit between the verified demand and the discovered Turkish manufacturer (and any intermediary). Runs only after both demand and supply have independent evidence.

**Hand-off condition:** a ranked, evidenced match with no failed hard gate. `DROP` ends the workflow for this pairing.

### 5. Opportunity Scoring

Source: [`specs/04_opportunity_scoring.md`](../specs/04_opportunity_scoring.md)

Score the accepted match by probability of reaching first revenue, using the five weighted dimensions and hard gates defined in the spec. Produces an Atlas Opportunity Score and status.

**Hand-off condition:** an accepted opportunity scorecard with status, score, hard-gate results and expiry. `DROP` ends the workflow for this opportunity.

### 6. CEO Decision

Source: [`specs/06_daily_opportunity_feed.md`](../specs/06_daily_opportunity_feed.md) (Top 1 / CEO recommendation section)

Atlas CEO reviews the Top 1 candidate and any flagged `WATCH` items and issues a binding `PROCEED`, `WATCH` or `DROP` decision from accepted evidence only. The CEO does not invent missing facts and does not use the feed to fill a quota.

**Hand-off condition:** a recorded decision with owner, next action and, for `WATCH`, a named missing evidence item with due date.

### 7. Daily Opportunity Feed

Source: [`specs/06_daily_opportunity_feed.md`](../specs/06_daily_opportunity_feed.md)

Publish the dated Top 20, Top 5 and Top 1 snapshot from accepted upstream records at one Istanbul-time cutoff, with change notes and exclusion summary. This step is the workflow's terminal, recurring output — it does not re-run steps 1–6, it packages their accepted results.

**Hand-off condition:** none — this is the workflow's output boundary. The next cycle re-enters at step 1 for new candidates and at step 3 for re-evaluated demand.

## Governing rules

- Any `DROP` at any step ends that candidate's path through the workflow; it is not carried forward.
- Any `WATCH` may re-enter its own step once the named missing evidence is resolved; it does not skip ahead.
- Demand (step 3) must be established before a Turkish supplier is treated as selected, even if discovery (step 1) surfaced the manufacturer first.
- Unknown facts remain `UNKNOWN` at every step; no step may invent a value to satisfy the next step's inputs.
- This workflow authorizes no outreach, CRM activity, quotation, order or commercial commitment at any step. Only the CEO Decision step (6) issues a binding decision, and only within the bounds of `specs/06_daily_opportunity_feed.md`.
- All steps must comply with [`ATLAS_RULES.md`](../ATLAS_RULES.md).

## Non-goals

This document does not implement any step, does not define scoring weights, and does not create a new specification. It orders existing, already-defined specifications and discovery process only.
