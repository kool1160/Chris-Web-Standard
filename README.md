# Chris Web Standard

Reusable operating standard for public websites, business sites, portfolios, landing pages, service sites, and content-driven web experiences.

If the product is primarily an interactive application with persistent user workflows, start from `Chris-App-Standard`. If it is primarily desktop/engineering/system software, start from `Chris-Software-Standard`.

## The rule

**A website should be obvious, fast, trustworthy, accessible, and easy to maintain before it is clever.**

Start with the visitor, business goal, content, conversion/action path, required integrations, V1 pages, non-goals, and proof of success. Do not start by choosing a heavy framework or building a backend the site may never need.

## Operating loop

```text
Owner vision / business decision
          ↓
Review-Control Chat locks one active gate
          ↓
       CONTINUE
          ↓
Codex implements or repairs one bounded pass
          ↓
    AWAITING_REVIEW
          ↓
Review-Control Chat checks exact head + evidence
     ↙                 ↘
CONTINUE            OWNER_DECISION / BLOCKED
```

## Core guardrails

- One repository, one active gate, one implementation PR.
- `CURRENT.md` keeps **IN SCOPE**, **OUT OF SCOPE**, acceptance evidence, and next action visible.
- New pages/features/integrations go to `BACKLOG.md` unless deliberately promoted.
- Prefer static/content-first delivery; add server, database, auth, CMS, analytics, or app-like state only when a real requirement earns it.
- No redesign-by-drift. Preserve the approved brand and visual system unless the active gate is a deliberate redesign.
- Performance, mobile behavior, accessibility, SEO/share metadata, forms, privacy, and broken-link/route behavior are product quality—not cleanup for later.
- Codex stops at `AWAITING_REVIEW`; it does not merge or advance itself.
- Review-Control Chat independently checks the exact head and may perform routine merge/next-gate advancement inside the already-approved plan.
- Production-domain changes, paid services, billing, customer/private data, secrets, tracking/privacy changes, destructive content/data changes, or material business/brand decisions escalate to the owner.

## Start here

1. `START_HERE.md`
2. `templates/PROJECT_INTAKE.md`
3. `PROJECT_SCOPE.md`
4. `CURRENT.md`
5. `OPERATOR_PROTOCOL.md`
6. `QUALITY_GATES.md`

## Standard files

- `START_HERE.md`
- `PROJECT_SCOPE.md`
- `CURRENT.md`
- `OPERATOR_PROTOCOL.md`
- `AGENTS.md`
- `QUALITY_GATES.md`
- `BACKLOG.md`
- `templates/PROJECT_INTAKE.md`
- `templates/GATE.md`
- `.github/pull_request_template.md`
- `sxf/project.sxf.example.yaml`

## Status

**V1 operating foundation is ready to use.** Hosting, framework, CMS, email provider, analytics, database, auth, and build tooling are intentionally chosen from project needs rather than hard-coded into this standard.