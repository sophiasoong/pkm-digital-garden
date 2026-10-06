---
title: "What Is Liquid Glass? Apple's Design Language, Explained"
source: "https://liquidglassdesign.com/what-is-liquid-glass"
author:
published: 2026-08-03
created: 2026-10-06
description: "Liquid Glass is the translucent material Apple introduced at WWDC 2025 and shipped across iOS 26, iPadOS 26, and macOS 26 Tahoe. What it is, where it came from, how it differs from glassmorphism, and how it's built."
tags:
  - "clippings"
status: ingested
wiki_source: "[[23 Sources/liquid-glass-explained-2026]]"
---
## What is Liquid Glass?

Apple’s translucent interface material, introduced at WWDC 2025 — what it actually is, where it came from, and how it differs from the glassmorphism that preceded it.

## The short answer

Liquid Glass is a material, not a colour scheme or a filter. It is the translucent surface Apple introduced at WWDC 2025 and shipped across iOS 26, iPadOS 26, macOS 26 Tahoe, watchOS 26, tvOS 26, and visionOS 26 — the company’s largest visual overhaul since iOS 7 flattened everything in 2013.

What separates it from every frosted panel that came before is that it behaves optically. Rather than blurring whatever sits behind it, a Liquid Glass surface *bends* that content the way a real lens would, catches specular highlights that shift as you tilt the device, and adapts its own tint and shadow to whatever is passing underneath. Move the content, and the glass responds. It is closer to a simulated physical object than to a CSS effect.

## Where it came from

Apple showed it first at WWDC 2025 on June 9, alongside a rename of every operating system to year-based numbering — hence iOS 26 rather than iOS 19. Two sessions introduced it in depth: *Meet Liquid Glass* and *Build a SwiftUI app with the new design*.

The lineage is longer than one keynote, though. You can read Liquid Glass as Apple consolidating twenty years of its own experiments: the glossy depth of Aqua in early Mac OS X, the real-time background blur that arrived with iOS 7, the fluid motion language of the iPhone X gestures and the Dynamic Island, and — most directly — the glass panels of visionOS, where interface surfaces had to sit convincingly inside a real room. Liquid Glass is that visionOS material brought back down to flat screens.

The reception was not universally warm. Early betas drew sustained criticism over legibility, and Apple spent the 26.1 releases adding controls to tone the effect down — a more opaque tinted appearance alongside the default clear one, on top of the existing Reduce Transparency and Increase Contrast accessibility settings. That history is worth knowing before you copy the look wholesale.

Apple’s own guidance on adopting it lives in the [Human Interface Guidelines](https://liquidglassdesign.com/resources/human-interface-guidelines).

## Liquid Glass vs. glassmorphism

These get used interchangeably and they are not the same thing.

**Glassmorphism** is the older and broader term, coined by designer Michal Malewicz in November 2020 and everywhere within weeks. It describes a look: a translucent panel, the background behind it blurred, a hairline light border to catch the edge, a soft shadow for lift. On the web it is four CSS properties — `backdrop-filter: blur()`, a semi-transparent background, a low-opacity border, a box shadow. It is static. The blur is the same whether the panel is at rest or mid-animation.

**Liquid Glass** is Apple’s 2025 evolution of that idea into something dynamic. The distinction that matters: glassmorphism blurs what is behind it, Liquid Glass refracts it. Add specular highlights that track device motion, tint and shadow that respond to the content passing underneath, and shapes that morph and merge into one another as the interface changes, and you have a material that is simulated per frame rather than declared once.

Practically: most of what gets posted online as “liquid glass” on the web is glassmorphism with better lighting. Genuine refraction in a browser needs displacement mapping or a shader, not `backdrop-filter`. Both are well represented in the [UI gallery](https://liquidglassdesign.com/ui), and the difference is easy to see once you know to look for the edges — real refraction distorts straight lines running behind the panel.

## How it's built

On Apple platforms it is largely handed to you. In SwiftUI the `.glassEffect()` modifier applies the material to a custom view, and `GlassEffectContainer` groups several glass shapes so they blend, light consistently, and morph between one another — which is also the cheaper path, since the container renders the group once rather than each shape separately.

On the web there is no equivalent primitive, so the effect is reconstructed. The approaches in circulation, roughly in order of fidelity:

- **CSS only** — `backdrop-filter` with a layered border and highlight. Cheap, universally supported, and stops at glassmorphism: no refraction.
- **SVG filters** — `feDisplacementMap` driven by a gradient to bend the backdrop at the edges. Real refraction with no WebGL. See [Liquid Glass SVG filters](https://liquidglassdesign.com/resources/liquid-glass-svg-filters).
- **WebGL / shaders** — the closest match, since refraction, chromatic dispersion, and highlights are what fragment shaders are for. [Liquid Glass Studio](https://liquidglassdesign.com/resources/liquid-glass-studio) is the most complete web recreation; [Liquid Glass Vue](https://liquidglassdesign.com/resources/liquid-glass-vue) is a smaller Vue 3 take on the same idea.
- **Framework components** — prebuilt implementations for [React](https://liquidglassdesign.com/resources/liquid-glass-react) and [Flutter](https://liquidglassdesign.com/resources/flutter-liquid-glass), and a native glass effect in [Figma](https://liquidglassdesign.com/resources/glass-effect-playground) for design work.

Every one of these is collected in [Resources](https://liquidglassdesign.com/resources).

## Designing with it

The failure mode is uniform and predictable: text on glass over a busy background stops being readable. Apple ran into it publicly enough to ship opacity controls in a point release. If you take one principle from the HIG, take this one — glass is for the layer that floats above content, not for the content itself. Toolbars, tab bars, sheets, and controls sit on it. Body copy does not.

Two more worth internalising. Contrast is not optional: check every glass surface against the busiest background it can land on, not a convenient one, and honour Reduce Transparency rather than treating it as an edge case. And restraint reads as intentional — the interfaces that hold up put glass on one or two layers and leave everything else solid. Glass on glass on glass reads as a demo.

## See it in practice

The rest of this site is the reference library: [UI design](https://liquidglassdesign.com/ui) for interfaces and components, [Art](https://liquidglassdesign.com/art) for generative and illustrative work in the same visual language, and [Video](https://liquidglassdesign.com/video) for motion studies — where the material is easiest to understand, since most of what makes Liquid Glass distinct only shows up once something moves.

Every gallery item carries a ready-to-use AI style prompt distilled from its cover, so you can generate new visuals in the same style rather than only looking at existing ones. [Browse the full gallery →](https://liquidglassdesign.com/)