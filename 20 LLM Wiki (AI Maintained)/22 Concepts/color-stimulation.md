---
type: concept
name: "Color Stimulation"
tags: [design, color, perception, emotion, framework]
sources: [duru-rethinking-color-theory-2026, duru-halfway-color-combinations-2021, material-design-testing-m3-2024, liquid-glass-explained-2026]
---

## Definition

Stimulation is the overall perceptual intensity of a color combination — how much it demands of the viewer. In the model this wiki's sources present, it is not a property of any single color but a quantity produced by three interacting properties of the combination:

1. **Overall intensity** (chroma) — how vivid the colors are, distinct from saturation; a fully saturated color can still read as low-intensity.
2. **Hue distance** — how far apart the hues sit on the wheel.
3. **Light–dark contrast** — the lightness spread, complicated by the fact that pure hues have different inherent lightness (yellow reads near white, purple near black).

The operative claim is that these behave like sliders on a mixing board: pushing one up invites bringing another down. Stimulation is therefore a budget to be spent rather than a value to maximize, and both extremes are failure states — understimulation reads as apathy, overstimulation as irritation or overwhelm. The target is the middle of the range [[23 Sources/duru-rethinking-color-theory-2026]].

The model is embedded in a three-step method: **balance the stimulation**, then **relate** the colors (restrict one property at a time to give the palette its glue, optionally via a bridge color or an imaginary colored light), then **complete** them (complementary logic extended beyond hue to lightness and temperature, most satisfying at dramatically unequal proportions). Both ends of the method are bracketed by an emotional gut check, which is given final authority over the analysis.

## How It Appears in This Wiki

The concept arrives fully formed in [[23 Sources/duru-rethinking-color-theory-2026]] and in germ form in [[23 Sources/duru-halfway-color-combinations-2021]], which is the same author five years earlier. The earlier article catalogues nine hue pairs by feel, then concludes that value and saturation choices change the mood more than the hue pair does — which is, in retrospect, the intensity and lightness sliders being noticed empirically before they were named. The later article supplies the third property, the balancing principle, and the method. This wiki therefore holds both ends of one person's thinking about the same problem.

Two refinements in the later source are worth keeping distinct from the core model:

- **Vibration** is the named exception to the contrast rule. Vibrant contrasting hues at the *same* lightness read as unpleasantly overstimulating — high hue distance with zero lightness contrast does not average out.
- **Atmosphere** is the low-stimulation technique: low light–dark contrast plus gradients and fuzzy boundaries gentles even vivid color. Scale and surface micro-variation also shift stimulation independently of the colors chosen.

The concept's polemical edge is the **"vibrant by default" critique** — that designers conceive of color as a binary between maximal-intensity "colorful" and the safety of neutrals, and so skip the muted middle where most usable and most natural color sits.

## Key Sources

- [[23 Sources/duru-rethinking-color-theory-2026]] — primary source. Supplies the three properties, the mixing-board principle, the balance/relate/complete method, and the vibration and atmosphere refinements.
- [[23 Sources/duru-halfway-color-combinations-2021]] — precursor. Its conclusion that value and saturation outrank the hue pair is the model in embryo.
- [[23 Sources/material-design-testing-m3-2024]] — the only empirical material in this wiki bearing on the model. Does not test it; measures something adjacent and finds effects on both sides of it.
- [[23 Sources/liquid-glass-explained-2026]] — bears on one property only, light–dark contrast, and on the "atmosphere" technique. Does not discuss color theory; describes a shipped material that applies the model's gentling lever and breaks on it.

## Related Concepts

- [[22 Concepts/color-relativity]] — the precondition. Stimulation is a property of a combination, which only makes sense if colors cannot be assessed individually. Relativity is why the stimulation model is stated in terms of relationships rather than values.
- [[22 Concepts/halfway-color-combinations]] — the earlier, narrower idea this model supersedes. Hue distance survives as one of three properties; the specific 90° prescription does not.
- [[22 Concepts/usability]] — in tension. See below.
- [[22 Concepts/hierarchy-utility-style]] — intersects at style. Its "energetic" and "emotive" measures exist because of an observation this model is built on.
- [[22 Concepts/liquid-glass]] — **shares a lever.** Translucency gentles a surface the way "atmosphere" does, by collapsing light–dark contrast and softening boundaries. See Tensions & Debates.
- [[22 Concepts/attentive-perception]] — resonance rather than argument. The claim that micro-shifts of color in natural surfaces add a stimulation flat color lacks is a design-register version of finding richness by attending closely to the small. Neither source claims the other.

## Tensions & Debates

**Against Material Design's vivid default.** [[23 Sources/duru-rethinking-color-theory-2026]] argues that treating vibrant color as the colorful option and neutrals as the sophisticated one skips the middle of the intensity range, and that overstimulation produces irritation and overwhelm. [[23 Sources/material-design-usability-2026]] takes the opposite tack on the same tactic, treating eye-catching primary/secondary color contrast as a usability asset, with M3 Expressive pushing dynamic and bold palettes further. Both are published by Google. The disagreement is not about whether color matters but about where on the intensity scale the default should sit — and neither source addresses the other. Recorded symmetrically in [[22 Concepts/usability]]. Unresolved as of 2026-10-05.

**Partial empirical support, from an unexpected direction.** [[23 Sources/material-design-testing-m3-2024]] is Material Design's own research, and it supplies the first measured evidence in this wiki touching the model's central claim. Two findings matter. First, in a comparison of an M2 against an M3 email app with 229 participants, the **only** measure M2 won was playfulness, at 65%, attributed by the authors to its colorful top app bar — vivid color bought one specific quality and none of the others measured. Second, and closer to Duru: the team's design interviews found that some people feel excited by colorful, loud interfaces while others find parsing the same aesthetic draining, which is why "energetic" and "emotive" entered their question set at all.

That is the stimulation model's premise observed independently — the same intensity produces opposite responses in different viewers — though it supports the weaker reading. It establishes that high intensity has a cost and that the cost is unevenly distributed; it does not establish that a middle setting is optimal, nor that the three properties trade off as the mixing-board metaphor claims. Note also that this cuts against Duru on one point: she ranks nostalgia and bittersweetness above joy as success indicators, while the one thing vivid color demonstrably delivered here was playfulness.

**The atmosphere lever, used by a vendor, broke something.** [[23 Sources/duru-rethinking-color-theory-2026]] names atmosphere as the low-stimulation technique: low light–dark contrast plus gradients and fuzzy boundaries, which gentles even vivid color. That is a precise description of what a translucent interface surface does to everything behind it. [[23 Sources/liquid-glass-explained-2026]] documents Apple shipping exactly that across six operating systems and then adding opacity controls in a point release after sustained legibility criticism — the named failure being text on glass over a busy background.

The two sources are not in conflict, and the interesting part is that they agree while pointing opposite ways. Duru treats low light–dark contrast as the tool for bringing stimulation down; the Apple case shows the same reduction, applied at the content layer, destroying legibility. Both are consistent with the mixing-board model — contrast is a slider and this is what the bottom of its range costs — and together they add something the model as stated lacks: a floor. Duru's framework has an explicit ceiling (overstimulation reads as irritation) and an explicit floor framed emotionally (understimulation reads as apathy), but no floor framed functionally. The Apple case supplies one: below some light–dark contrast, the question stops being how the palette feels and becomes whether the text can be read.

Note what this does *not* support. Liquid Glass is a material, not a palette, and its source discusses color only to say the material is not a color scheme. Reading the case as a test of the stimulation model would be overreach; it is an independent instance of one of the three properties being pushed to an extreme in production, with the result recorded.

**Is stimulation actually calculable?** The mixing-board model implies a quantity, but no formula, units or weighting is given. [[21 Entities/color-moods]] is cited as the implementation without specifying how the three properties combine. The model may be a teaching metaphor presented in the register of a calculation.

**Feeling over analysis.** The method's own author subordinates it to the designer's gut response, and ranks nostalgia, bittersweetness and sadness above joy as success indicators — a strong aesthetic claim supported by two books rather than evidence. Whether the analytical apparatus does work, or legitimizes a judgment made before it, is left open by the source.

## Open Questions

- How does a muted-middle preference interact with accessibility contrast minimums? The sources address palette composition, not application, and this is the most likely point of friction. [[23 Sources/liquid-glass-explained-2026]] is the nearest thing the wiki has to an answer and it is a cautionary one: a vendor hit the floor and shipped a control to climb back off it.
- Does the model have a functional floor as well as an emotional one? Stated in terms of apathy and irritation, it has no vocabulary for illegible.
- Is the three-property model sufficient, or are there further independent contributors to stimulation? Scale and surface micro-variation are named as affecting stimulation but are not among the three properties.
- Is the "vibrant by default" bias a real pattern in the field, or a characterization of a position no one holds explicitly? [[23 Sources/material-design-usability-2026]] suggests it is real and institutional.
- Does the emotional gut check travel? The success criteria are stated as universal but drawn from one designer's responses.
