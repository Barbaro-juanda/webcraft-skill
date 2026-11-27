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
SKILL.md                      the router — intake, routes, delegation
references/
  workflow.md                 step-by-step per page type
  art-direction.md            how to choose a visual direction
  react-bits.md               component catalog by effect
  motion.md                   animation vocabulary and defaults
  sources.md                  using design galleries responsibly
  stack.md                    single-file HTML vs React vs Astro
```

References load on demand, not upfront. That is the whole reason this is a router and not one large file.

## Design notes

**Intake is mandatory.** A page built without positioning is a generic page, however good the execution. The router asks four questions and will not skip them.

**Copy before layout.** Layout built around real words survives contact; layout built around lorem does not.

**Galleries give principles, not pages.** `references/sources.md` covers how to use Awwwards, Cosmos and the rest without producing a copy of someone else's work.

## License

MIT — see `LICENSE`. Attribution for the referenced projects is in `NOTICE`.
