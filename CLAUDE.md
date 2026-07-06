# CLAUDE.md

Guidance for Claude Code working in this repository.

## Scope boundary

- **Foreign → Turkey is STABLE.** Do not modify anything outside `turkey_export/` unless explicitly asked. Treat it as frozen by default.
- **Turkey → World is active work** and lives entirely inside [`turkey_export/`](turkey_export/).
- Work only in the folder the user's request points to. Do not wander into sibling directories to "help."

## Governing rules

- Follow [`turkey_export/ATLAS_RULES.md`](turkey_export/ATLAS_RULES.md) for every Turkey → World task.
- Prefer writing or updating a specification before any implementation. Specifications are commercial contracts, not engines.
- Keep specification files under 80 lines.
- No CRM integration, no email automation, no invented data. Unknown facts stay `UNKNOWN`.
- This repository is Commercial Intelligence only — no executable outreach, transaction or automation logic.

## Working style

- Avoid broad repo scans. Go directly to the requested file or folder; don't grep the whole repository when a path is already known.
- Don't create new top-level folders or specs unless asked.
- Commit locally after each completed task. If a push is requested and fails, stop after the local commit — do not force-push or retry destructively.

## Reference

- [`turkey_export/specs/README.md`](turkey_export/specs/README.md) — how to create and approve a specification.
- [`turkey_export/playbook.md`](turkey_export/playbook.md) — commercial playbook context.
