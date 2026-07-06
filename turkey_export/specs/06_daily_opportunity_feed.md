# SPEC_006 — Daily Opportunity Feed

## Purpose

Define a daily, decision-ready Turkey → World opportunity snapshot that converts accepted upstream records into a ranked Top 20, Top 5 and Top 1 CEO recommendation. The feed prioritizes evidence-backed first-revenue probability, not record volume. This is a specification only: it implements no scheduler, engine, dashboard, CRM, discovery, outreach or automation.

## Inputs

| Input | Required content | Evidence rule |
|---|---|---|
| Opportunity scorecards | Opportunity ID, status, Atlas Opportunity Score, five dimensions, hard gates, expiry | Accepted output under [`04_opportunity_scoring.md`](04_opportunity_scoring.md) |
| Upstream decisions | Demand, manufacturer, match and commercial-model status | Any upstream `WATCH` caps the opportunity at `WATCH`; any decisive `DROP` excludes it |
| Evidence register | Sources, dates, states, contradictions, verification confidence | Public or authorized; critical `UNKNOWN` prevents Top 1 `PROCEED` |
| Execution record | Next action, owner, dependencies, due date, capacity requirement | Missing owner or executable next action lowers eligibility |
| Prior feed | Previous rank, status, score, recommendation and changes | Used for deduplication and change explanation, not momentum scoring |

Apply [`ATLAS_RULES.md`](../ATLAS_RULES.md). Resolve duplicate opportunities by stable entity, demand and match IDs; preserve materially distinct buyer needs separately.

## Outputs

- Dated feed header: generation date, evidence cutoff, eligible count, excluded count and source records.
- Ranked Top 20, decision-ready Top 5 and one Top 1 CEO recommendation, without padding.
- Each row: rank, opportunity ID, buyer/country, Turkish manufacturer, need, model, score, status, expiry, next action and owner.
- Change note: new, moved, unchanged, expired or removed, with reason.
- Exclusion summary: hard-gate failure, stale evidence, duplicate, `DROP` or incomplete upstream record.

Outputs distinguish `VERIFIED`, `ESTIMATED`, `HYPOTHESIS` and `UNKNOWN` and authorize no contact or commitment.

## Daily opportunity generation

Use one Istanbul-time daily cutoff. Include only opportunities updated or still valid at that cutoff, with traceable upstream records and no failed hard gate. Re-evaluate expiries, contradictions and status changes before ranking. Do not create opportunities to fill a quota; if none qualify, publish an empty feed and the highest-priority verification gap.

The daily feed is a snapshot, not a CRM history. It must preserve prior-feed references and explain material rank or status changes.

## Ranking

Rank eligible opportunities by:

1. Decision class: `PROCEED` before `WATCH`; never rank `DROP`.
2. Atlas Opportunity Score, highest first.
3. Verification Confidence, then Accessibility, then Execution Speed.
4. Earlier credible first-revenue window.
5. More recent verified demand signal.
6. Stable Opportunity ID as the deterministic final tie-breaker.

Scores are not recalculated here. A failed identity, demand, manufacturing, legal/sanctions, mandatory-fit or evidence-integrity gate overrides rank. Rank changes caused only by stale or missing evidence must be stated.

## Top 20

Include up to 20 unique opportunities with score ≥50 and status `PROCEED` or `WATCH`. Show the decisive evidence, limitation, expiry and next action. If fewer than 20 qualify, report the actual number; never lower standards or duplicate records.

## Top 5

Select up to five execution-priority opportunities from the Top 20. A Top 5 candidate must have score ≥75, Verification Confidence ≥70, a named owner and one bounded next action. `WATCH` may appear only when its single verification action could plausibly unlock `PROCEED` quickly and is labeled.

## Top 1

Select exactly one Top 1 only when a Top 5 opportunity is `PROCEED`, meets the [`04_opportunity_scoring.md`](04_opportunity_scoring.md) `PROCEED` gates, has no critical `UNKNOWN`, and has the strongest evidence-backed first-revenue path. If none qualifies, state `NO PROCEED CANDIDATE` and name the one verification action with the greatest decision value.

## CEO recommendation

For Top 1, recommend `PROCEED`, `WATCH` or `DROP` with confidence, commercial impact, expected time to first revenue or `UNKNOWN`, preferred commercial model, owner, next action and blocking issues. The recommendation is advisory; Atlas CEO makes the binding decision from accepted evidence and does not use the feed to invent missing facts.

- **PROCEED:** approve only the named next commercial-validation action.
- **WATCH:** request the named missing evidence with owner, due date and expiry; no outreach is authorized.
- **DROP:** remove the opportunity when a hard gate fails or expected value no longer justifies work.

## Acceptance criteria

- [ ] The feed is Turkey → World only and uses one dated evidence cutoff.
- [ ] Every ranked opportunity has accepted upstream records and traceable evidence.
- [ ] Ranking follows the stated deterministic order and never includes `DROP`.
- [ ] Top 20 and Top 5 are maximums, not padding requirements.
- [ ] Top 1 is selected only from eligible `PROCEED` candidates; otherwise `NO PROCEED CANDIDATE` is explicit.
- [ ] CEO recommendation includes status, confidence, impact, time to revenue, model, owner, next action and blockers.
- [ ] Stale, duplicate, contradictory and expired records are controlled and changes explained.
- [ ] Missing facts remain `UNKNOWN`; no opportunity, score, buyer, manufacturer, price or demand is invented.
- [ ] Outputs authorize no outreach, CRM activity, transaction or commercial commitment.
- [ ] No implementation, scheduler, engine, dashboard or automation is included.
