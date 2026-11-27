# Workflow per page type

The router picked a route in Step 0. This file holds what each one actually runs.

---

## Landing

One page, one offer, one action. The most common job.

1. `ui-ux-pro-max` → direction, palette, type
2. `copywriting` → headline, sections, CTA. Then `content-humanizer`
3. `landing` → build (single-file HTML, GSAP, self-contained)
4. `design-taste-frontend` → look-and-fix loop on screenshots
5. `page-cro` → conversion pass
6. `seo-audit` + `schema-markup`

**Section order that works**, unless the subject argues otherwise: hero that states the thesis → the problem in the visitor's words → the mechanism (how it works, concretely) → proof (numbers, names, faces) → objection handling → single CTA repeated, never competing.

**Do not** put three CTAs with different verbs on one page. Pick one action.

---

## Marketing site

Several pages, navigation, ongoing content.

1. `site-architecture` → URL structure and internal linking **first**. Changing this later is expensive.
2. `ui-ux-pro-max` + `design-system` → tokens, because consistency across pages needs a system, not per-page choices
3. Per page: `copywriting` → build → `page-cro`
4. `seo-audit` across the set, not page by page
5. `aeo` if being cited by AI assistants matters

---

## Product page

Deep detail on one thing.

1. `ui-ux-pro-max` → direction
2. `copywriting` → feature copy that names benefits, not specs alone
3. `landing-page-generator` → structure (it is built for this)
4. `page-cro` → specifically the scroll depth and the point where visitors decide
5. `schema-markup` → `Product` schema, which affects how it appears in search

---

## Portfolio

The work is the content. Design around it, never over it.

1. `design-taste-frontend` → this is where it matters most; portfolios live or die on taste
2. `ui-ux-pro-max` → grid and type only. Keep chrome minimal.
3. `copywriting` → short. Captions, not essays.
4. `landing` → single-file keeps it fast and portable

---

## Pricing

1. `pricing-strategy` → the tiers and what goes in them, before any layout
2. `copywriting` → tier names and the one line under each
3. `landing-page-generator` → structure
4. `page-cro` → specifically the anchor tier and the comparison table
5. `form-cro` if there is a contact-sales path

---

## App screen

Dashboards, settings, inboxes, admin. Scanned and operated, not read.

1. `design-taste-frontend` → it has a separate run and rules for app screens; use that one
2. `ui-styling` → components (shadcn/Radix/Tailwind patterns)
3. `ui-ux-pro-max` → information density, chart types, state encoding
4. Skip `copywriting`; use `copy-editing` on the microcopy instead
5. Skip SEO entirely

**Different craft from a landing page.** Surface summary before detail. Encode state in form as well as number — a pill, a chip, a severity stripe. Semantic color (good / warning / critical) is separate from the brand accent.

---

## Rebuild / restyle an existing page

No intake needed; the page already states its purpose.

1. Read the existing page first. Understand what it is trying to do before changing it.
2. `design-taste-frontend` → diagnose what reads as generic
3. Fix direction before fixing details — a better button on a templated page is still templated
4. `page-cro` → check the rebuild did not lose a conversion mechanic that was working
