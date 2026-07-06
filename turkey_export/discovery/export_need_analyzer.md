# Export Need Analyzer

## Operating contract

This procedure implements [SPEC_001](../specs/01_export_need_analyzer.md). It evaluates whether an already-discovered Turkish manufacturer is likely to need external business-development support for a defined foreign-demand context.

It does not discover manufacturers, buyers, contacts or demand; perform full due diligence; create CRM records; draft or send outreach; or authorize a commercial commitment.

## Entry gate

Open an [Export Need Assessment](export_need_assessment.md) only when all of the following are available:

- stable Turkish manufacturer ID and upstream discovery record;
- resolved legal/trading identity and Turkey operating location;
- foreign product/capability demand, target country or buyer segment, source and date;
- at least one first-party product/process source;
- at least one independent industrial, institutional or certification source;
- current opportunity owner and evidence cutoff.

If the discovery record or demand context is missing, issue `WATCH` with one verification action. Do not replace the missing upstream work inside this analyzer.

## Evidence states

- **VERIFIED:** directly supported by current first-party, authoritative or accepted Atlas evidence.
- **ESTIMATED:** derived from disclosed evidence and assumptions; never presented as fact.
- **HYPOTHESIS:** plausible explanation requiring a named test.
- **UNKNOWN:** absent, inaccessible, stale beyond usefulness or materially contradictory.

Every scored claim records source URL or stable record ID, source class, publication/event date, access date, evidence state, supported claim and limitation. Same-owner pages count as one source class. `UNKNOWN` earns zero.

## Workflow

1. **Lock scope.** Record manufacturer ID, discovery ID, demand record, target context, owner and cutoff.
2. **Resolve identity.** Match name, domain, city, factory address and institutional identifier; reject distributors, traders, brokers, marketplaces and service-only firms.
3. **Build evidence ledger.** Capture manufacturing, export, growth, business-development, partnership, commercial-model and contradiction evidence.
4. **Apply hard gates.** Record PASS, WATCH or FAIL before scoring.
5. **Score Evidence Quality.** Award only evidenced points factor by factor.
6. **Score dimensions.** Use [Export Need Scoring](export_need_scoring.md) for Export Readiness, Growth Need, Business Development Need, Partnership Openness and Atlas Revenue Potential. Consume Manufacturing Strength from the accepted manufacturing assessment; do not recalculate it here.
7. **Test alternatives.** State at least one competing explanation for the apparent need and the evidence that would distinguish it.
8. **Calculate and decide.** Apply thresholds and floors without discretionary overrides.
9. **Record action.** `PROCEED` names one deeper validation step; `WATCH` names one bounded verification plan; `DROP` names the decisive disqualifier.
10. **Stop.** End when one defensible decision and next action exist.

## Hard gates

| Gate | PASS | WATCH | FAIL / decision |
|---|---|---|---|
| Upstream discovery | Stable accepted record | Missing or stale but recoverable | Fabricated/misattributed → `DROP` |
| Entity/manufacturer | Turkish operating manufacturer verified | Identity/manufacturer status resolvable | Non-manufacturer or false identity → `DROP` |
| Demand context | Defined foreign need and target context | Missing/stale but recoverable | Proven no relevant fit → `DROP` |
| Manufacturing fit | Relevant capability plausibly evidenced | Mandatory capability fact unknown | Relevant capability absent → `DROP` |
| Evidence integrity | Sources traceable and correctly attributed | Material contradiction under review | Invented/fabricated evidence → `DROP` |
| Critical risk | No known disqualifying signal | Authoritative check required by a signal | Confirmed legal/sanctions/fraud/safety conflict → `DROP` |
| Commercial model | Lawful value and revenue path plausible | Payer/event/access unverified | No structural value-capture path → `DROP` |
| Contradictions | None could reverse decision | Decisive contradiction unresolved | Contradiction disproves core case → `DROP` |

Every gate must PASS for `PROCEED`. Numeric scores never override a failed gate.

## Evidence Quality — 0 to 100

| Component | Points |
|---|---:|
| Entity identity and source ownership resolved | 20 |
| Manufacturing directly evidenced and independently corroborated | 25 |
| Export-readiness evidence current and verifiable | 15 |
| Growth and business-development need supported by dated evidence | 20 |
| Partnership and commercial-model evidence traceable | 10 |
| Contradictions, freshness and limitations handled | 10 |
| **Total** | **100** |

Unavailable points score zero. Record awarded points and rationale; `PROCEED` requires at least 70.

## Export Need Score — 0 to 100

| Dimension | Weight | Required evidence focus | `PROCEED` floor |
|---|---:|---|---:|
| Manufacturing Strength | 15 | Relevant process, factory, quality and delivery evidence | 60 |
| Export Readiness | 15 | Export activity, certifications, documentation, language and logistics | 50 |
| Growth Need | 20 | Dated expansion, investment, hiring, market or capacity-utilization signal | 55 |
| Business Development Need | 20 | Specific target-market coverage, buyer-access, export-sales or partner gap | 60 |
| Partnership Openness | 15 | Verified agent, representative, distributor or external-partner evidence | 50 |
| Atlas Revenue Potential | 15 | Named model, payer/event, access, repeatability and first-revenue path | 60 |
| **Total** | **100** |  |  |

Use anchors consistently: 0 = disproven/absent/entirely `UNKNOWN`; 25 = weak indirect signal; 50 = plausible with material gaps; 75 = strong current evidence; 100 = exceptional multi-source evidence without material contradiction. Scores between anchors require written justification.

`Atlas Export Need Score = Σ(dimension score × weight) / 100`

Round only the final score. Keep component calculations unrounded. Need must be an evidenced capability or access gap, never inferred financial distress. English content and public contact details alone do not prove export readiness or partnership openness.

The five commercial dimensions and final decision must be calculated under [Export Need Scoring](export_need_scoring.md). Manufacturing Strength remains an upstream technical score and hard floor; this scoring implementation does not redefine it.

## Decision

### PROCEED

All hard gates PASS; Export Need Score ≥75; Evidence Quality ≥70; all six dimension floors pass; no critical `UNKNOWN`; and one deeper partnership-validation action is defined.

This authorizes only the named validation step. It does not authorize contact.

### WATCH

Use when score is 50–74, Evidence Quality is below 70, a floor misses because evidence is incomplete, or a gate/contradiction is realistically resolvable. Record one missing fact, decision impact, smallest verification action, owner, due date and review trigger. Reassess at expiry; do not leave WATCH open indefinitely.

### DROP

Use when a hard gate fails; score is below 50 without a credible reversal path; manufacturing/fit is disproven; no business-development gap or partnership route exists; the manufacturer already covers the target market without a credible Atlas role; revenue capture is structurally absent; risk is unacceptable; or verification effort exceeds plausible value.

A dropped record may re-enter only after a new dated signal materially changes the failed condition.

## Quality and stop rules

- Do not infer need from company size, weak website, no public export team or silence.
- Do not infer openness from an email address, partner logo or generic “contact us” page.
- Do not treat export capability as proof of external business-development need.
- Do not conceal contradicting evidence or select only favorable sources.
- Stop after one actionable decision; do not research to make a preferred score pass.
- Preserve the assessment and evidence ledger for review.
