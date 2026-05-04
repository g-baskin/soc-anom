# Phase 1 — Knowledge and SOPs

**Status:** not_started  
**Owner:** _(you)_  
**Last updated:** 2026-05-04

## Purpose

Convert **training and policy** into **repeatable playbooks** so automation (Phase 3) implements known-good steps instead of inventing analysis ad hoc.

## Outcomes (done when)

- [ ] **Playbook template** adopted (single file or table): trigger, assumptions, data needed, steps, false-positive handling, escalation.
- [ ] **Curriculum map**: TryHackMe (or other) rooms/paths **mapped to playbooks** (each row: room → tactic → playbook id).
- [ ] At least **3 draft playbooks** for in-scope scenarios from Phase 0 (can be rough).
- [ ] **Severity / priority rubric** documented (P1–P4 or your scale) aligned to response SLAs.
- [ ] **Evidence retention** note: what to log, how long, where (even if “TBD in Phase 2”).

## TryHackMe → playbook mapping (starter table)

| THM module / path | Tactic / topic | Playbook ID | Notes |
|-------------------|----------------|-------------|-------|
| _(example)_ SOC Level 1 | Alert triage | PB-TRIAGE-001 | |
| | | | |

_Add rows as you complete rooms; playbook IDs should stay stable once referenced by automation._

## Playbook template (copy per playbook)

```markdown
# PB-XXX: Title
- **Trigger:** (alert name, rule id, or log pattern)
- **Data sources:** (where analyst—or bot—looks first)
- **Steps:** numbered; each step testable
- **False positives:** how to close benign quickly
- **Escalate when:** explicit conditions
- **References:** THM room, internal policy link, MITRE technique id
```

## Dependencies

- [Phase 0](phase-0-charter-and-scope.md) mission and scope agreed.

## Next phase

[phase-2-technical-foundation.md](phase-2-technical-foundation.md) — inventory systems and choose first log pipeline.
