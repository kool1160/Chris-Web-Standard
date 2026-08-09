# Quality Gates — Web Standard

## 1. Scope and brand

- Every changed file maps to the active gate or a documented repair.
- No extra page, feature, integration, redesign, tracking tool, or architecture expansion entered the PR.
- Approved brand, copy source, assets, and tone are preserved unless the gate explicitly changes them.

## 2. Visitor workflow

- The primary visitor can understand the page and complete the intended action.
- Navigation, links, forms, downloads, galleries, and calls to action work as intended.
- Loading, empty, success, error, validation, and fallback states are clear where relevant.

## 3. Responsive and accessibility

- Critical content/actions work at documented mobile, tablet, and desktop sizes.
- Keyboard access, focus visibility, labels/names, semantic structure, alt text, and contrast are appropriate to the site.
- Reduced-motion and motion safety are handled when animation is used.

## 4. Performance

- Avoid unnecessary JS and third-party weight.
- Images/media are appropriately sized/optimized.
- Critical layout does not depend on slow optional resources.
- No obvious layout shift, blocking asset, or runaway request was introduced.
- Project-specific performance budgets may tighten these defaults.

## 5. SEO and sharing

When the site is public/indexable:

- useful title/description metadata exists;
- canonical/indexing rules are intentional;
- headings are structurally useful;
- social/share metadata is correct when needed;
- routes return appropriate status/fallback behavior;
- sitemap/robots behavior is correct when applicable.

## 6. Forms, security, privacy

When applicable:

- validate input server-side or at the trusted boundary;
- secrets stay off the client;
- abuse prevention is proportional and does not punish normal users;
- failures never claim a successful submission;
- tracking/cookies/third-party scripts match the approved privacy position;
- private uploads/content are not accidentally public.

## 7. Build and deployment

Run the project's declared lint/static checks, tests, route/content audits, build/dry-run, and browser/E2E checks. Verify production-specific config before changing it; do not guess binding IDs, domains, database IDs, or environment values.

## Definition of done

The intended visitor/business outcome is proven on the exact head, required checks pass, blocking findings are resolved, and the accepted change did not quietly turn the website into a larger product.