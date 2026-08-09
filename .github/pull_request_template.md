## Active gate

`<ID — name>`

## Scope delivered

- 
- 

## Explicitly not changed

- 
- 

## Evidence

- Lint/static checks: `<command + result>`
- Tests/audits: `<command + result>`
- Build/dry-run: `<command + result>`
- Browser/E2E: `<command + result or N/A>`
- Mobile/tablet/desktop evidence: `<result or N/A>`
- Accessibility/performance/SEO/form checks: `<result or N/A with reason>`

## Brand / privacy / production check

- [ ] Approved brand/content direction was preserved unless this gate explicitly changes it.
- [ ] No unnecessary CMS/auth/database/dashboard/tracking/app infrastructure entered the PR.
- [ ] No secret was exposed to client/source/logs/evidence.
- [ ] No production domain/DNS, billing, destructive data/content, or tracking/privacy change occurred outside authority.
- [ ] Every changed file is required by the active gate or a documented repair.

## Risk / rollback

`<one short statement>`

## Handoff

`AWAITING_REVIEW`

Head: `<full SHA>`