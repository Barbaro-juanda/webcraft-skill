# Art direction

Read before proposing any visual direction. This file holds the decision logic; `design-taste-frontend` holds the deep house style and the screenshot review loop. Use both — this one to choose, that one to execute and verify.

## The order

1. **Find the subject's own world first.** Every distinctive page comes from the material of what it sells. A protein drink has cans, condensation, gym light, aluminium. A law firm has paper, ink, seals, weight. Before choosing a palette, name three physical things from the subject's world. The direction comes from there, not from a trend.
2. **Write the direction in one sentence** before touching color. "Editorial weight with an industrial accent, like a spec sheet that happens to be beautiful." If the sentence could describe any other client, it is not a direction yet.
3. **Then** pick palette, type, layout — each derived from the sentence.

## Defaults to avoid

These are what AI-generated design currently looks like. If the user explicitly asks for one, give it to them — their words win. If nothing was specified, do not spend the freedom here:

- Warm cream `#F4F1EA` + serif display + terracotta accent
- Near-black + a single acid-green or vermilion pop
- Purple-to-blue gradient hero on white
- Inter or Space Grotesk as the "safe" face
- Emoji as section markers
- Everything centered
- `rounded-lg` on everything
- Accent bar on rounded cards, repeated down the page
- Numbered markers (01 / 02 / 03) on content that is not actually a sequence

## Color

- **4 to 6 tokens, named.** Ground, surface, ink, muted, accent, and one semantic if the page needs state.
- **Neutrals are chosen, not inherited.** A pure mid-grey reads as unconsidered. Bias the greys slightly toward the accent's hue.
- **One accent, used sparingly.** If it fights the ground, shift it analogous or drop saturation — do not swap it for a safer color.
- **Both themes or neither.** If the page commits to one visual world (neon arcade, letterpress invitation), stay single-theme deliberately. Otherwise build light and dark as equal citizens, not an inversion.

## Type

- **Two faces minimum, three if there is data.** Display with character, body that disappears, mono for captions or numbers.
- **System stacks are legitimate.** `ui-serif` gives New York on macOS; `ui-monospace` gives SF Mono. Both are good and load instantly. Reach for a webfont only when the direction needs a specific voice.
- **Running text near 65 characters.** Headings get `text-wrap: balance`. Uppercase labels get letter-spacing.
- **Set a scale and stay on it.** Arbitrary sizes read as unconsidered even when nobody can name why.

## Composition by page type

| Type | Opening move | Rhythm |
|---|---|---|
| Landing | The most characteristic thing in the subject's world — not a headline over a stock photo | Alternating density: dense proof, open breathing room |
| Product page | The product doing its job, in one frame | Spec-sheet precision, consistent intervals |
| Portfolio | The work itself, immediately, no preamble | The grid is the design |
| Pricing | The tiers, legible in one glance | Tight, comparative, tabular numerals |
| Marketing site | A thesis, not a greeting | Each page a different density, same system |
| App screen | Summary before detail; state readable at a glance | Information density over typographic drama |

## Motion

See `motion.md`. One rule here: **spend the boldness in one place.** An orchestrated page-load moment lands harder than scattered hover effects, and scattered effects are themselves a tell of generated design.

## The check before handing over

Ask, honestly: could this exact page belong to a different client in a different industry? If yes, the direction failed — go back to step 1 and find the subject's world again.

Then run `design-taste-frontend` for the screenshot review loop. It catches what reads as templated even when every individual choice was defensible.
