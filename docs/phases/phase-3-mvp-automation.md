# Phase 3 — MVP automation

**Status:** not_started  
**Owner:** _(you)_  
**Last updated:** 2026-05-04

## Purpose

Ship **one** end-to-end path: from **signal** (real or synthetic) through **playbook execution** to a **recorded outcome**, proving the “replace routine human steps” model before scaling alert types.

## Outcomes (done when)

- [ ] **Single MVP scenario** named (e.g. “failed SSH brute from known scanner IP → enrich → auto-close as benign noise” or “phishing IOC match → ticket + notify”).
- [ ] **Automation implements** the matching playbook from Phase 1 (step numbers traceable in logs or ticket comments).
- [ ] **Audit trail**: who/what ran, inputs, decision, timestamp (append-only log or ticket history is fine for MVP).
- [ ] **Kill switch**: documented way to disable automation for that scenario without redeploying everything.
- [ ] **Retrospective** short doc: what broke, what to automate next, what stays human.

## MVP scenario spec (fill in)

| Field | Value |
|-------|--------|
| Scenario name | |
| Playbook ID | |
| Trigger | |
| Automated actions | |
| Human escalation | |
| Success criteria (from Phase 0) | |

## Test plan (minimal)

1. Generate or replay trigger in lab.
2. Confirm playbook engine receives normalized event.
3. Confirm each automated step matches SOP order.
4. Confirm escalation path when boundary condition injected (e.g. missing field).

## Dependencies

- [Phase 2](phase-2-technical-foundation.md) integration for trigger + at least one outbound action (ticket or webhook).

## After MVP

- Add playbooks one at a time; consider **metrics** (MTTD, MTTR, auto-close % with FP sampling).
- Hardening: auth, rate limits, idempotency, replay protection.
