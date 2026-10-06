---
type: entity
name: "Material Design"
kind: product
tags: [design, ux, google, design-system]
sources: [material-design-usability-2026, material-design-testing-m3-2024]
---

## Overview

Material Design is Google's design system, currently in its third major iteration (M3), which includes an approach called "M3 Expressive" — a set of design tactics aimed at making digital products more intuitive, engaging, and usable. It provides both a conceptual framework (visual hierarchy, emphasis) and concrete tools (a 35-shape library, dynamic color roles, typography scales) for applying that framework.

## Key Facts

- Currently on its third major version, M3, with an "M3 Expressive" design tactic set. [[23 Sources/material-design-usability-2026]]
- Provides dynamic color roles that automatically generate palettes with proper emphasis and accessible contrast ratios. [[23 Sources/material-design-usability-2026]]
- Maintains a shape library of 35 shapes, designed so every shape can morph into any other in the set — used to mask imagery, fill space, and signal interaction states (selected, tap, swipe, scroll, release, long press). [[23 Sources/material-design-usability-2026]]
- Frames usability as achieved through six tactics: color & color contrast, containment & grouping, motion, shape & shape morph, size, typography. [[23 Sources/material-design-usability-2026]]
- Explicitly builds its usability guidance on the Nielsen Norman Group's five-aspect definition of usability rather than defining the term independently. [[23 Sources/material-design-usability-2026]]
- Runs an in-house UX research programme that evaluates the design system as a whole, using a standardized survey instrument built on three dimensions — hierarchy, utility, style — rather than NN/g's five aspects. [[23 Sources/material-design-testing-m3-2024]]
- Validated M3 against M2 by paired comparison: 229 US-based participants, email-app context, M3 preferred on attention (81%), informativeness (92%), obviousness of use (77%), clarity of main function (76%), creativity and personality (63% each). [[23 Sources/material-design-testing-m3-2024]]
- M2 beat M3 on exactly one measure — playfulness, 65% — which its own researchers attribute to M2's colorful top app bar. [[23 Sources/material-design-testing-m3-2024]]
- Team motto, quoted in its research post: "design is never done." [[23 Sources/material-design-testing-m3-2024]]

## Appearances

- [[23 Sources/material-design-usability-2026]] — Material Design's own usability guidance page; the prescriptive voice.
- [[23 Sources/material-design-testing-m3-2024]] — Its research arm's account of how the system is evaluated; the empirical voice, and noticeably more cautious than the guidance.

## Connections

- [[22 Concepts/usability]] — Material Design's usability page is the wiki's introduction to this concept.
- [[21 Entities/nielsen-norman-group]] — Material Design explicitly adopts NN/g's usability framework on its foundations page — but not in its research, which uses a three-dimension instrument of its own and does not cite NN/g.
- [[22 Concepts/hierarchy-utility-style]] — its research team's own framework for what an interface communicates.
- [[21 Entities/ruxandra-duru]] — **In tension.** Also published by Google, and argues against the vivid-by-default color approach Material's guidance prescribes. See [[22 Concepts/usability]].
- [[21 Entities/apple]] — **The structural comparison, not a disagreement.** The wiki's second vendor design language. Both pursued expressive visual systems and both ran into legibility; the reckonings differ in kind. Material Design's is a published research instrument with stated limits. Apple's is an opacity control shipped in a point release after beta criticism. See [[22 Concepts/usability]].
- [[22 Concepts/liquid-glass]] — Apple's material, held here as the comparison case to M3 Expressive.

## Contradictions

**Internal: the guidance is more confident than the research.** [[23 Sources/material-design-usability-2026]] asserts that larger key actions "dramatically increases usability," reduce errors and improve learnability. [[23 Sources/material-design-testing-m3-2024]] is the apparent basis, and it is a first-impressions preference study across four simultaneous changes whose authors call it exploratory and offer the size explanation as a hypothesis. Same organization, two registers. Documented in [[22 Concepts/usability]]. Unresolved as of 2026-10-05.

**Internal: two measurement frameworks, unreconciled.** The foundations page adopts NN/g's five aspects; the research post builds hierarchy/utility/style and does not mention NN/g. Neither source addresses the relationship.
