# Phase 2 — Technical foundation

**Status:** not_started  
**Owner:** _(you)_  
**Last updated:** 2026-05-04

## Purpose

Define **where data lives**, how it reaches analysis, and what **integration boundaries** exist so Phase 3 automation has concrete APIs/files/queues to call.

## Outcomes (done when)

- [ ] **Environment diagram** (ASCII or exported image): sources → collector → storage → analysis → ticketing/chat.
- [ ] **Integration inventory** table: system, owner, auth method, data type, rate limits, link to runbook.
- [ ] **Lab / simulation** plan: how you generate **safe, repeatable** alerts (THM VMs, Atomic Red Team with guardrails, vendor test feeds, etc.).
- [ ] **Repo layout decision** for code (e.g. `src/` Python services, `playbooks/` YAML, `infra/` as needed)—documented here, even if folders are empty.
- [ ] **Secrets handling** rule: env vars, vault, no secrets in git—one paragraph.

## Integration inventory (starter table)

| System | Role | Auth | Notes |
|--------|------|------|-------|
| _(e.g.)_ syslog VM | Log source | SSH / API | |
| _(e.g.)_ SIEM or Loki | Storage / search | API token | |
| _(e.g.)_ Jira / Linear | Tickets | OAuth / PAT | |

## Data flow (placeholder diagram)

```text
[Sources] --> [Ingest] --> [Store/Search] --> [Rules/Detections] --> [Queue/Work]
                                                      |
                                                      v
                                              [Playbook engine]
                                                      |
                                    +---------------+---------------+
                                    v               v               v
                              [Enrich]      [Ticket update]    [Escalate human]
```

## Dependencies

- [Phase 1](phase-1-knowledge-and-sops.md) playbooks drafted for the scenarios you will wire first.

## Next phase

[phase-3-mvp-automation.md](phase-3-mvp-automation.md) — implement one vertical slice.
