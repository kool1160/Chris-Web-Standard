# Agent Instructions — Web Standard

## Authority order

1. Explicit owner instruction for the current decision
2. `PROJECT_SCOPE.md`
3. `CURRENT.md`
4. `OPERATOR_PROTOCOL.md`
5. `AUDIT_PROCESS.md`
6. `AGENTS.md`
7. active gate / issue
8. active PR, exact head, review threads, CI
9. `QUALITY_GATES.md`
10. `BACKLOG.md`
11. historical notes

Conflict means `BLOCKED`.

## Permanent rules

- One active gate and one implementation PR.
- Codex implements or repairs only what `CURRENT.md` allows.
- Preserve approved brand/content direction unless redesign is the explicit gate.
- Prefer the lightest architecture that satisfies the site.
- Do not add CMS, database, auth, dashboard, customer portal, analytics, tracking, payment, or server infrastructure without a current requirement.
- Do not introduce third-party scripts casually; every one adds performance, privacy, security, and maintenance cost.
- Forms validate on the appropriate boundary, fail clearly, resist obvious abuse, and never expose secrets.
- No secrets in client code, source, logs, screenshots, prompts, fixtures, or CI.
- No real private/customer data in public tests or evidence.
- Production domain/DNS, tracking/privacy, paid service, billing, destructive content/data change, or externally visible release action follows its explicit authority boundary.
- New ideas and unrelated cleanup go to `BACKLOG.md`.
- Builder confidence is not independent review.
- **Claude / Anthropic is not used for standard audit, review, fallback, or tie-breaking.** Follow `AUDIT_PROCESS.md`.

## Codex stop condition

After one bounded implementation/repair pass is pushed with evidence, stop at `AWAITING_REVIEW`. Do not start another page, feature, redesign, or optimization pass.