---
type: concept
name: "Liquid Glass"
tags: [design, ui, apple, material, glassmorphism, usability]
sources: [liquid-glass-explained-2026]
---

## Definition

Liquid Glass is the translucent interface material Apple introduced at WWDC 2025 and shipped across iOS 26, iPadOS 26, macOS 26 Tahoe, watchOS 26, tvOS 26 and visionOS 26. The distinction its source insists on is that it is a *material* rather than a color scheme or a filter: it is defined by how it behaves optically, not by how it looks in a still image.

Three behaviors constitute it. A Liquid Glass surface **refracts** the content behind it — bending it the way a lens would rather than blurring it. It catches **specular highlights** that shift as the device tilts. And its own tint and shadow **adapt** to whatever content passes underneath. Shapes additionally morph and merge into one another as the interface changes, which is the "liquid" half of the name. The practical consequence is that the material is simulated per frame rather than declared once, and that most of what makes it distinct is invisible until something moves [[23 Sources/liquid-glass-explained-2026]].

## How It Appears in This Wiki

Through one secondhand explainer, not Apple's own documentation — the source is a reference gallery for the aesthetic, which distributes AI style prompts for it. The wiki therefore holds a well-organized account of the material, with the provenance caveat recorded on the source page, and holds nothing from Apple directly.

It enters as the wiki's second major vendor design language after [[21 Entities/material-design]], and its arrival is what makes a comparison possible: two companies, two expressive visual systems, two public reckonings with legibility.

## Liquid Glass vs. Glassmorphism

The source's main analytical move, and the reason the concept is worth a page rather than a note:

| | Glassmorphism | Liquid Glass |
|---|---|---|
| Coined / introduced | Michal Malewicz, November 2020 | Apple, WWDC 2025 |
| What it names | a look | a material behavior |
| Background treatment | blurs it | refracts it |
| State | static — identical at rest and mid-animation | simulated per frame |
| Lighting | a hairline border to catch the edge | specular highlights tracking device motion |
| Web implementation | four CSS properties: `backdrop-filter: blur()`, semi-transparent background, low-opacity border, box shadow | no equivalent primitive; needs displacement mapping or a shader |

The one-line version: glassmorphism blurs what is behind it, Liquid Glass refracts it. The source notes that most work posted online as liquid glass on the web is glassmorphism with better lighting, and gives a detection test — real refraction distorts straight lines running behind the panel, so the edges give it away.

## Lineage

The source reads the material as Apple consolidating twenty years of its own experiments rather than inventing a look: Aqua's glossy depth in early Mac OS X, the real-time background blur introduced with iOS 7, the fluid motion language of the iPhone X gestures and the Dynamic Island, and — most directly — the glass panels of visionOS, where interface surfaces had to sit convincingly inside a real room. Liquid Glass is characterized as that visionOS material brought back down to flat screens, which also explains the emphasis on optical plausibility: a surface that has to hold up against a real room cannot get away with a blur.

## Implementation

On Apple's platforms the material is largely handed to the developer: `.glassEffect()` applies it to a custom view, and `GlassEffectContainer` groups several glass shapes so they blend, light consistently and morph between one another — which is also the cheaper path, since the container renders the group once rather than each shape separately.

Off Apple's platforms it is reconstructed, at four ascending levels of fidelity: CSS-only (cheap, universally supported, stops at glassmorphism — no refraction); SVG filters using `feDisplacementMap` driven by a gradient (real refraction without WebGL); WebGL and fragment shaders (closest match, since refraction, chromatic dispersion and highlights are what shaders are for); and prebuilt framework components for React, Vue and Flutter, plus a native glass effect in Figma for design work.

## The Legibility Problem

The part of the concept with consequences beyond Apple's platforms, and the reason this page links into the wiki's design cluster.

The failure mode is specific and predictable: text on glass over a busy background stops being readable. The material's defining property — that its appearance is determined by whatever is behind it — is also the property that makes it unsafe to specify in advance, because a surface cannot be checked against a backdrop that has not happened yet.

This was not hypothetical. Early betas drew sustained criticism over legibility, and Apple used the 26.1 releases to add controls toning the effect down: a more opaque tinted appearance alongside the default clear one, on top of the pre-existing Reduce Transparency and Increase Contrast accessibility settings. The source presents this history as something to know before copying the look wholesale.

Three principles are derived from it:

- **Glass is for the layer that floats above content, not for content itself.** Toolbars, tab bars, sheets and controls sit on it; body copy does not. This is a hierarchy rule stated as a material rule — see [[22 Concepts/hierarchy-utility-style]].
- **Contrast is not optional.** Check every glass surface against the busiest background it can land on rather than a convenient one, and honor Reduce Transparency rather than treating it as an edge case.
- **Restraint reads as intentional.** Interfaces that hold up put glass on one or two layers and leave everything else solid; glass on glass on glass reads as a demo.

## Key Sources

- [[23 Sources/liquid-glass-explained-2026]] — the only source. Supplies the definition, the glassmorphism distinction, the lineage, the implementation ladder and the legibility history.

## Related Concepts

- [[22 Concepts/usability]] — **The live connection.** Apple shipping opacity controls after beta criticism is the wiki's second instance of a vendor paying a measurable price for an expressive default. Written up there.
- [[22 Concepts/color-stimulation]] — **Closer than it looks.** [[23 Sources/duru-rethinking-color-theory-2026]] names "atmosphere" — low light–dark contrast plus gradients and fuzzy boundaries — as the technique for lowering stimulation. That describes what a glass surface does to everything behind it. Liquid Glass is atmosphere applied to interface chrome, and its documented failure is insufficient light–dark contrast: the same lever, recommended for gentling in one source and breaking legibility in the other.
- [[22 Concepts/color-relativity]] — **The acute case.** Relativity holds that a color has no fixed appearance because the surround changes it. A glass surface has no fixed appearance at all, by construction. Every difficulty relativity raises for fixed color tokens is sharper here, and neither source connects them.
- [[22 Concepts/hierarchy-utility-style]] — the floating-layer rule assigns a material to a position in the hierarchy, reaching that framework's first dimension from the material side.

## Tensions & Debates

**The defining property is the failure mode.** Refraction and adaptive tint are what distinguish the material from a frosted panel, and dependence on the backdrop is exactly what makes legibility uncontrollable. The source documents both and does not treat them as the same fact. Apple's response — shipping an opaque variant — resolves it by making the material optional rather than by solving it, which is worth recording as the honest outcome.

**Fidelity without a stated benefit.** The implementation ladder is organized entirely by how closely a technique reproduces real refraction, and the source never argues that refraction makes anything easier to use. The implicit claim is that physical plausibility is a good in itself. Against that, [[22 Concepts/usability]]'s source material would ask what task it serves — and nothing in this wiki answers.

**An interested witness on restraint.** The source's own design advice is for less glass, more opacity and more contrast checking, published by a site whose business is distributing style prompts for the look. The advice cuts against the site's interest, which is a reason to credit it. The datable facts around it — versions, dates, session titles, the Malewicz attribution — are uncited and should be confirmed against Apple's own material before anything is built on them.

**No measurement.** The legibility criticism is reported as sustained and the response as shipped, but there is no study, sample or audit anywhere in the source. Compare [[23 Sources/material-design-testing-m3-2024]], which at least states its instrument and its limits. Apple's reckoning is visible in a release note rather than in a paper, which is a different kind of evidence — arguably stronger, since it cost something, and certainly less analysable.

## Open Questions

- Was the 26.1 opacity control opt-in or a changed default? A toggle users must discover is a much smaller concession than a changed default, and the source does not say which it is.
- Does Apple's Human Interface Guidelines state the floating-layer rule, or is it this author's synthesis? Attributed loosely and not quoted.
- What does per-frame simulation cost — battery, frame budget, low-end hardware — and is there a point on the fidelity ladder past which it stops being worth climbing?
- How is a backdrop-dependent material specified in a design system at all? Tokens assume a stable appearance; this material has none.
- Will the retreat hold, or is 26.1 a trough? The wiki is recording a design language mid-revision, and the source is dated 2026-08-03.
