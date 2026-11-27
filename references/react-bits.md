# react-bits — component catalog

[react-bits](https://github.com/DavidHDev/react-bits) by David Haz. 221 animated React components.

This file is an **index**: component names and the effect each produces, so you can pick one fast. It contains no source code from the project.

## License — read before shipping

**MIT + Commons Clause.**

- ✅ Use the components in any website, app or product, **including paid commercial work**. A client landing page is fine.
- ❌ **Do not sell, sublicense or redistribute the components themselves** — alone, bundled, or ported to another framework.

Practically: build client sites with them, yes. Ship them inside a template pack, component library or starter kit you sell — no. That is also why this file is a catalog and not a copy.

## Install

Per component, via their CLI — not as a dependency:

```bash
npx jsrepo add https://reactbits.dev/<Category>/<ComponentName>
```

Requires React. For Tailwind variants see their docs. The source lands in your project and you own the copy.

---

## By what you need

### Hero backgrounds

Pick one. Two animated backgrounds on one page is noise.

| Feel | Components |
|---|---|
| Organic, flowing | `Aurora` · `Silk` · `LiquidEther` · `SoftAurora` · `Waves` · `LineWaves` · `PatternWaves` · `ShapeWaves` · `SlicedWaves` |
| Cosmic, deep | `Galaxy` · `Particles` · `Orb` · `Hyperspeed` · `LightTunnel` · `Prism` · `PrismaticBurst` |
| Technical, grid | `DotGrid` · `DotField` · `RippleGrid` · `GridMotion` · `GridDistortion` · `GridScan` · `MagnetLines` · `Topography` · `ShapeGrid` |
| Retro, glitch | `FaultyTerminal` · `LetterGlitch` · `CRTWarp` · `GradientASCII` · `NeonGlyphs` · `PixelSnow` · `PixelBlast` |
| Material, metallic | `LiquidChrome` · `MoltenMetal` · `Ferrofluid` · `Iridescence` · `HoloMosaic` |
| Light, atmospheric | `LightRays` · `Lightning` · `LightPillar` · `Lightfall` · `SideRays` · `Beams` · `Plasma` · `PlasmaWave` |
| Textured, grainy | `Dither` · `Grainient` · `ColorBends` · `GradientBlinds` · `GradientWaves` |
| Playful | `Ballpit` · `Balatro` · `Antigravity` · `MagicRings` · `EvilEye` · `AcidSquares` |
| Dark, moody | `DarkVeil` · `GhostFibers` · `Threads` · `WebThreads` · `FloatingLines` · `FluxLines` · `MicroSlats` · `AeroShards` · `Radar` · `Scanner` |

### Headline treatments

One per page. Two animated headlines compete.

| Effect | Components |
|---|---|
| Reveal on entry | `SplitText` · `BlurText` · `ScrollReveal` · `ScrollFloat` · `FallingText` · `FoldText` |
| Typewriter / decode | `TextType` · `DecryptedText` · `ScrambledText` · `Shuffle` · `SplitFlapText` |
| Cycling words | `RotatingText` · `TextLoop` · `EchoText` |
| Surface treatment | `GradientText` · `ShinyText` · `StrokeText` · `FuzzyText` · `GlitchText` · `TechText` |
| Spatial | `DepthText` · `WarpText` · `CurvedLoop` · `CircularText` · `TextPressure` · `VariableProximity` |
| Generative | `ASCIIText` · `ParticleText` · `MaskedHeading` |
| Focus / scroll-linked | `TrueFocus` · `ScrollVelocity` · `TextCursor` |
| Numbers | `CountUp` |

### Layout and navigation

| Need | Components |
|---|---|
| Nav bar | `CardNav` · `PillNav` · `GooeyNav` · `StaggeredMenu` · `FlowingMenu` · `BubbleMenu` · `BranchedMenu` |
| Sidebar / dock | `Dock` · `LineSidebar` · `InfiniteMenu` |
| Card grid | `MagicBento` · `Masonry` · `ChromaGrid` · `BounceCards` |
| Carousel | `Carousel` · `FlexCarousel` · `CircularCarousel` · `DepthCarousel` · `MorphSlider` · `CardSwap` · `Stack` |
| Gallery | `CircularGallery` · `DomeGallery` · `AccordionGallery` · `FlyingPosters` · `InfiniteSpiral` · `DriftWall` |
| Scroll structure | `ScrollStack` · `AnimatedList` |
| Stepper / flow | `Stepper` · `Counter` · `OptionWheel` |

### Cards and surfaces

`SpotlightCard` · `TiltedCard` · `PixelCard` · `DecayCard` · `HoloCard` · `ReflectiveCard` · `ProfileCard` · `GlassSurface` · `GlassIcons` · `FluidGlass` · `BorderGlow` · `Folder` · `Lanyard` · `ModelViewer`

### Micro-interactions

Small controls with personality. Use where the interaction itself is the product moment — a submit, a toggle, a rating.

| Kind | Components |
|---|---|
| Buttons | `SpecularButton` · `FuseButton` · `SlingButton` · `FlyingButton` · `HoldButton` · `SlideCommit` |
| Toggles / inputs | `SquishSwitch` · `JellyRadio` · `SpringCheck` · `BellToggle` · `GlideSelect` · `CurvedInput` · `ScrubField` · `WakeSlider` · `ElasticSlider` · `RubberSegment` |
| Feedback | `SwipeToast` · `WarmTooltip` · `StatusMark` · `PulseHeart` · `PeekRating` · `SloshGauge` · `LatticeLoader` |
| Playful physical | `PaperCrumple` · `Shredder` · `TearTicket` · `FlipCard` · `FolderFloat` · `DodgeField` · `SwipeRow` |
| Specialized | `PromptBar` · `VoicePill` · `CodeSlots` · `CallChip` · `CometDial` · `ThoughtLine` · `RefineFrame` |

### Cursor effects

Use at most one, and only when the page is a showcase. On a conversion page a custom cursor usually costs more than it returns.

`SplashCursor` · `BlobCursor` · `GlowCursor` · `GhostCursor` · `SwarmCursor` · `TargetCursor` · `CursorGrid` · `Crosshair` · `ClickSpark` · `ImageTrail` · `PixelTrail` · `Magnet`

### Transitions and reveals

`AnimatedContent` · `FadeContent` · `GradualBlur` · `PixelTransition` · `PixelSwap` · `HalftoneReveal` · `ScrollExpand` · `ShapeBlur` · `RippleDistortion` · `DitherVeil` · `ElasticMesh` · `Noise`

### Brand and logo

`LogoLoop` (logo wall / ticker) · `ElectricLogo` · `NeonLogo` · `MetallicPaint` · `ElectricBorder` · `StarBorder` · `StickerPeel` · `Ribbons` · `Strands` · `MetaBalls` · `Cubes` · `CrystalizedBall` · `OrbitImages` · `LaserFlow`

---

## Choosing well

**One statement effect per page.** A `Galaxy` background plus `ParticleText` plus `SplashCursor` reads as a demo reel, not a product.

**Match the weight to the subject.** WebGL backgrounds (`Galaxy`, `LiquidChrome`, `Prism`) are heavy and dramatic. A B2B SaaS page usually wants `DotGrid` or nothing.

**Check the cost.** Several of these run shaders on every frame. Test on a mid-range phone before shipping, and verify `prefers-reduced-motion` is honored.

**They are React.** For a single-file HTML page, use GSAP directly instead — see `motion.md`.
