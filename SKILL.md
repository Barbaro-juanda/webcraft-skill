---
name: webcraft
description: "Build any kind of web page end to end — landing pages, marketing sites, product pages, portfolios, one-pagers, pricing pages, app screens. Routes the whole pipeline: intake, art direction, copy, build, conversion and SEO, delegating to the specialist skill at each step. Use whenever the user wants to create, design, build, rebuild, restyle, polish or review a web page or site, in any stack (single-file HTML, React, Next.js, Astro, Shopify). Also when they ask for a visual direction, a component for a specific effect, or say a page looks generic, templated or 'AI-made'."
license: MIT
metadata:
  version: "1.0.0"
  author: Juan David Escobar
  category: web
---

# webcraft

Router for building web pages. You do not build the page from this file — you run the intake, pick the route, then hand each step to the skill that owns it.

## Hard rules

1. **Never skip intake.** A page built without positioning is a generic page. Run Step 0 even when the user sounds impatient.
2. **Announce the skill you are invoking at each step.** The user should know what is driving each decision.
3. **Show the result of a step before moving to the next.** No silent pipelines.
4. **Never copy a design wholesale from a gallery.** Galleries are for extracting *principles* — composition, rhythm, type scale, motion logic. See `references/sources.md`.

---

## Step 0 — Intake (always)

Ask only what you cannot infer. Stop at four questions; more than that and the user disengages.

- **What is it?** Product, service, or thing being presented.
- **Who is it for?** The visitor, in one phrase.
- **What should they do?** One action. If the user names three, make them pick the first.
- **Brand?** Colors and tone if they exist; "propose one" if not.

Then classify the job and state your read back in one line before proceeding:

| Signal | Route |
|---|---|
| One page, one offer, one CTA | **Landing** |
| Several pages, nav, content | **Marketing site** |
| Feature/product detail, deep | **Product page** |
| Personal work, showcase | **Portfolio** |
| Plans and tiers | **Pricing** |
| Dashboard, settings, inbox, admin | **App screen** |

Load `references/workflow.md` for the step-by-step of the route you picked.

---

## Step 1 — Art direction

Decide the look before writing markup. Never start with code.

- `ui-ux-pro-max` — palette, type pairing, layout patterns, product-type conventions
- `design-taste-frontend` — the anti-slop house style and the look-and-fix loop on real screenshots. **Use this on every public-facing page.**
- `brand-guidelines` — only when the user already has a brand to respect
- `design` / `design-system` — when the job needs tokens, a logo, or a full identity

Read `references/art-direction.md` before proposing a direction. It holds the house rules and the defaults to avoid.

---

## Step 2 — Copy

Copy before layout. Layout built around real words survives contact; layout built around lorem does not.

- `copywriting` — headlines, section copy, CTAs
- `content-humanizer` — run on everything `copywriting` produces
- `copy-editing` — final pass

---

## Step 3 — Build

Pick the stack, then the builder.

| Situation | Stack | Skill |
|---|---|---|
| One page, animated, self-contained | Single-file HTML + GSAP | `landing` |
| Conversion-structured page | Structured HTML | `landing-page-generator` |
| React / Next / Astro project | Components | `frontend-design` + `react-bits` catalog |
| Interactive explorer or configurator | Single-file HTML | `playground` |
| Shopify theme | Liquid | work in the theme directly |

For animation and component choices, load `references/react-bits.md` and `references/motion.md`.

---

## Step 4 — Conversion

Never hand over a page that has not been through this.

- `page-cro` — every page, always
- `form-cro` — if it has any form that is not signup
- `signup-flow-cro` — if it has registration
- `popup-cro` — only if the user asked for a popup

---

## Step 5 — SEO

- `seo-audit` — every public page
- `schema-markup` — structured data
- `site-architecture` — only for multi-page sites
- `aeo` — when the user cares about being cited by AI assistants
- `local-seo-manager` — physical business with a location
- `programmatic-seo` — template-generated pages at scale

---

## Step 6 — Video (optional)

Only when the page needs motion assets.

- `/hyperframes` — router; picks `product-launch-video`, `motion-graphics`, or another flow
- `remotion-*` — when the project is already React and video belongs in the codebase

---

## Quick paths

**"Just make me a landing"** → Step 0 (4 questions) → `ui-ux-pro-max` → `copywriting` → `landing` → `page-cro` → `seo-audit`. Announce each.

**"This page looks generic"** → straight to `design-taste-frontend`. Skip intake; the page already exists.

**"I need a component that does X"** → `references/react-bits.md`, then `ui-ux-pro-max` if nothing fits.

**"Review my page"** → `design-taste-frontend` + `page-cro` + `seo-audit`, report only.

---

## References

Load on demand, not upfront.

| File | When |
|---|---|
| `references/workflow.md` | Step-by-step per page type |
| `references/art-direction.md` | Before proposing any visual direction |
| `references/react-bits.md` | Choosing a component or effect |
| `references/motion.md` | Any animation decision |
| `references/sources.md` | Looking for reference or inspiration |
| `references/stack.md` | Deciding how to build it |
