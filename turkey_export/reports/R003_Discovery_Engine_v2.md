# R003 — Discovery Engine v2

- **Module:** Turkey → World
- **Version:** Commercial Signal Discovery Engine v2
- **Date:** 2026-07-06
- **Scope changed:** `turkey_export/` only
- **External contact:** None

## Executive Summary

Discovery Engine v2 replaces company-name-first discovery with a signal-to-opportunity system. Atlas now monitors evidence of commercial change—exports, certifications, investments, capacity, fairs, hiring, new lines, partnership searches and buyer procurement access—then resolves and verifies the organizations behind those signals.

The main governance change is multi-source verification. A company website can prove a company-stated capability, but it cannot alone support `PROCEED`. Weak digital presence is no longer a disqualifier: OSB, chamber, exporters' association, government, fair, machinery-supplier and certification records can establish identity, factory presence, capability and timing.

All 20 Sprint 001 opportunities were migrated without deleting legacy fields. Their current v2 decision is `WAIT` because manufacturer-side evidence is still concentrated in company-controlled sources and no candidate yet reaches Verification Score 70. ERBAB → CNH ranks first at Atlas Opportunity Score 77, Accessibility 80, Signal 55 and Verification 65. The next sprint should verify that pair through independent institutional sources before any outreach preparation.

## Architecture Changes

### v1 — Company Finder

The prior engine began with named companies, verified manufacturing claims and ranked matches. This favored firms with mature websites and allowed official supplier portals to carry too much decision weight.

### v2 — Commercial Signal Discovery

The v2 sequence is:

1. monitor public, industrial and commercial-signal sources;
2. capture a dated signal;
3. resolve the organization behind the signal;
4. verify identity and decisive claims across independent source classes;
5. classify manufacturer and foreign buyer type;
6. score commercial accessibility and timing;
7. create a commercial-model hypothesis;
8. calculate Atlas Opportunity Score;
9. issue `PROCEED`, `WAIT` or `DROP` with one first action.

This supports manufacturers with weak websites because entity resolution can begin from an OSB record, chamber registration, fair list, machinery installation, certification registry or export association.

## Discovery Layers

### Layer 1 — Public Digital Discovery

Company websites, LinkedIn, public job pages, Google Business, trade directories, industry associations and certification databases. These sources expose public activity and access routes but remain vulnerable to self-reporting and stale profiles.

### Layer 2 — Industrial Discovery

OSB directories, chambers of industry/commerce, exporters' associations, industrial clusters, fair exhibitor lists, government industrial directories, machine-supplier references and certification registries. This layer is the primary verification and weak-digital-presence recovery route.

### Layer 3 — Commercial Signals

Dated evidence of new export activity, certification, investment, capacity, fair participation, distributor/partner search, international-sales hiring, product launch, production line or buyer procurement access. Each signal has a freshness window, evidence state, contradiction check and review date.

## Buyer Discovery Expansion

The engine no longer limits buyer discovery to end-user OEMs. Valid buyer/partner types are:

- foreign OEM;
- Tier 1 or Tier 2 supplier;
- procurement company;
- sourcing company;
- contract-manufacturing buyer;
- purchasing office;
- industrial distributor;
- trading company;
- supply-chain partner.

Buyer function, product need and outsourcing intent are separate claims. A supplier portal verifies access architecture—not a current RFQ.

## New Scoring System

| Component | Weight | Decision meaning |
|---|---:|---|
| Manufacturing Score | 20% | Is relevant production real and technically credible? |
| Export Readiness | 15% | Can the manufacturer serve foreign accounts? |
| Commercial Accessibility | 15% | Can Atlas establish a relationship within 90 days? |
| Commercial Signals | 15% | Is now the right time? |
| Revenue Potential | 15% | Could the opportunity produce repeat commercial value? |
| Execution Speed | 10% | Can the next commercial gate be reached within 90 days? |
| Verification Confidence | 10% | Are decisive claims independently verified? |

`Atlas Opportunity Score = Σ(component score × component weight) / 100`

Every component is 0–100 and labeled VERIFIED, ESTIMATED or UNKNOWN. UNKNOWN earns no points. Price, volume, order and commission values remain unknown until commercial evidence exists.

## Commercial Signal Model

Signal Score measures strength/relevance (30%), recency (20%), independent corroboration (15%), investment/capacity/new-line evidence (15%), new-market/hiring/fair/partnership evidence (15%) and 90-day actionability (5%).

Important distinctions:

- an undated supplier portal mainly improves Accessibility and is only a weak timing signal;
- hiring Export Sales within 90 days is a strong current intent signal but does not prove export revenue;
- a machine installation announcement is capacity evidence only after the correct factory/entity is resolved;
- international fair participation is a market-development signal but not proof of buyer demand;
- announced expansion and commissioned capacity are different evidence states.

## Verification Model

Verification Score combines entity consistency, factory/operating address, public business contact, manufacturing/buyer-function evidence, institutional records, certification scope, current team/activity and source independence.

`PROCEED` requires at least two independent source classes. Multiple pages controlled by the same company remain one class. A copied directory entry is not independent. Contradictions must be resolved or the opportunity stays `WAIT`.

Minimum v2 thresholds:

- Atlas Opportunity Score ≥ 75;
- Verification Score ≥ 70;
- Accessibility Score ≥ 60;
- Signal Score ≥ 50;
- manufacturing hard gate passed;
- no unresolved material conflict;
- executable first action within 90 days.

## Accessibility Model

Commercial Accessibility measures company-size fit, export-department maturity, distributor/channel openness, decision-maker/category-owner access, contact usability, public supplier/partner openness, growth and explicit partnership signals.

The score intentionally penalizes two opposite problems:

- an inaccessible large organization with closed incumbent networks;
- a small manufacturer with no verified contact or ability to support export development.

A weak website only affects digital contact maturity. Verified phone, chamber/OSB access, fair presence or public procurement registration can compensate.

## Migrated Sprint 001 Snapshot

| Rank | Opportunity | Manufacturing | Export | Accessibility | Signal | Revenue | Speed | Verification | Atlas Opportunity | v2 Decision |
|---:|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 1 | ERBAB → CNH | 92 | 90 | 80 | 55 | 80 | 65 | 65 | 77 | WAIT |
| 2 | ERBAB → KION | 92 | 90 | 78 | 45 | 74 | 70 | 62 | 75 | WAIT |
| 3 | Pro-Mak → CNH | 88 | 80 | 80 | 55 | 73 | 65 | 62 | 74 | WAIT |
| 4 | Pro-Mak → KION | 88 | 80 | 78 | 45 | 81 | 70 | 60 | 73 | WAIT |
| 5 | Pro-Mak → GEA | 88 | 80 | 82 | 50 | 71 | 70 | 60 | 73 | WAIT |

Scores are ESTIMATED from existing Sprint 001 evidence. Legacy decisions are preserved in CSV fields. None is promoted under v2 because independent manufacturer verification is incomplete.

## Data and Governance Changes

- Manufacturer records now capture signal type/date/state, source classes, Verification, Accessibility, Signal and legacy status.
- Buyer records now capture source classes, Verification, Accessibility, Signal, signal type/date/state and legacy status.
- Opportunity records now contain all seven v2 component scores, Atlas Opportunity Score, evidence state/summary, buyer type/country and legacy decision.
- Current decisions were changed to `WAIT`; this is a controlled migration, not deletion of historical conclusions.

## Risks

- Institutional directories may be stale and require recency checks.
- Multiple sources may repeat the same company claim and create false confidence.
- Job postings or fair attendance may be overinterpreted as commercial intent.
- Signal monitoring can favor visible activity unless industrial sources are systematically covered.
- Verification work may become open-ended; each `WAIT` requires a narrow promotion/drop test.
- Scoring remains estimated until independent records and direct commercial facts are captured.

## Recommended Next Sprint

Run a verification sprint on the top three migrated opportunities only:

1. **ERBAB → CNH:** verify ERBAB through Bursa OSB/chamber or government industrial records, confirm current certificate scope through registries, verify factory phone/address independently, and confirm whether CNH's relevant commodity route is currently accessible.
2. **ERBAB → KION:** reuse verified manufacturer evidence, then confirm KION category access and channel conflict.
3. **Pro-Mak → CNH:** verify Bursa industrial registration, IATF certificate scope, factory identity and a dated manufacturer-side export/growth signal.

Stop when one opportunity reaches Verification 70 and all `PROCEED` gates—or when decisive evidence forces `DROP`.

## First Recommended Action

Verify ERBAB's legal/factory identity and current certification scope through at least two independent industrial source classes. Do not contact ERBAB or CNH during discovery. If Verification reaches 70, review channel conflict and manufacturer commercial openness as the next gate.

## Decision

**WAIT** — Engine v2 is production-defined and data migration is complete, but no current Sprint 001 opportunity yet satisfies the new multi-source Verification gate.
