# Sprint 001 Review — OEM Metal Components

Evidence cutoff: 2026-07-06. Covers discovery (`discovery/discovery_engine.md`), Discovery Engine v2 migration (`reports/R003_Discovery_Engine_v2.md`), and the Commercial Opportunity Workflow run (`runs/sprint_001/`).

## Objective

Discover, verify and rank Turkey → World commercial opportunities in OEM Metal Components, and identify the highest-probability first action toward first revenue — without outreach, CRM activity or any commercial commitment.

## What worked

- Signal-first discovery (Layers 1–3) produced six manufacturers, ten foreign buyers and 20 scored opportunities without inventing data.
- The v1→v2 scoring migration preserved legacy fields and re-graded every record against a stricter, seven-component model instead of silently overwriting history.
- The Commercial Opportunity Workflow run independently reached the same conclusion as the discovery-engine migration, cross-validating the decision.
- Hard gates held: no opportunity was force-promoted to `PROCEED` to fill a quota; the feed reported the true count (0) rather than padding.

## What failed

- Manufacturer and buyer evidence never advanced past single-source-class (company-controlled) support; the required two-independent-source-class bar was never cleared for any of the six manufacturers.
- No dated, manufacturer-side commercial signal (export event, capacity change, hiring, fair participation) was captured for any candidate — Signal Score is the weakest dimension across the portfolio (35–80, mostly under 55).
- No commercial owner was ever assigned to any opportunity; every action in the 30-day plan carries owner `UNKNOWN`.
- Estimated order value, commission potential and buyer mandate remain `UNKNOWN` for all 20 opportunities — the portfolio has no economic sizing.

## Key findings

- Rank 1 (ERBAB → CNH Industrial, Italy, score 77) is the closest candidate to `PROCEED` but fails Verification Confidence (65 vs. 70 floor).
- Pro-Mak Automotive appears in 5 of the top 11 opportunities — the broadest buyer fit of any manufacturer, but still single-source.
- Ulus Metal carries an unresolved channel-conflict risk: its own website lists a Polish contact entity, which could bypass Atlas on Poland-market matches.
- Buyer-side evidence is uniformly procurement-access evidence (supplier portals, registration routes) — none confirms an open, category-specific order.

## Wrong assumptions

- That a detailed company website (machine lists, certifications, export claims) would be sufficient evidence for `PROCEED`; the v2 verification gate showed company-controlled content alone caps every record at `WATCH`.
- That a live supplier portal or self-registration route implied current buyer demand; `discovery/discovery_engine.md` corrected this — access architecture is not proof of an open order.
- That English-language content indicated export readiness; several manufacturers were flagged where this assumption alone would have overstated readiness.

## Correct assumptions

- That demand should be evidenced before Turkish supply is selected — no opportunity was built supply-first.
- That numeric scores should never override hard gates — no opportunity reached `PROCEED` despite several scoring 70+ on Manufacturing Strength or Accessibility.
- That reporting fewer, honest results beats padding a list — the Top 5 PROCEED and Top 1 outputs correctly returned zero and `NO PROCEED CANDIDATE`.

## Improvements for Sprint 002

1. Prioritize independent verification (OSB/chamber, exporters' association, certification registry) over adding new manufacturers.
2. Capture at least one dated commercial signal per top-5 manufacturer before further scoring work.
3. Assign a named Atlas commercial owner per opportunity before any action is scheduled.
4. Resolve the Ulus Metal / Poland channel-conflict question before scoring any further Poland-market match.
5. Bound Sprint 002 to the top 3 opportunities only, per `reports/R003_Discovery_Engine_v2.md`'s recommended next sprint.

## CEO decision

**WATCH.** No opportunity meets the `PROCEED` gate; none is `DROP`. Approve only the named verification action on ERBAB → CNH Industrial (independent identity and certificate-scope verification, due 2026-07-20). No outreach, CRM activity, quotation or commitment is authorized.
