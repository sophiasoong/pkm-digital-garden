---
type: source
title: "Rethinking Color Theory"
author: "Ruxandra Duru"
date: unknown
source_type: article
url: https://design.google/library/color-theory-ruxandra-duru
ingested: 2026-10-05
tags: [design, color, color-theory, perception, emotion, google-design]
---

## Summary

Published on Google Design by Ruxandra Duru, co-creator of the Color Moods tool, this article sets out a three-step method for composing color palettes: **balance the stimulation, relate the colors, complete them**. Its distinguishing move is to bracket that rational method with explicitly emotional gut checks — the author opens by instructing the reader to listen to the immediate feeling a scheme generates, and closes by insisting that wherever logic leads, the spontaneous emotional response decides. Nostalgia, bittersweetness and sadness are singled out as *stronger* indicators of a successful palette than joy, a claim supported by reference to Susan Cain's *Bittersweet* and Christopher Alexander's *The Nature of Order*.

Before the method, the article does two pieces of conceptual work that are arguably sharper than the method itself. First it attacks what it treats as a false dichotomy in how designers conceive of color: at one end "colorful," meaning joyful color at maximal intensity, and at the other the supposedly sophisticated safety of blacks, whites, grays and neutrals. This framing, the author argues, skips the vast middle of the intensity spectrum where the genuinely useful colors live — the terra-cottas, butters and sea blues that have few default names and that nature is overwhelmingly composed of. Second, it argues that analyzing colors individually is near-useless because color is relative: the visual system actively pushes neighboring hues, lightnesses and intensities apart, and no backdrop is truly neutral. Two illusions demonstrate a single continuous strip reading as two different colors depending only on what sits behind each end.

The method itself treats stimulation as a calculable quantity rising with three properties — overall intensity, hue distance, and light-dark contrast — operated like sliders on a mixing board, where pushing one up invites bringing another down. The target is the middle of the range, since both under- and overstimulation produce unwanted responses (apathy, irritation, overwhelm). Relatedness is then achieved by restricting one property at a time to give a palette its "glue," optionally via bridge colors or an imaginary colored light. Completion covers complementary logic, extended beyond hue to lightness and temperature, with the notable observation that satisfaction is heightened when the proportions are dramatically unequal — a pinch of cool in a wash of warm.

## Key Points

- Three-step method: **balance the stimulation → relate → complete**, bracketed by emotional gut checks at both ends.
- Stimulation rises with overall **intensity**, **hue distance**, and **light-dark contrast**; these behave like mixing-board sliders and should be balanced against one another.
- Both extremes of stimulation are failure states: understimulation reads as apathy, overstimulation as irritation or overwhelm. Aim for the middle.
- **Intensity (chroma)** is distinct from **saturation** — a fully saturated color can have low intensity.
- Pure hues have *different inherent lightness*: yellow reads near white, purple near black.
- The **"vibrant by default" bias**: treating color as either maximal-intensity "colorful" or safe neutral skips the middle of the intensity spectrum, where most usable and most natural colors sit.
- Color is relative. The visual system pushes neighboring hue, lightness and intensity apart; the effect strengthens when one color surrounds another; no backdrop is perfectly neutral.
- **Relatedness** comes from restricting one property at a time (hue, intensity, or lightness). More shared properties means more harmony but also more predictability — some dissonance adds welcome surprise.
- A **bridge color** ties intact colors together: a more muted color reading as a mixture of the parent hues.
- **Completion** is not hue-only — dark completes light, cool completes warm — and is most satisfying at dramatically unequal proportions.
- **Vibration** is the named exception to the contrast rule: vibrant contrasting hues at the *same* lightness read as unpleasantly overstimulating.
- **Atmosphere** is produced by low light-dark contrast plus gradients and fuzzy boundaries; it gentles even vivid color.
- Scale affects stimulation independently of color choice; micro-shifts of color in natural surfaces add a subtle stimulation flat color lacks.

## Entities Mentioned

- [[21 Entities/ruxandra-duru]] — author; visual designer, co-creator of Color Moods, works with Google designers on color, emotion and UX.
- [[21 Entities/color-moods]] — her tool, presented as the operational implementation of this article's stimulation model.

Cited but not given their own pages (single mentions, insufficient substance for a grounded page):
Josef Albers (*Interaction of Color*, credited as "the original color relativity manual"), Johannes Itten (*The Elements of Color*), Riccardo Falcinelli (*Chromorama*), Ingrid Fetell Lee (*Joyful*, named as the source of the stimulation framing), Susan Cain (*Bittersweet*), Christopher Alexander (*The Nature of Order*), Joel Meyerowitz (paired B&W/color photographs), Gerhard Richter (the leave-it-on-the-wall gut check), Donald Kaufman (the phrase "re-creating light").

## Concepts Mentioned

- [[22 Concepts/color-stimulation]] — the article is this concept's primary source; supplies the three-property model and the whole balance/relate/complete method.
- [[22 Concepts/color-relativity]] — argued at length as the precondition for the method: there is no point assessing a color alone.
- [[22 Concepts/usability]] — not named, but the article's position on color's role conflicts with Material Design's treatment of the same tactic. See Connections.

## Connections

- [[23 Sources/duru-halfway-color-combinations-2021]] — Same author, five years earlier. This article lists "Two-Color Combinations: A Toolkit" as the origin of Color Moods, placing the earlier Medium work upstream of this framework. The 2021 piece's conclusion — that value and saturation choices alter mood more than the hue pair does — is this article's stimulation model in embryo.
- [[22 Concepts/usability]] — **Tension.** Material Design's usability page lists color as "eye-catching" primary/secondary contrast and M3 Expressive pushes dynamic, bold palettes; this article argues the vivid default is a conceptual trap and locates the useful range in the muted middle. Both are Google-published. Documented in both concept pages.
- [[22 Concepts/attentive-perception]] — Resonance rather than argument. The passages on micro-shifts of color in natural surfaces, and on Meyerowitz's photographs showing how color "infuses everything," share the Blake quatrain's move of finding richness by attending closely to the small. Neither source makes a claim about the other.

## Quotes

> "There is no such thing as a perfectly neutral backdrop."

## Questions Raised

- Is stimulation genuinely calculable, or is the mixing-board model a teaching metaphor? The article offers no formula or units, and colormoods.co is cited as the implementation without specifying how the three properties are weighted.
- The "vibrant by default" critique is aimed at designers generally, but Material Design — published by the same company — is among the strongest advocates of bold, dynamic color. Is this an internal disagreement at Google, a difference between editorial and product voices, or a distinction between brand-level and component-level color work?
- Nostalgia and sadness are claimed as *stronger* success indicators than joy. On what basis, beyond the two books cited? This is a strong aesthetic claim presented without research backing.
- The method addresses palette composition but not application — nothing on how stimulation interacts with accessibility contrast minimums, which is where a muted-middle preference would most plausibly run into trouble.
