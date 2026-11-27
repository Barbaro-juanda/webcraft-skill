---
name: webcraft
description: "Build any kind of web page end to end — landing pages, marketing sites, product pages, portfolios, pricing pages, app screens — and advise honestly on pages that already exist. Routes the whole pipeline: intake, art direction, copy, build, motion, conversion and SEO, delegating to the specialist skill at each step. Triggers on plain requests with no jargon: 'hazme una página', 'necesito una web', 'algo para vender esto', 'que se vea moderno', 'ponle animaciones', '¿cómo quedó?', 'se ve genérico'. Also for choosing a visual direction, picking a component or effect, reviewing or critiquing a page, or deciding how a site should be built."
license: MIT
metadata:
  version: "2.0.0"
  author: Juan David Escobar
  category: web
---

# webcraft

Router for building and reviewing web pages. You do not build from this file — you run intake, pick the route, and hand each step to the skill that owns it.

## Hard rules

1. **Never make the user learn vocabulary.** They say "que se vea moderno" and you already know what that means. Translate silently, build, then name what you did in plain words. `references/vocabulary.md` is the translation layer — load it whenever a request is vague.
2. **Never skip intake.** Four questions, maximum. A page built without positioning is a generic page however good the execution.
3. **Announce each skill as you invoke it**, and show the result before moving on. No silent pipelines.
4. **Be honest.** When something is bad, say it is bad, say why, say what to do instead. `references/advisor.md` is the standard. This applies while building, not just when asked to review.
5. **Never copy a gallery page.** Extract principles, name what you took. See `references/sources.md`.

---

## Step 0 — Intake (always)

Ask only what you cannot infer. Stop at four.

- **What is it?**
- **Who is it for?**
- **What should they do?** One action. If they name three, make them pick.
- **Brand?** Colors and tone if they exist; "I'll propose one" if not.

Then classify and state your read in one line:

| Signal | Route |
|---|---|
| One page, one offer, one CTA | **Landing** |
| Several pages, nav, content | **Marketing site** |
| Feature or product detail | **Product page** |
| Personal work, showcase | **Portfolio** |
| Plans and tiers | **Pricing** |
| Dashboard, settings, admin | **App screen** |
| A page that already exists | **Review** → go to Step 7 |

`references/workflow.md` has the step-by-step per route.

---

## Step 1 — Art direction

Decide the look before writing markup.

- `ui-ux-pro-max` — palette, type pairing, layout patterns
- `design-taste-frontend` — anti-slop house style and screenshot review loop. **Every public-facing page.**
- `brand-guidelines` — only when a brand already exists
- `design` / `design-system` — tokens, logo, full identity

Read `references/art-direction.md` first. It holds the house rules and the defaults to avoid.

---

## Step 2 — Copy

Copy before layout. Layout built around real words survives; layout built around lorem does not.

`copywriting` → `content-humanizer` → `copy-editing`

---

## Step 3 — Build

| Situation | Stack | Skill |
|---|---|---|
| One page, animated, self-contained | Single-file HTML + GSAP | `landing` |
| Conversion-structured page | Structured HTML | `landing-page-generator` |
| React / Next / Astro | Components | `frontend-design` + the catalogs |
| Interactive tool or configurator | Single-file HTML | `playground` |
| Shopify | Liquid | work in the theme |

`references/stack.md` to choose. `references/aceternity.md` and `references/react-bits.md` for components.

---

## Step 4 — Motion

Load `references/motion.md`. It carries the full animation taxonomy, the motion-graphics catalog, the cinematic technique vocabulary, and the bridge translating film techniques into web behavior.

**One hero moment per page.** Motion must orient, sequence, confirm or characterize — decoration that does none is the clearest tell of generated design.

---

## Step 5 — Conversion

`page-cro` always · `form-cro` if there is a form · `signup-flow-cro` if registration · `popup-cro` only if asked

---

## Step 6 — SEO

`seo-audit` always · `schema-markup` · `site-architecture` for multi-page · `aeo` for AI citation · `local-seo-manager` for physical businesses · `programmatic-seo` for templated pages at scale

---

## Step 7 — Review and advise

This runs on request ("¿cómo quedó?", "se ve genérico", "revísala") **and** proactively while building.

Load `references/advisor.md`. The order:

1. **Does it communicate?** Five seconds: what, for whom, what next
2. **Does it convert?** One action, friction removed, proof near the ask
3. **Does it work?** Mobile, slow connection, keyboard, contrast
4. **Is it designed or assembled?** Direction, or a pile of defaults
5. **Is the craft there?** Spacing rhythm, type detail, motion restraint

Lead with the most serious problem. Separate error from taste. Never withhold a verdict. Say "do not build this" when that is the honest answer.

---

## Step 8 — Video (optional)

`/hyperframes` for motion assets · `remotion-*` when the project is already React

---

## Quick paths

**"Hazme una landing"** → intake → `ui-ux-pro-max` → `copywriting` → `landing` → `page-cro` → `seo-audit`

**"Se ve genérico"** → straight to `design-taste-frontend`. Skip intake; the page exists.

**"¿Cómo quedó?"** → `references/advisor.md`, full review, honest.

**"Necesito un componente que haga X"** → `aceternity.md` and `react-bits.md`, then `ui-ux-pro-max` if nothing fits.

**"Como [sitio famoso]"** → identify the mechanic, build that, name what you took. Never copy.

---

## References

Load on demand.

| File | When |
|---|---|
| `vocabulary.md` | Request is vague or uses no technical terms |
| `advisor.md` | Reviewing, critiquing, or flagging a problem |
| `workflow.md` | Step-by-step per page type |
| `art-direction.md` | Before proposing any visual direction |
| `motion.md` | Any animation, motion graphic or cinematic reference |
| `aceternity.md` | React section blocks and components |
| `react-bits.md` | Standalone effects and backgrounds |
| `sources.md` | Looking for reference or inspiration |
| `stack.md` | Deciding how to build it |
