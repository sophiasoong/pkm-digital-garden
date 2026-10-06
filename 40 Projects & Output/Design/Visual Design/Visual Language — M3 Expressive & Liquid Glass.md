---
title: "Visual Language — M3 Expressive & Liquid Glass"
date: 2026-09-10
source: https://app.notion.com/p/New-Design-3c7b3ec8a02280d6aad7c35dc3bc03ea
tags: [design, visual-design, material-design, liquid-glass, shape, color]
---

Two current expressive design languages — Google's M3 Expressive and Apple's Liquid Glass — plus the visual tactics that serve usability. Structure they sit on: [[Scaffold & Breakpoints (Google M3)]]. Their motion counterparts: [[Motion Principles & Patterns]].

## Usability Foundation

The five usability metrics and the full six-tactic set are already documented at [[22 Concepts/usability|Usability — wiki concept page]] — not duplicated here.

Of the six tactics, four are visual and belong to this note:

- **Color** — eye-catching primary / secondary contrast
- **Content** — grouping through containment and sections, with headings and spacing
- **Shape** — mask imagery or fill empty space; adds focus and emotional tone, differentiates elements, signals interaction
- **Size** — the bigger the element, the more important it reads, and the fewer errors it invites
- **Typography** — group similar content under the same font

The remaining tactic, **Motion**, is covered in [[Motion Principles & Patterns]].

## M3 Expressive (Google)

Goal: improve usability by emphasizing key actions and building effective visual hierarchy — with a tone of playfulness, energy, creativity, and friendliness.

> **Watch-out:** too much expression becomes distraction.

### Shape

- Card shape and button shape as primary expressive surfaces
- **State transitions** — default `chip` → selected `rounded square`
- **Split button** — button paired with a menu icon button
- **Badge container** — number badge
- **Background illustration**

### Dynamic Color

> **Watch-out:** in a rich palette, hierarchy is easy to lose.

Use contrast plus surface tone — primary, secondary, and tertiary containers and their on-container pairs — so the main action or element stays visually dominant.

### Material Shape Library

35 shapes — https://m3.material.io/m3/pages/shape/overview-principles

Reference: [M3 Expressive update](https://m3.material.io/blog/building-with-m3-expressive#what-rsquo-s-in-the-update)

## Liquid Glass (Apple)

### What It Is

A **material**, not a color scheme or filter. Introduced at WWDC 2025 (June 9) and shipped across every Apple platform's 26 release — iOS, iPadOS, macOS Tahoe, watchOS, tvOS, visionOS. Apple's biggest visual overhaul since iOS 7 went flat in 2013.

Feature: the optical properties of glass combined with fluidity. Rather than blurring what's behind it, the surface bends that content like a lens, catches specular highlights that shift as the device tilts, and adapts its own tint and shadow to whatever passes underneath.
Goal: focus, hierarchy, harmony, consistency.

Lineage: Aqua's glossy depth (early Mac OS X) → iOS 7 real-time blur → iPhone X gesture motion and Dynamic Island → visionOS glass panels, adapted to flat screens.

### Liquid Glass vs. Glassmorphism

| | Glassmorphism (Michal Malewicz, 2020) | Liquid Glass (Apple, 2025) |
|---|---|---|
| Background | Blurred | Refracted |
| Highlights | Static hairline border, soft shadow | Specular, tracks device motion |
| Tint & shadow | Fixed | Responds to content underneath |
| Shape | Static | Morphs as the interface changes |
| Rendering | Declared once | Simulated per frame |

> "Glassmorphism blurs what is behind it, Liquid Glass refracts it."

### Where It Applies

Glass is for the layer that floats **above** content — never the content itself, and never body copy.

- System framework: bars, sheets, popovers
- Controls: button, toggle, stepper, slider, segmented control, picker, text field
- Navigation Stack, Navigation Split View, title bar, toolbar, tabs

### Design Rules

> **Alert:** avoid overuse. Restraint reads as intentional.

- **Main failure mode:** text on glass over a busy background becomes unreadable
- **Contrast is mandatory** — test every glass surface against the busiest background it could sit on
- **One or two glass layers, max** — stacked glass reads as a demo, not a product
- **Accessibility is a standard case, not an edge case** — honor Reduce Transparency and Increase Contrast. Early betas drew legibility complaints; Apple responded in the 26.1 releases with more opaque tinted variants
- Custom backgrounds that overlay the material can interfere with the glass effect

### How It's Built

**Apple platforms (SwiftUI)**
- `.glassEffect()` — applies the material to a custom view
- `GlassEffectContainer` — groups shapes so they blend, share lighting, and morph together

**Web** — four approaches; the first three rise in fidelity:
1. CSS `backdrop-filter` — glassmorphism only, no refraction
2. SVG filters (`feDisplacementMap`) — real refraction without WebGL
3. WebGL / shaders — closest match, including chromatic dispersion
4. Framework components — prebuilt React, Vue, Flutter, and Figma implementations

### Prompt Vocabulary

Keywords: glassmorphism · soft frost glass · smooth gradients · gentle lighting · pastel color palette

Subjects to prompt against: color · light · shape · dimension

Note: by the distinction above, these keywords describe the older, static glassmorphism look. To get true Liquid Glass references, prompt for what's different — refraction, lens distortion, specular highlights, content-reactive tint.

### References

- [What is Liquid Glass?](https://liquidglassdesign.com/what-is-liquid-glass) — explainer: definition, lineage, glassmorphism comparison, build approaches, design rules
- [Liquid Glass Design Inspiration](https://liquidglassdesign.com/) — gallery with AI style prompts per look
- [Glass — Liqui Design handbook](https://liqui.design/docs/handbook/glass) — what the material needs from your layout, and where it degrades
- [Adopting Liquid Glass — Apple Developer](https://developer.apple.com/documentation/technologyoverviews/adopting-liquid-glass)

## Open Threads

- XR / spatial devices are noted in the source but not yet developed — though Liquid Glass itself descends from visionOS glass panels, so that's a natural place to start.
- M3 Expressive and Liquid Glass both claim hierarchy as their goal but reach it differently — M3 through tonal containers, Apple through optical depth. Worth testing whether they can coexist in one product or whether picking one is forced.
