# Audit Process — Web Standard

## Audit authority

**The Review-Control Chat is the acceptance auditor. Codex builds; it never accepts its own work.**

Claude / Anthropic is **not** part of the standard audit, review, fallback, or tie-break process. Do not route website work to Claude for audit. If an additional model review is deliberately requested, use an approved OpenAI review path; deterministic and browser evidence remain primary.

## Audit order

Audit the exact pushed PR head in this order.

### 1. Scope audit

Compare the complete diff to `PROJECT_SCOPE.md` and `CURRENT.md`.

Reject unapproved pages, dashboards, portals, auth, CMS, database, analytics/tracking, payment, server infrastructure, redesign, or other future work. Useful ideas go to `BACKLOG.md`.

### 2. Deterministic audit

Run and inspect exact-head checks as applicable:

- format/lint;
- type/static checks;
- unit/integration tests;
- build;
- route/link/asset checks;
- form validation tests;
- dependency/security/secret checks;
- repository policy/guard checks.

### 3. Visitor/browser audit

Verify changed user-facing behavior in a real browser at representative supported widths:

- primary visitor/business action path;
- navigation and broken-route behavior;
- mobile/responsive layout;
- keyboard/focus/accessibility;
- form success/failure/fallback behavior;
- major visual regressions;
- performance-sensitive changes;
- SEO/share metadata when affected.

Use browser E2E/screenshots when the behavior cannot be proven by static checks.

### 4. Privacy / production audit

When applicable, inspect:

- third-party scripts;
- analytics/tracking consent and privacy impact;
- form/provider secrets;
- customer/private data handling;
- environment variables;
- preview versus production separation;
- domain/DNS/deployment boundary.

A successful build or preview does not authorize a production-domain or tracking/privacy change.

### 5. Exact-head review

Review the complete diff against the exact SHA and acceptance criteria. Confirm the site remains obvious, fast, trustworthy, accessible, on-brand, and inside scope.

## Verdicts

Return exactly one:

```text
PASS
Head: <full SHA>
Evidence: <short summary>
Next: routine merge / next approved gate
```

```text
REPAIR
Head: <full SHA>
Finding: <specific blocking defect>
Next: CONTINUE
```

```text
BLOCKED
Head: <full SHA>
Reason: <missing decision/evidence/external prerequisite>
```

Any new commit invalidates the prior audit and requires exact-head review again.

## Principle

**Scope first. Browser truth second. Independent Review-Control judgment. No Claude audit.**