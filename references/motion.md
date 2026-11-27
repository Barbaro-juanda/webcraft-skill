# Motion

Animation decisions for web pages. For video, use `/hyperframes` instead — different medium, different rules.

## When motion earns its place

Motion is justified when it does one of these. If it does none, cut it.

- **Orients** — shows where a thing came from or went (a panel sliding from the edge it belongs to)
- **Sequences** — establishes reading order on first load
- **Confirms** — acknowledges an action the user took
- **Characterizes** — carries the brand's personality in a way static type cannot

Decoration that does none of the four is the single clearest tell of generated design. Scattered hover effects on every card read as noise; one orchestrated page-load moment reads as intent.

## The defaults

- **Entry, not ambient.** Animate things as they arrive. Continuous ambient motion competes with reading.
- **Fast out, slow in.** 150–250ms for anything the user triggered; 400–800ms for narrative entry sequences.
- **Stagger, do not cascade forever.** 40–80ms between siblings. Past six items, stagger the group not the item.
- **One hero moment per page.** Spend the budget in the first viewport, then get quiet.
- **Respect `prefers-reduced-motion`.** Every time. Replace movement with a fade, never with nothing.

## Technique vocabulary

Naming a technique precisely is most of the work. These are the ones worth knowing by name:

| Technique | What it is | Good for |
|---|---|---|
| **Staggered reveal** | Siblings entering in sequence | Lists, grids, nav on load |
| **Kinetic type** | Letterforms animating independently | Hero statements, brand moments |
| **Scroll-driven sequence** | Timeline bound to scroll position | Explaining a process, product tours |
| **Parallax depth** | Layers at different scroll rates | Hero depth without 3D |
| **Mask reveal** | Content appearing through a moving shape | Image intros, section transitions |
| **Match cut** | Shape persists while content changes | Page transitions, state changes |
| **Displacement** | Pixels pushed by a field or cursor | Hero texture, interactive surfaces |
| **Magnetic hover** | Element drawn toward the cursor | CTAs, single focal controls |
| **Marquee / ticker** | Continuous horizontal run | Logo walls, social proof |
| **Count-up** | Numbers animating to value | Stats, only once on entry |
| **FLIP** | Element morphing between two layout states | Expanding cards, filtered grids |
| **Text trail / shuffle** | Characters resolving into final text | Headlines, use at most once |

## Implementation

| Stack | Reach for |
|---|---|
| Single-file HTML | GSAP + ScrollTrigger; Lenis for smooth scroll |
| React / Next | `react-bits` components (see `react-bits.md`), Framer Motion |
| Simple state change | CSS transitions. Do not import a library for a fade. |
| Heavy generative or 3D | Canvas or WebGL, never hand-authored SVG paths |

## The check

Load the page and watch it once at normal speed, then once with the network throttled. If the motion makes the page feel slower rather than more alive, it is decoration. Cut it.
