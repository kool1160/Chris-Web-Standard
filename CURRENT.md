# Current — Web Standard

**Status:** `NOT_CONFIGURED`

This file answers one question for every agent: **What exactly are we doing right now?**

## Active gate

**Gate:** `<GATE_ID — SHORT NAME>`  
**Issue:** `<#>`  
**PR:** `none`  
**State:** `READY_TO_IMPLEMENT | AWAITING_REVIEW | REPAIR | BLOCKED | COMPLETE | HELD`

## Objective

`<One sentence describing the complete visitor/business outcome this gate delivers.>`

## IN SCOPE

- `<bounded page/feature/content item>`
- `<bounded item>`
- `<bounded item>`

## OUT OF SCOPE

- `<future page/feature>`
- `<redesign/architecture expansion not required here>`
- `<tracking/CMS/auth/backend/etc. not required here>`

## Acceptance evidence

- [ ] Required deterministic/build checks pass.
- [ ] Gate-specific visitor/business behavior is proven.
- [ ] Mobile/responsive behavior is verified where relevant.
- [ ] Accessibility/performance/SEO/form checks required by the gate pass.
- [ ] No broken production route/asset behavior was introduced.
- [ ] No unresolved blocking review finding remains.
- [ ] No out-of-scope behavior entered the PR.

## Review state

**Reviewed head:** `none`  
**CI:** `none`  
**Blocking finding:** `none`

## Next valid action

`COMPLETE PROJECT INTAKE BEFORE IMPLEMENTATION`

## Hard rule

Exactly one active gate. Mentioned, attractive, or easy-to-add features remain out of scope until promoted.