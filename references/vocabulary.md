# Plain language → what to actually do

The user does not need to know the jargon. They say "que se vea moderno" and the skill is expected to know what that means and run the whole pipeline. This file is the translation layer.

**Rule: never make the user learn vocabulary to get a result.** Translate silently, build, and then name what you did — that is how they learn it, if they want to.

---

## Requests that mean "run everything"

Any of these is a full-pipeline request. Do not answer them with a question about which skill to use.

> "hazme una página" · "necesito una web" · "una landing" · "algo para vender esto" · "una página para mi negocio" · "quiero mostrar mi trabajo" · "algo donde la gente pueda contactarme"

→ Intake (4 questions) → direction → copy → build → CRO → SEO. Announce each step. Never stop halfway to ask permission to continue.

---

## Look and feel

| They say | They mean | Do this |
|---|---|---|
| "moderno" / "actual" | Current conventions, not dated | Generous whitespace, strong type scale, restrained palette, one motion moment. **Not** gradients-everywhere — that reads as 2021. |
| "limpio" / "minimalista" | Less, but considered | Fewer elements, more space, one accent. Minimal is harder — precision in spacing carries it. |
| "elegante" / "premium" / "de lujo" | Restraint plus craft | Serif display, tight tracking, deep neutrals, slow motion, lots of air. Never neon, never busy. |
| "llamativo" / "que impacte" | High contrast, bold scale | Oversized type, saturated accent, one dramatic hero effect. |
| "profesional" / "serio" / "corporativo" | Trustworthy, low risk | Conservative palette, grid discipline, real photography, minimal motion. |
| "divertido" / "fresco" / "juvenil" | Playful | Rounded forms, bright palette, springy easing, personality in microcopy. |
| "futurista" / "tech" | Technical register | Mono accents, dark ground, grid/dot backgrounds, glow, precise motion. |
| "cálido" / "cercano" / "humano" | Approachable | Warm neutrals, soft shapes, real faces, friendly copy. |
| "caro" | Looks expensive | Space + restraint + one perfect detail. Expensive is what you leave out. |
| "que no parezca hecho con IA" | Avoid the defaults | Go straight to `design-taste-frontend`. Read the avoid-list in `art-direction.md`. |

## Motion

| They say | Do this |
|---|---|
| "que tenga movimiento" | One hero entrance + scroll reveals. Nothing ambient. |
| "que se mueva al bajar" | Scroll-triggered reveals; consider a pinned section. |
| "animaciones chéveres" / "efectos" | Pick **one** statement effect from `motion.md`, not several. |
| "que sea interactivo" | Hover states + one cursor or drag interaction. |
| "como [sitio famoso]" | Identify the underlying technique, build that — never copy the page. Name what you took. |
| "algo en 3D" | Ask first whether it is decoration or content. 3D costs load time; it must earn it. |
| "suave" | Lenis smooth scroll + ease-out everywhere + longer durations. |
| "rápido" / "con energía" | Short durations, ease-in, tight stagger, snappy snaps. |

## Structure

| They say | They mean |
|---|---|
| "una sola página" | Landing — one offer, one CTA |
| "varias secciones" | Still one page; they mean scroll depth |
| "un sitio completo" | Multi-page → run `site-architecture` first |
| "que se vea bien en celular" | Mobile-first is the default, not a feature. Build it that way and say so. |
| "que cargue rápido" | Budget the motion. Say out loud what a WebGL background costs. |
| "quiero un blog" | Multi-page + CMS question → `stack.md` |
| "que la gente me escriba" | Form → `form-cro` is mandatory |
| "quiero vender" | E-commerce or checkout link → different build, ask which |

## Content

| They say | Do this |
|---|---|
| "ponle un texto bonito" | `copywriting` — then `content-humanizer`. Never lorem. |
| "no sé qué poner" | Run the copy intake. Four questions produce real copy. |
| "arregla el texto" | `copy-editing` |
| "que salga en Google" | `seo-audit` + `schema-markup`. Explain it takes weeks, not days. |
| "que lo recomiende ChatGPT" | `aeo` |
| "ponle fotos" | Ask: real photos, stock, or generated. Real wins when they exist. |

## Review

| They say | Do this |
|---|---|
| "¿cómo quedó?" | Run the honest review in `advisor.md`. Not reassurance. |
| "no me convence" | Diagnose before changing. Usually direction, not details. |
| "algo le falta" | Almost always: contrast in the type scale, or whitespace. Check those first. |
| "se ve genérico" | `design-taste-frontend`. The direction failed, not the execution. |
| "¿está bien así?" | Give the real answer, including when it is "no". See `advisor.md`. |

---

## How to answer a vague request

1. **Do not interrogate.** Four intake questions, maximum. More and they disengage.
2. **Propose, do not ask open questions.** Not "what colors do you want?" but "I'd go deep green with warm neutrals — it fits a product like this. Want something brighter?" A proposal is easier to react to than a blank field.
3. **Translate silently.** Do the work, then say what you did in plain words: "I used a slow entrance and lots of space so it reads as expensive."
4. **Teach only on request.** If they ask why, explain. Otherwise just deliver.

## Never require the user to

- Know what CRO, AEO, schema or a type scale is
- Choose a stack
- Supply hex codes
- Name an animation technique
- Know which skill does what
