---
type: entity
name: "Apple"
kind: org
tags: [design, technology, apple, design-system, ui]
sources: [liquid-glass-explained-2026]
---

## Overview

Apple enters this wiki as the originator of [[22 Concepts/liquid-glass]], the translucent interface material introduced at WWDC 2025 and shipped across six operating systems in 2025–2026. Coverage is narrow by construction: one secondhand explainer about one design language, with nothing from Apple's own documentation ingested yet. The company's hardware, business and history are not covered and should not be assumed from this page.

What the single source does support is a comparison the wiki could not make before. Apple is now its second vendor design language alongside [[21 Entities/material-design]], and the two reached a similar problem — an expressive visual default running into legibility — by different routes and resolved it in different registers: Google's arrives as a published research instrument, Apple's as a settings toggle in a point release.

## Key Facts

- Introduced Liquid Glass at WWDC 2025 on June 9, 2025, alongside renaming every operating system to year-based numbering — hence iOS 26 rather than iOS 19. [[23 Sources/liquid-glass-explained-2026]]
- Shipped the material across six platforms: iOS 26, iPadOS 26, macOS 26 Tahoe, watchOS 26, tvOS 26 and visionOS 26. [[23 Sources/liquid-glass-explained-2026]]
- The source characterizes it as the company's largest visual overhaul since iOS 7 flattened everything in 2013. [[23 Sources/liquid-glass-explained-2026]]
- Introduced it in depth through two WWDC sessions: *Meet Liquid Glass* and *Build a SwiftUI app with the new design*. [[23 Sources/liquid-glass-explained-2026]]
- Exposes it to developers through SwiftUI as the `.glassEffect()` modifier and `GlassEffectContainer`, the latter grouping glass shapes so they blend, light consistently and morph between one another, and rendering the group once rather than each shape separately. [[23 Sources/liquid-glass-explained-2026]]
- **Took sustained public criticism over legibility during the early betas, and responded in the 26.1 releases** by adding a more opaque tinted appearance alongside the default clear one — on top of the pre-existing Reduce Transparency and Increase Contrast accessibility settings. [[23 Sources/liquid-glass-explained-2026]]
- Maintains Human Interface Guidelines containing its adoption guidance for the material; the source refers to them but does not quote them. [[23 Sources/liquid-glass-explained-2026]]
- The source reads the material as consolidating twenty years of Apple's own work — Aqua's gloss, iOS 7's real-time blur, the iPhone X gesture and Dynamic Island motion language, and visionOS's glass panels — rather than as a new invention. [[23 Sources/liquid-glass-explained-2026]]

## Appearances

- [[23 Sources/liquid-glass-explained-2026]] — not Apple's own voice. A third-party reference gallery explaining Apple's material, including a critical account of its reception that Apple's documentation would be unlikely to carry.

## Connections

- [[22 Concepts/liquid-glass]] — the material itself; the whole of Apple's presence in this wiki so far.
- [[21 Entities/material-design]] — **The structural comparison.** Two vendors pursuing expressive visual systems and both running into legibility. Each reckoned with it publicly in a different form: in-house research with stated limits versus a shipped opacity control.
- [[22 Concepts/usability]] — Apple's 26.1 retreat is evidence in the standing tension there about whether expressive visual defaults serve or cost usability.
- [[22 Concepts/color-stimulation]] — the glass legibility failure is a light–dark contrast failure, which is one of that model's three properties.

## Contradictions

*(None between sources — only one source mentions Apple so far.)*

One internal tension worth recording, since it is about Apple's own actions rather than about disagreeing sources: the property that defines the material is the property that breaks it. Refraction and adaptive tint are what separate Liquid Glass from a frosted panel, and dependence on the backdrop is exactly what makes legibility impossible to guarantee in advance. Shipping an opaque variant in 26.1 makes the material optional rather than fixing it. Documented on [[22 Concepts/liquid-glass]].
