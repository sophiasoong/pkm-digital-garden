---
type: source
title: "What does your UI say to your users?"
author: "Nico Thornley, Brenton Simpson, Julia Feldman, Michael Gilbert (Material Design)"
date: 2024-05-13
source_type: article
url: https://m3.material.io/blog/testing-material-3
ingested: 2026-10-05
tags: [design, ux, usability, research, material-design, color]
---

## Summary

A Material Design research post by four of Google's UX researchers and engineers, describing the survey instrument they built to evaluate Material 3 against Material 2 at the scale of a whole design system. Its contribution is methodological rather than prescriptive: where [[23 Sources/material-design-usability-2026]] tells designers what to do, this explains how the team decided whether any of it worked.

The instrument comes out of interviews with Google designers about what interfaces are *intended* to accomplish and with users about what they *actually* accomplish. The finding that organizes everything else is that interfaces communicate three things — **hierarchy** (relative importance), **utility** (what each piece does and how to use it), and **style** (brand, vibe, who made this and for whom). Standardized questions tuned to those three properties let the team poll hundreds of participants in a few hours, automate the parsing, and compare designs pairwise across many sample contexts rather than testing changes one at a time.

The reported experiment had 229 US-based participants rank an M2 email app against its M3 counterpart. M3 won nearly everything: 81% said it more effectively guided attention, 92% found it more informative, 77% found it more obviously usable, 76% found its main function clearer, and 63% called it more creative and preferred its personality. One metric reversed — 65% thought the **M2** design was more playful, which the authors attribute to its colorful top app bar.

Two caveats the authors state plainly deserve as much weight as the numbers, because the rest of the wiki's design material leans on claims this article is the apparent evidence for. First, the questions measure **first impressions, not behaviour** — the authors explicitly hand task completion off to usability testing. Second, comparing two entirely different designs is **exploratory** research: it provokes questions rather than answering them, and the attributions to specific elements (the larger Compose button, the expanded search bar) are offered as hypotheses, in those words.

## Key Points

- Interfaces communicate in three measurable dimensions: **hierarchy**, **utility**, **style**.
- Hierarchy was probed with two questions, because hierarchy can be clear but inefficient: how "effectively" a design draws attention to important features, and how "informative" it is. Their counterexample is a blank screen with one giant button — perfect hierarchy, wasted space.
- Utility was probed by asking whether a design is "obvious to use" and has a "clear main function," on the reasoning that users have learned a shared language of app design that a system can leverage.
- Style used the largest question set: "modern," "clean," "visually appealing," "energetic," "emotive," "positivity," "playfulness," "friendliness," "creativity," plus "personality" and "vibe or feel" as holistic measures.
- **Interviews found that some people feel excited by colorful, loud interfaces while others find the same aesthetic draining** — the reason "energetic" and "emotive" were measured at all.
- Experiment: 229 US-based participants, M2 vs M3, email app context.
- Results favoring M3 — attention 81%, informative 92%, obvious to use 77%, clear main function 76%, more creative 63%, preferred personality 63%.
- The single reversal: 65% found **M2 more playful**, attributed to its colorful top app bar. The authors' advice is to use big splashes of color for a playful feel.
- Stated scope limit: these questions measure first impressions, not whether users can complete tasks — "That's what usability tests are for."
- Stated epistemic limit: M2-vs-M3 comparison is exploratory research that "doesn't give us all the answers." Element-level explanations are flagged as hypotheses.
- Four changes are hypothesized to drive the M3 result: a larger, text-labelled Compose button; more prominent conversation names; a large search bar replacing a small icon button; and the loss of M2's colorful top app bar.

## Entities Mentioned

- [[21 Entities/material-design]] — the design system under evaluation and the publisher; this is its research arm's account of how it validates itself.

Authors recorded as mentions rather than given pages: **Nico Thornley** (UX Researcher), **Brenton Simpson** (Senior UX Engineer, Material Design), **Julia Feldman** (Senior UX Researcher, Material Design), **Michael Gilbert** (Staff UX Researcher, Material Design). Nothing is known of any of them beyond a job title and co-authorship of this one post, which is thinner than the threshold applied to the nine figures cited in [[23 Sources/duru-rethinking-color-theory-2026]]. Worth revisiting if a second source features any of them.

## Concepts Mentioned

- [[22 Concepts/hierarchy-utility-style]] — this source is the concept's origin and sole source.
- [[22 Concepts/usability]] — adjacent but deliberately distinguished. The authors separate perception research from usability testing; this article does the former and says so.
- [[22 Concepts/color-stimulation]] — not named, but the playfulness reversal and the excited-versus-drained interview finding are the first empirical material in this wiki bearing on color intensity and response.

## Connections

- [[23 Sources/material-design-usability-2026]] — **The important link, and it cuts two ways.** Same publisher, same domain, and this is the research the foundations page's confident claims appear to rest on. But the foundations page asserts that larger key actions "dramatically increases usability… fewer errors… more learnable," while this article's own framing gives it a preference comparison of two whole designs, four simultaneous changes, first-impression measures, and an explicit "we hypothesize" about the button size. The guidance is stated more strongly than the cited research supports. Documented in [[22 Concepts/usability]].
- [[22 Concepts/color-stimulation]] — **Empirical third voice in an existing dispute.** [[23 Sources/duru-rethinking-color-theory-2026]] argues the vivid default overstimulates; [[23 Sources/material-design-usability-2026]] prescribes eye-catching color. This article measured something adjacent and found both effects in the same data: color won *playfulness* and nothing else, and the team's interviews recorded that loud interfaces excite some people and drain others. That reframes a flat disagreement as a trade-off with a known cost.
- [[21 Entities/nielsen-norman-group]] — not cited here. Notable by absence: the foundations page borrows NN/g's five-aspect definition, while this research programme builds its own three-dimension instrument instead. Two different ways of deciding what to measure, published by the same team.
- `10 Inbox & Raw/Fleeting Notes/UI communicates in 3 areas.md` — the human's own synthesis of this article's framework, written before the source was ingested.

## Quotes

> "That's what usability tests are for."

## Questions Raised

- Does anything in the Material 3 guidance distinguish claims validated behaviourally from claims supported only by first-impression surveys? The foundations page draws no such line, and this article says the line exists.
- The playfulness reversal is treated as a curiosity and converted into advice (use color for playfulness). But it is also the one place the redesign lost. Was anything given up that the instrument wasn't built to detect?
- Why 229 US-based participants only, and how far do style judgments — playfulness, friendliness, vibe — travel across cultures? The article reports the constraint without discussing it.
- The three dimensions came from interviews with Google designers and users of Google products. Is hierarchy/utility/style a general account of what interfaces communicate, or a description of what this design system optimizes for?
- Hierarchy, utility and style were all measured by self-report on paired comparisons. Is a stated preference between two screenshots evidence about an interface someone has to use for a year?
