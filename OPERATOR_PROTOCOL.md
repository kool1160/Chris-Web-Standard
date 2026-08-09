# Operator Protocol — Web Standard

## Purpose

Keep website work fast and simple without letting content, design, and technical scope wander.

> **Review-Control Chat decides and reviews. GitHub remembers. Codex implements one bounded pass.**

One repo. One active gate. One implementation PR.

## Review-Control Chat

Owns business/product scope, durable decisions, `PROJECT_SCOPE.md`, `CURRENT.md`, brand/content direction, exact-head review, GitHub findings, and routine merge/next-gate advancement inside the already-approved plan.

It escalates material brand/business decisions, production-domain/DNS changes, tracking/privacy changes, paid services/billing, customer/private data, secrets, destructive content/data actions, or architecture expansion to the owner.

It does not perform normal implementation.

## Codex Implementation Chat

Owns one bounded implementation/repair pass on the active gate and same PR. It adds verification evidence and stops.

It never chooses new pages/features, redesigns the site by drift, merges, advances, deploys production by implication, or approves its own work.

## Normal loop

Review-Control Chat returns:

```text
CONTINUE
Gate: <id/name>
PR: none | #__
Reason: <one sentence>
```

Codex reads GitHub and returns:

```text
AWAITING_REVIEW
Gate: <id/name>
PR: #__
Head: <full SHA>
CI: green | failing | running
Work: <one sentence>
Blocker: none | <one sentence>
```

If a real decision is required, Review-Control returns `OWNER_DECISION`. If valid work cannot proceed, either chat returns `BLOCKED`.

## What Codex does on `CONTINUE`

1. If `CURRENT.md` is `NOT_CONFIGURED` or `HELD`, stop.
2. Repair unresolved blocking review findings first, on the same PR.
3. Repair required CI/build failures second, without expanding scope.
4. If the PR is green and unblocked, refresh exact-head evidence and stop at `AWAITING_REVIEW`.
5. If no PR exists, implement the smallest complete slice allowed by the active gate, open one focused draft PR, and stop.
6. If the needed work conflicts with scope/brand/content truth or requires a missing business/privacy/production decision, stop `BLOCKED`.

`CONTINUE` never means “add anything else that would make the site cooler.”

## What Review-Control does after `AWAITING_REVIEW`

1. Read scope, current gate, issue, full diff, exact head, review threads, and checks fresh.
2. Independently verify visitor/business behavior, brand alignment, and quality gates.
3. If repair is needed, record the exact blocking finding on GitHub and return `CONTINUE` so Codex repairs the same PR.
4. If accepted and routine, merge with exact-head protection, record evidence in `CURRENT.md`, activate exactly one next already-approved gate, and return `CONTINUE`.
5. If complete, return `COMPLETE`.
6. Escalate instead of guessing when advancement changes business scope, brand direction, privacy/tracking, production domain/DNS, customer data, payment/billing, secrets, or material architecture.

## Scope-drift firewall

Send to `BACKLOG.md`:

- extra pages/sections;
- dashboard/portal/app ideas;
- unrelated redesigns;
- new tracking/analytics tools;
- CMS/auth/database additions without a current requirement;
- speculative integrations;
- “while we're here” cleanup not needed by the active gate.

## Routine merge authority

No separate routine `Advance` command is required by this standard. Review-Control may merge an accepted exact head and activate the next already-approved gate. High-risk production/domain/release gates may require explicit owner advancement.