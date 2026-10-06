---
type: source
title: "What Is Liquid Glass? Apple's Design Language, Explained"
author: "liquidglassdesign.com (unattributed)"
date: 2026-08-03
source_type: article
url: https://liquidglassdesign.com/what-is-liquid-glass
ingested: 2026-10-06
tags: [design, ui, apple, material, glassmorphism, usability]
---

## Summary

An explainer on Liquid Glass, the translucent interface material Apple introduced at WWDC 2025 and shipped across iOS 26, iPadOS 26, macOS 26 Tahoe, watchOS 26, tvOS 26 and visionOS 26 — described here as the company's largest visual overhaul since iOS 7 flattened everything in 2013. The article's organizing insistence is that Liquid Glass is a material rather than a color scheme or a filter, and that this is a technical distinction with consequences rather than marketing language.

The distinction rests on optical behavior. Where a conventional frosted panel blurs whatever sits behind it, a Liquid Glass surface bends that content the way a lens would, catches specular highlights that shift as the device tilts, and adapts its own tint and shadow to the content passing underneath. The article's compressed version of the difference: glassmorphism blurs what is behind it, Liquid Glass refracts it. One is declared once in CSS and is identical at rest and mid-animation; the other is simulated per frame. The article dates and credits the older term — glassmorphism, coined by designer Michal Malewicz in November 2020 — and notes that most work posted online as liquid glass on the web is in fact glassmorphism with better lighting, since genuine refraction in a browser requires displacement mapping or a shader rather than `backdrop-filter`.

Two further sections carry most of the article's usable content. The lineage section reads Liquid Glass as Apple consolidating twenty years of its own experiments rather than inventing a look: the glossy depth of Aqua in early Mac OS X, the real-time background blur introduced with iOS 7, the fluid motion language of the iPhone X gestures and the Dynamic Island, and most directly the glass panels of visionOS, where interface surfaces had to sit convincingly inside a real room. Liquid Glass is characterized as that visionOS material brought back down to flat screens. The implementation section gives a fidelity ladder for reproducing it off Apple's platforms, and notes that on Apple's own platforms it is largely handed to the developer through a SwiftUI modifier and a container type.

The section most consequential for this wiki is the critical one, and the article does not soften it. Early betas drew sustained criticism over legibility, and Apple spent the 26.1 releases adding controls to tone the effect down — a more opaque tinted appearance alongside the default clear one, layered on top of the pre-existing Reduce Transparency and Increase Contrast accessibility settings. The article presents this history as something to know before copying the look wholesale, and derives three design principles from it: glass belongs to the layer floating above content and not to content itself, contrast must be checked against the busiest background a surface can land on rather than a convenient one, and restraint reads as intentional while glass on glass on glass reads as a demo.

Provenance caveat, recorded because it bears on how much weight the page can carry: this is a secondhand account, not Apple documentation. The site is a reference gallery for the aesthetic, it links its own resource pages throughout, and it states that every gallery item carries a ready-to-use AI style prompt distilled from its cover. It is therefore a commercially interested party in the popularity of the look it is describing. That interest cuts against the article's own critical passages rather than toward them, which is a reason to take the legibility history seriously; but the datable facts here — release versions, session titles, dates, the Malewicz attribution — are reported without citation and should be treated as needing confirmation from Apple's own material before anything is built on them.

## Key Points

- Liquid Glass is a material, not a color scheme or a filter — the article's central framing claim.
- Introduced at WWDC 2025 on June 9, 2025, alongside the rename of every Apple operating system to year-based numbering (hence iOS 26 rather than iOS 19).
- Shipped across six platforms: iOS 26, iPadOS 26, macOS 26 Tahoe, watchOS 26, tvOS 26, visionOS 26.
- Characterized as Apple's largest visual overhaul since iOS 7 in 2013.
- Introduced in depth by two WWDC sessions: *Meet Liquid Glass* and *Build a SwiftUI app with the new design*.
- Optical behavior is the differentiator: refraction of background content rather than blur, specular highlights that track device motion, and tint and shadow that respond to what passes underneath.
- Shapes morph and merge into one another as the interface changes — the "liquid" half of the name.
- Lineage claimed: Aqua's glossy depth, iOS 7's real-time blur, the iPhone X gesture and Dynamic Island motion language, and most directly visionOS's glass panels, where surfaces had to sit inside a real room.
- **Glassmorphism** is the older, broader term — coined by designer Michal Malewicz in November 2020 and widespread within weeks. It names a look, not a behavior: translucent panel, blurred backdrop, hairline light border, soft shadow.
- On the web glassmorphism is four CSS properties — `backdrop-filter: blur()`, a semi-transparent background, a low-opacity border, a box shadow — and it is static: the blur is the same at rest and mid-animation.
- The operative one-line distinction: glassmorphism blurs, Liquid Glass refracts.
- Real refraction is visually detectable at the edges, because it distorts straight lines running behind the panel.
- On Apple platforms: `.glassEffect()` applies the material to a custom view; `GlassEffectContainer` groups glass shapes so they blend, light consistently and morph between one another — and is the cheaper path, since the container renders the group once rather than each shape separately.
- Web fidelity ladder, lowest to highest: CSS-only (`backdrop-filter`, cheap and universally supported, stops at glassmorphism, no refraction); SVG filters (`feDisplacementMap` driven by a gradient, real refraction without WebGL); WebGL/shaders (closest match, since refraction, chromatic dispersion and highlights are what fragment shaders do); prebuilt framework components for React, Vue and Flutter, plus a native glass effect in Figma.
- **Early betas drew sustained criticism over legibility.** Apple used the 26.1 releases to add a more opaque tinted appearance alongside the default clear one, on top of the existing Reduce Transparency and Increase Contrast accessibility settings.
- The named failure mode is specific and predictable: text on glass over a busy background stops being readable.
- First design principle, derived from that: glass is for the layer that floats above content, not for content itself. Toolbars, tab bars, sheets and controls sit on it; body copy does not.
- Second: contrast is not optional. Check every glass surface against the busiest background it can land on, not a convenient one, and honor Reduce Transparency rather than treating it as an edge case.
- Third: restraint reads as intentional. Interfaces that hold up put glass on one or two layers and leave everything else solid; glass on glass on glass reads as a demo.
- Most of what makes the material distinct only becomes visible once something moves, which is why the source routes understanding it to motion studies.

## Entities Mentioned

- [[21 Entities/apple]] — originator of the material; the subject of the article.
- Michal Malewicz — designer credited with coining "glassmorphism" in November 2020. Mention only; no page. This is one dateable fact with nothing else attached, and it sits below the threshold applied to the nine figures held as mentions from [[23 Sources/duru-rethinking-color-theory-2026]].
- liquidglassdesign.com — the publishing site. Unattributed, no byline; a reference gallery that sells no product but distributes AI style prompts for the aesthetic. Recorded here rather than as an entity page because nothing is known of it beyond its own pages.

## Concepts Mentioned

- [[22 Concepts/liquid-glass]] — the material itself, including the glassmorphism distinction.
- [[22 Concepts/usability]] — the legibility failure and Apple's opacity controls are the wiki's second vendor-side evidence that an expressive default carries a measurable cost.
- [[22 Concepts/color-stimulation]] — the glass failure mode is a light–dark contrast failure, which is one of that model's three properties.
- [[22 Concepts/hierarchy-utility-style]] — "glass belongs to the floating layer, not to content" is a hierarchy rule expressed as a material rule.

## Connections

- [[22 Concepts/usability]] — **Direct bearing on the standing tension there.** Apple shipped an expressive translucent default, took sustained legibility criticism, and added opacity controls in a point release. That is a second vendor paying a measurable price for an expressive default, after [[23 Sources/material-design-testing-m3-2024]] found M3's one loss to M2 was playfulness. Written up there.
- [[21 Entities/material-design]] — the comparison the wiki now supports. Two vendors, two expressive design languages, two different public reckonings with legibility. Material Design's arrives as in-house research; Apple's arrives as a shipped settings toggle.
- [[22 Concepts/color-stimulation]] — **A sharper link than it first appears.** [[23 Sources/duru-rethinking-color-theory-2026]] names "atmosphere" as the technique for lowering stimulation: low light–dark contrast plus gradients and fuzzy boundaries. That is a description of what a glass surface does to everything behind it. Liquid Glass is atmosphere applied to interface chrome, and its documented failure is precisely insufficient light–dark contrast — the same lever, used for gentling in one source and breaking legibility in the other.
- [[22 Concepts/hierarchy-utility-style]] — the floating-layer rule assigns a material to a position in the hierarchy, which is that framework's first dimension arrived at from the material side.

## Quotes

None taken. The passages worth preserving are the three design principles and the glassmorphism distinction, both of which are compressed restatements of the source's own argument rather than quotable formulations, and the source is itself a secondhand account of Apple's material — so it is the wrong document to quote as authority. Summarized above instead. Same treatment as [[23 Sources/duru-halfway-color-combinations-2021]].

## Questions Raised

- Does Apple's own Human Interface Guidance state the floating-layer rule, or is that this author's synthesis? The article attributes the principle to the HIG loosely ("if you take one principle from the HIG") without quoting it.
- What exactly did the 26.1 opacity control change, and was it opt-in or applied by default? The difference matters: a toggle users must find is a very different concession from a changed default.
- Was the legibility criticism borne out in measurement, or was it loud? The source reports sustained criticism and a shipped response but cites no study, no sample and no accessibility audit.
- Does refraction buy anything a user can use, or only something a user can notice? The article argues the material is more faithful to physics than blur is, and never claims this makes anything easier to operate.
- If genuine refraction on the web needs a shader, what is the cost — battery, frame budget, low-end devices — and does the fidelity ladder have a point past which it stops being worth climbing? Not addressed.
- How does a material whose appearance depends entirely on what is behind it get specified in a design system at all? This is [[22 Concepts/color-relativity]]'s problem in an acute form, and neither source raises it.
