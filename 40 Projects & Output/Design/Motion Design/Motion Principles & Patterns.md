---
title: "Motion Principles & Patterns"
date: 2026-09-10
source: https://app.notion.com/p/New-Design-3c7b3ec8a02280d6aad7c35dc3bc03ea
tags: [design, motion-design, material-design, liquid-glass, animation]
---

Motion as a usability tactic, and the specific patterns each design language offers. Visual counterpart: [[Visual Language — M3 Expressive & Liquid Glass]]. Structural context: [[Scaffold & Breakpoints (Google M3)]].

## The Governing Rule

Motion is one of the six usability tactics documented at [[22 Concepts/usability|Usability — wiki concept page]]. The restraint principle appears three separate times across the source material, once per design system — worth treating as the default posture rather than a caveat.

> **Reserve motion for key moments or unique experiences. Too much is distraction.**

### Hero Moments

One to two key, impactful interactions per experience. Each should be:

- **Focused** — one thing moving, for one reason
- **Brief**
- **Delightful**
- **Surprising**

Everything else stays still.

## Shape Morph

Interactions that highlight state or action — buttons being the clearest case.

- Default `chip` → selected `rounded square`
- The morph *is* the state feedback; it does the work a separate indicator would otherwise do

## M3 Expressive — Progress Indicators

Where Google's expressive motion is most developed.

Prompt vocabulary:

- Sinusoidal curve
- Wavy effect
- Ripple effect
- Scalloped arc

## Liquid Glass — A Material That Moves

Glassmorphism is declared once and sits still; Liquid Glass is simulated every frame. Motion is built into the material rather than added on top. (Source: [What is Liquid Glass?](https://liquidglassdesign.com/what-is-liquid-glass))

### Ambient Motion (always on)

- Specular highlights shift as the device tilts
- Tint and shadow adapt to the content passing underneath

### Morphing Between Views

- Glass shapes morph as the interface changes
- `GlassEffectContainer` (SwiftUI) groups shapes so they blend, share lighting, and morph into one another
- **`matchedGeometry`** — the default transition
- **`materialize`** — simple custom transition

Lineage: the fluid motion language of iPhone X gestures and Dynamic Island.

Same watch-outs as the visual material: one or two glass layers at most, and custom backgrounds interfere with the effect. Because highlights and tint are always moving, glass surfaces use up some of the hero-moment budget just by being on screen — worth factoring in.

## Pane Expand & Resize

Layout behaviour expressed as motion — full detail in [[Scaffold & Breakpoints (Google M3)]].

- Drag UI drives the resize
- **Persistent** — resized state sticks
- **Temporary** — returns to a default pane width

## Open Threads

- The hero-moment budget (1–2 per experience) is asserted but not scoped — per screen, per session, or per product?
- Progress indicators are the only M3 Expressive motion pattern captured so far; the shape-morph and transition systems likely have more.
