# Tasks — Test Webhook 19-05

**Feature status:** `in_progress` → awaiting task approval  
**Stage:** task breakdown  
**Machine state:** lives in `tasks/T<n>.yaml` — this file is narrative only.

## Index

| ID | Wave | Title | Depends on |
|----|------|-------|------------|
| T1 | 1 | Define webhook smoke-test contract | — |
| T2 | 2 | Prepare management-repo trigger artifacts | T1 |
| T3 | 3 | Run webhook trigger and observe delivery | T2 |
| T4 | 4 | Record result and handoff evidence | T3 |

---

## T1 — Define webhook smoke-test contract

### Description
Define exactly what this feature uses to prove webhook functionality. The task
sets the expected trigger, expected observable signal, pass/fail criteria, and
evidence that later tasks must capture.

### Required skills

### Subtasks
- [ ] Define the webhook event to trigger.
- [ ] Define expected branch, commit, and optional PR signals.
- [ ] Define the observation point for delivery evidence.
- [ ] Define pass/fail criteria for the smoke test.
- [ ] Document what evidence T4 must preserve.

---

## T2 — Prepare management-repo trigger artifacts

### Description
Create or update the management-repo artifacts needed to produce a controlled
webhook event. The task keeps the trigger scoped to this feature branch and
does not change runtime behavior.

### Required skills

### Subtasks
- [ ] Confirm the feature branch name and task branch names.
- [ ] Add a small trigger artifact or state change tied to the smoke test.
- [ ] Confirm the artifact matches the T1 test contract.
- [ ] Validate markdown/YAML formatting before push.
- [ ] Commit the trigger artifact on the task branch.

---

## T3 — Run webhook trigger and observe delivery

### Description
Push or open the agreed trigger event and observe the webhook receiver or log
stream. The task records the delivery state, payload identity, and any failure
details needed to diagnose webhook behavior.

### Required skills

### Subtasks
- [ ] Push the trigger branch or open the agreed PR event.
- [ ] Observe the webhook receiver, dashboard, or log stream.
- [ ] Capture event id, timestamp, branch, commit, and delivery status.
- [ ] Capture failure response details if delivery fails.
- [ ] Leave the task blocked if no observation point is available.

---

## T4 — Record result and handoff evidence

### Description
Write the smoke-test result into the feature handoff area so the outcome is
auditable. The task should include the trigger reference, observed delivery
evidence, and any follow-up recommendation.

### Required skills

### Subtasks
- [ ] Create a handoff result note for the webhook smoke test.
- [ ] Include trigger branch, commit, and PR references if present.
- [ ] Include observed delivery evidence from T3.
- [ ] Summarize pass/fail result and any follow-up action.
- [ ] Validate the handoff note before review.
