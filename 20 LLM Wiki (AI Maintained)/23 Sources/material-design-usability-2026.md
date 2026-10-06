---
type: source
title: "Usability"
author: "Material Design (Google)"
date: unknown
source_type: article
url: https://m3.material.io/foundations/usability/overview
ingested: 2026-08-28
tags: [design, ux, usability, material-design]
---

## Summary

This is Google's Material Design 3 overview page on usability. It opens by borrowing the Nielsen Norman Group's five-aspect definition of usability — efficiency, errors, learnability, memorability, satisfaction — then spends most of its length on the actionable half: the concrete "M3 Expressive" design tactics used to achieve those aspects. The core move of the page is treating usability not as an abstract quality but as something produced tactic by tactic: visual hierarchy first, then emphasis for delight.

The tactics covered are color & color contrast, containment & grouping, motion, shape & shape morph, size, and typography — each framed around the same underlying principle: the most important action should be the most visually dominant one, and everything else should recede in support of it. Size gets a notably strong claim: making key actions larger doesn't just look better, it measurably reduces errors and increases satisfaction and learnability.

The page also draws a clean boundary between usability and accessibility — accessibility is about making a product usable by people with disabilities specifically (perceivable, operable, understandable, robust); usability is the broader, universal goal of making a product intuitive for everyone. It closes with a caution against overusing its own tactics: too many expressive moves at once undermine the hierarchy they're meant to create, and every design choice should be validated through iterative user testing rather than assumed to work.

## Key Points

- Usability is defined via five aspects (Nielsen Norman Group): efficiency, errors, learnability, memorability, satisfaction.
- Usability ≠ accessibility: accessibility targets people with disabilities specifically; usability targets everyone.
- Core method: build strong visual hierarchy first (color, size, spacing, placement, containment), then add expressive emphasis (illustration, scale, shape morph) to celebrate progress or success.
- Six named design tactics: color & color contrast, containment & grouping, motion, shape & shape morph, size, typography.
- Size is called out as unusually effective: larger key actions correlate with fewer errors, higher satisfaction, and better learnability.
- Motion should be used sparingly — it's effective for emphasis but distracting if overused.
- Material's shape library has 35 shapes; shapes can morph into one another to signal interaction state (selected, tap, swipe, scroll, release, long press).
- Design should be organized around primary/secondary/tertiary goals, with only one primary task emphasized per page.
- Explicit anti-pattern warning: combining too many expressive tactics at once is distracting rather than helpful.
- Usability claims should be validated through iterative testing, not assumed from the tactics alone.

## Entities Mentioned

- [[21 Entities/material-design]] — Google's design system; source of all the design tactics and the M3 Expressive framing.
- [[21 Entities/nielsen-norman-group]] — UX research organization; source of the five-aspect usability definition this page builds on.

## Concepts Mentioned

- [[22 Concepts/usability]] — The page's entire subject; both defined (five aspects) and operationalized (six design tactics).

## Connections

- [[23 Sources/material-design-testing-m3-2024]] — **The research behind this page's claims, and it qualifies them.** Same team, published 2024. This page states the size effect as established fact; that study is a first-impressions preference comparison of two whole designs with four simultaneous changes, labelled exploratory by its authors, with the button-size explanation offered as a hypothesis. It also uses a different measurement framework — hierarchy/utility/style — rather than the NN/g five aspects this page adopts. Documented in [[22 Concepts/usability]].
- [[23 Sources/duru-rethinking-color-theory-2026]] — **Tension on the color tactic.** Also Google-published. Argues the eye-catching, vivid default this page prescribes is a conceptual trap, and locates usable color in the muted middle of the intensity range. Neither source addresses the other.
- [[22 Concepts/hierarchy-utility-style]] — the alternative frame its own research team uses.

## Quotes

> "Usability focuses on making products intuitive and easy to understand for everyone."

> "Using larger sizes for key actions dramatically increases usability and makes products more efficient. Users are satisfied, they make fewer errors, and find the products to be more learnable."

> "Not using too many expressive tactics at the same time as they can be distracting."

## Questions Raised

- The size→usability claim (larger key actions reduce errors, increase satisfaction/learnability) is stated as fact — what's the actual evidence base behind it, and does it hold across contexts (e.g., dense data UIs vs. simple consumer apps)?
- How do these tactics reconcile when they conflict — e.g., if the accessible/high-contrast color choice clashes with the "eye-catching" emphasis color?
- No publish date is available on the page — is this guidance stable, or does M3 Expressive change frequently enough that this page should be periodically re-ingested?
