# Start Here — Web Standard

Read in this order before changing the site:

1. `PROJECT_SCOPE.md`
2. `CURRENT.md`
3. `OPERATOR_PROTOCOL.md`
4. `AGENTS.md`
5. `QUALITY_GATES.md`
6. active gate / issue
7. active PR, exact head, review findings, and CI

## First setup

1. Complete `templates/PROJECT_INTAKE.md`.
2. Lock visitor, business goal, content, V1 pages, action/conversion path, and non-goals in `PROJECT_SCOPE.md`.
3. Inventory existing brand/content/assets before redesigning anything.
4. Choose the lightest architecture that can truthfully satisfy the site.
5. Put exactly one bounded gate in `CURRENT.md`.
6. Tell Codex only: **`CONTINUE`**.

## Scope test

Before implementation, ask:

> Does this directly improve the active visitor/business outcome in the current gate?

If not, park it in `BACKLOG.md`.

## Complexity test

Before adding a framework, backend, CMS, database, auth, analytics package, or third-party script, ask:

> What real requirement fails without this?

If there is no concrete answer, do not add it.

## Template safety

The untouched template is `NOT_CONFIGURED`. Do not invent pages, brand copy, hosting, tracking, forms, payments, CMS, auth, or a web-app architecture.