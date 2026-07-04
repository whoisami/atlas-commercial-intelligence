# Atlas OS Governance

## Purpose

Atlas OS is a documentation-first commercial intelligence operating system for international B2B market development. It converts public and internal evidence into traceable product, manufacturer, buyer, pricing, outreach and representation decisions.

It is not software, a CRM replacement or an autonomous contacting system.

## Operating principles

1. Evidence before opinion.
2. First-party sources before directories.
3. Commercial usefulness before research volume.
4. Unknown stays `UNKNOWN`; it is never guessed.
5. Every claim is traceable to a URL, document or dated internal observation.
6. Every recommendation has an owner, next action and decision gate.
7. No agent contacts a company unless a human explicitly authorizes the message and channel.
8. Commission or representation models are preferred before inventory risk.

## Write ownership

| Surface | Writer | Rule |
|---|---|---|
| `intelligence/<domain>/` | Assigned specialist agent | Reports and CSV delta packages only |
| `database/` | Atlas CEO | Canonical tables; updated only from validated deltas |
| `dashboard/CEO_DASHBOARD.md` | Atlas CEO | Consolidates proposed metrics from agent reports |
| `projects/` | Atlas CEO | Project charters and closed-project records |
| `workspace/` | Atlas CEO | Current operating state |
| `decisions/` | Atlas CEO only | Formal GO/WATCH/NO-GO decisions |
| `knowledge/` | Learning Intelligence proposes; Atlas CEO approves | Reusable lessons and patterns |
| `templates/` and `playbooks/` | Atlas CEO | Controlled operating standards |

The “agents write only inside intelligence” rule applies to all specialist execution agents. Atlas CEO is the governance exception that validates and promotes evidence into canonical database, dashboard, workspace, knowledge and decision files.

## Status vocabulary

- **GO:** evidence is sufficient to take the defined next commercial action.
- **WATCH:** commercially relevant, but one or more material facts remain unresolved.
- **NO-GO:** evidence shows poor fit, unacceptable risk, channel conflict or insufficient credibility.
- **UNKNOWN:** a field value could not be verified; it is not a decision status.

## Evidence levels

- **E1 — First party:** official website, catalogue, certificate, filing, named company employee or direct written reply.
- **E2 — Authoritative independent:** regulator, customs authority, trade association, official trade agency or credible professional database.
- **E3 — Corroborative:** reputable industry publication, event listing or established business directory.
- **E4 — Lead only:** marketplace, reseller page, scraped directory or unverified social content.

GO decisions require at least one E1 source for company identity and the decisive claim. E4 cannot support a GO decision by itself.

## Report lifecycle

1. Specialist creates the next sequential report in its intelligence domain.
2. Specialist attaches a CSV delta when canonical records should change.
3. Atlas CEO validates evidence, duplicate risk, schema and decision logic.
4. Atlas CEO promotes accepted deltas into `database/`.
5. Atlas CEO updates dashboard, workspace and—when required—a decision file.
6. Learning Intelligence reviews completed work for reusable patterns.

## Decision authority

Only Atlas CEO creates or changes formal files in `decisions/`. Specialist agents may recommend GO/WATCH/NO-GO inside reports but cannot make binding portfolio decisions.

