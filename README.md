# webcraft

A router skill for Claude Code that builds web pages end to end.

One entry point. It runs intake, picks the route for the kind of page you need, and delegates each step — art direction, copy, build, conversion, SEO — to the specialist skill that owns it.

## What it is not

It is **not** a bundle. webcraft does not contain the skills it routes to; it calls them by name. That keeps it small (a few KB instead of ~11 MB), keeps each dependency updating on its own schedule, and keeps the licensing clean — nothing here redistributes anyone else's work.

The cost: those skills have to be installed for the routes to work. See **Dependencies**.

## Install

```bash
git clone https://github.com/<your-user>/webcraft.git ~/.claude/skills/webcraft
```

Restart Claude Code. Then:

```
/webcraft
```

or just describe the page you want — the description triggers it.

## Dependencies

webcraft routes to these. Missing ones degrade gracefully: it will tell you which step it cannot run.

**Core (from [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills), MIT)**
`landing` · `landing-page-generator` · `copywriting` · `copy-editing` · `content-humanizer` · `brand-guidelines` · `page-cro` · `form-cro` · `signup-flow-cro` · `popup-cro` · `seo-audit` · `schema-markup` · `site-architecture` · `aeo` · `local-seo-manager` · `programmatic-seo` · `pricing-strategy`

**Design (from [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill))**
`ui-ux-pro-max` · `ui-styling` · `design` · `design-system` · `brand` · `banner-design` · `slides`

**Quality gate**
`design-taste-frontend` — art-direction review loop on real screenshots

**Plugins**
`frontend-design` and `playground` from [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) · `hyperframes` from [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) (Apache-2.0), optional, for video

**Component reference**
[react-bits](https://github.com/DavidHDev/react-bits) by David Haz — cataloged in `references/react-bits.md`, not vendored

## Structure

```
SKILL.md                      the router — intake, 8 steps, delegation
references/
  vocabulary.md               plain language → what to actually do
  advisor.md                  the honest review standard
  workflow.md                 step-by-step per page type
  art-direction.md            how to choose a visual direction
  motion.md                   animation + motion graphics + cinematic bridge
  aceternity.md               Aceternity UI catalog
  react-bits.md               react-bits catalog (221 components)
  sources.md                  gallery taxonomies, used responsibly
  stack.md                    single-file HTML vs React vs Astro
```

References load on demand, not upfront. That is the whole reason this is a router and not one large file.

## Design notes

**No jargon required.** Say "hazme algo moderno" and the pipeline runs. `vocabulary.md` translates plain language into decisions — the user never has to know what CRO, AEO or a type scale is.

**Honest by default.** `advisor.md` sets the standard: lead with the most serious problem, separate error from taste, never withhold a verdict, and say "do not build this" when that is the real answer. It applies while building, not only on request.

**Intake is mandatory.** Four questions. A page built without positioning is a generic page, however good the execution.

**Copy before layout.** Layout built around real words survives contact; layout built around lorem does not.

**Cinematic vocabulary, translated.** `motion.md` carries 130+ film technique names and a bridge table mapping each to its web equivalent — a dolly zoom becomes two layers scaling in opposition on scroll, a match cut becomes a FLIP shared-element transition.

**Galleries give principles, not pages.** `sources.md` holds the real filter taxonomies read from Awwwards and the others, and the rule against reproducing their content.

## License

MIT — see `LICENSE`. Attribution for the referenced projects is in `NOTICE`.
