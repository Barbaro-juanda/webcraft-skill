# Choosing the stack

Decide this before building. Changing it mid-project costs more than any other decision on this list.

## The decision

| If | Build it as | Why |
|---|---|---|
| One page, needs to look impressive, user is not a developer | **Single-file HTML** (`landing`) | Opens by double-click, hosts anywhere, no build step, nothing to maintain |
| One page, conversion-focused, plain | **Structured HTML** (`landing-page-generator`) | Same portability, less animation weight |
| The client already has a React/Next codebase | **Components in their stack** | Never introduce a second stack into a working project |
| Several pages, content that changes | **Astro or Next** | Routing and content collections earn their complexity past ~5 pages |
| Interactive tool, calculator, configurator | **Single-file HTML** (`playground`) | Self-contained, shareable, no deploy |
| Shopify store | **Liquid, in the theme** | Fighting the theme system always loses |
| It must be editable by a non-technical person later | **Their CMS / page builder** | A beautiful page they cannot edit becomes a dead page |

## The question that settles most cases

**Who maintains this in six months?**

- The user, who does not code → single-file HTML or their existing CMS
- A developer on their team → their existing stack, no exceptions
- Nobody, it is a campaign page → single-file HTML
- It grows into a product → Next or Astro from the start

## Single-file HTML — the default here

Most of what gets asked for is one page that must look excellent and be easy to host. Single-file wins that case:

- GSAP + ScrollTrigger from CDN for motion, Lenis for smooth scroll
- Tailwind from CDN, or hand-written CSS with custom properties
- Images referenced by filename from the same folder
- No build, no `node_modules`, no deploy pipeline

**Limits to say out loud** before committing: no server-side anything, no CMS, no auth, and past roughly 1500 lines it becomes unpleasant to edit. When the brief implies any of those, pick a real stack now rather than migrating later.

## React / Next

When the project is already React, or it will grow:

- `react-bits` for animated components (see `react-bits.md`)
- `ui-styling` for shadcn/Radix/Tailwind patterns
- `frontend-design` for the UI decisions
- `typescript-lsp` plugin gives real type intelligence while editing

## Hosting

| Build | Host |
|---|---|
| Single-file HTML | Netlify drop, Cloudflare Pages, GitHub Pages — drag and drop |
| Astro / Next static | Vercel, Netlify, Cloudflare Pages |
| Next with server features | Vercel |
| Shopify | It is already hosted |

For a quick share without a host, an Artifact works: the page gets a private URL immediately.
