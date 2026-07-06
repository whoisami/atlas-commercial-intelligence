# Top 5 — PROCEED Gate Applied

Per [`specs/06_daily_opportunity_feed.md`](../../specs/06_daily_opportunity_feed.md), a Top 5 candidate requires score ≥75, Verification Confidence ≥70, a named owner and one bounded next action. Per [`specs/04_opportunity_scoring.md`](../../specs/04_opportunity_scoring.md), `PROCEED` additionally requires Atlas Opportunity Score ≥80 and no critical `UNKNOWN`.

## Result: 0 of 20 opportunities qualify for PROCEED or for the strict Top 5 gate

| Rank | Opportunity | Score | Verif. Confidence | Gate result |
|---:|---|---:|---:|---|
| 1 | ERBAB → CNH Industrial (Italy) | 77 | 65 | Score <80; Verification <70 |
| 2 | ERBAB → KION Group (Germany) | 75 | 62 | Score <80; Verification <70 |
| 3 | Pro-Mak → CNH Industrial (Italy) | 74 | 62 | Score <80; Verification <70 |
| 4 | Pro-Mak → GEA Group (Germany) | 73 | 60 | Score <80; Verification <70 |
| 5 | Pro-Mak → KION Group (Germany) | 73 | 60 | Score <80; Verification <70 |

No opportunity in the full Top 20 reaches Verification Confidence ≥70. Rank 1 is the only record at or above the score-75 line, and it fails on verification alone. Per `specs/06_daily_opportunity_feed.md`: report the actual number rather than lower the standard or pad the list. This feed publishes zero PROCEED candidates.

## Top 5 WATCH priority (substitute, for verification sequencing only)

Because no opportunity meets the PROCEED gate, the following are the five highest-ranked `WATCH` opportunities — the sequencing priority for the verification work in [`04_30day_action_plan.md`](04_30day_action_plan.md), not an authorization to proceed commercially:

1. ERBAB → CNH Industrial N.V. (Italy) — score 77
2. ERBAB → KION Group AG (Germany) — score 75
3. Pro-Mak → CNH Industrial N.V. (Italy) — score 74
4. Pro-Mak → GEA Group AG (Germany) — score 73
5. Pro-Mak → KION Group AG (Germany) — score 73

## Decisive gap

The single factor separating rank 1 from PROCEED is Verification Confidence: ERBAB and Pro-Mak identity, manufacturing and certification claims are currently supported only by company-controlled sources (official website, official contact channel). No independent industrial source class (Bursa OSB/chamber record, exporters' association record, certification registry, government industrial directory) has yet corroborated either manufacturer, per `discovery/discovery_engine.md`'s two-independent-source-class rule.

This feed authorizes no outreach, CRM activity, quotation or commitment for any of the five.
