# Phase 0 — Charter and scope

**Status:** not_started  
**Owner:** _(you)_  
**Last updated:** 2026-05-04

## Purpose

Lock a **shared definition** of what this project delivers so later phases do not creep into “generic security research” without an operations outcome.

## Outcomes (done when)

- [ ] One-paragraph **mission** (who is protected, what environment—home lab, SMB, MSSP-style, etc.).
- [ ] **In scope** list: e.g. endpoint logs, firewall denies, auth failures, phishing triage, vuln scan dedupe—pick a small set.
- [ ] **Out of scope** list: e.g. physical security, full IR retainers, malware RE at nation-state depth—explicit non-goals.
- [ ] **Human vs automation** model documented:
  - **Human-out-of-loop** for which classes of action (read-only enrich, ticket fields, routing).
  - **Human-on-the-loop** for which classes (isolation, account disable, legal/comms).
- [ ] **Success metric** for Phase 3 MVP: one measurable sentence (e.g. “time from synthetic alert to documented disposition &lt; X minutes without manual log pivot”).

## Mission draft (edit in place)

_(Replace this block with your final mission.)_

> Build a **minimal SOC** that executes **documented procedures** for routine detection and triage, using automation where safe, and preserves an **audit trail** for every decision.

## Principles (suggested defaults)

1. **Procedure before code** — no automation without a written SOP/playbook (Phase 1).
2. **Least privilege** — automated actions use the narrowest credentials and can be disabled per integration.
3. **Explainability** — every automated disposition states *which* SOP step and *which* evidence satisfied it.
4. **Small surface** — fewer alert types done well beats dozens of flaky rules.

## Dependencies

- None (start here).

## Next phase

When Phase 0 is satisfied, proceed to [phase-1-knowledge-and-sops.md](phase-1-knowledge-and-sops.md).
