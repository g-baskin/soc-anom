# soc-anom documentation

Human-facing documentation for building an **automated SOC** (Security Operations Center): encoded processes, playbooks, and tooling that handle routine analyst work with clear escalation rules—not a lab-only red-team toy.

## Where to start

| Audience | Start here |
|----------|------------|
| Anyone landing cold | [phases/README.md](phases/README.md) — phased roadmap |
| Charter and boundaries | [phases/phase-0-charter-and-scope.md](phases/phase-0-charter-and-scope.md) |
| TryHackMe → procedures | [phases/phase-1-knowledge-and-sops.md](phases/phase-1-knowledge-and-sops.md) |
| Data plane and integrations | [phases/phase-2-technical-foundation.md](phases/phase-2-technical-foundation.md) |
| First end-to-end automation | [phases/phase-3-mvp-automation.md](phases/phase-3-mvp-automation.md) |

## Repo layout (high level)

- **`docs/`** — this tree: vision, phases, runbooks as you add them.
- **`library/knowledge-base/wiki/`** — Legion-style wiki (entities, ADRs); optional parallel to `docs/` for machine-oriented links.

## Conventions (suggested)

- **Phase docs** describe outcomes and acceptance criteria; deep runbooks can live as `docs/runbooks/<name>.md` later.
- Date major edits at the bottom of each phase file (`Last updated: YYYY-MM-DD`).
