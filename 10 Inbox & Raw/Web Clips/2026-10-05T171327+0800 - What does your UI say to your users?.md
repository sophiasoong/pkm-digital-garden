---
title: "What does your UI say to your users?"
source: "https://m3.material.io/blog/testing-material-3"
author:
  - "[[Nico Thornley]]"
  - "[[Brenton Simpson]]"
  - "[[Julia Feldman]]"
  - "[[Michael Gilbert]]"
published: 2024-05-13
created: 2026-10-05
description: "How we tested M2 and M3 interfaces to understand the impact of visual changes"
tags:
  - "clippings"
status: ingested
wiki_source: "[[23 Sources/material-design-testing-m3-2024]]"
---

> [!warning] Clip repaired 2026-10-05
> The re-clip captured frontmatter only — m3.material.io is client-rendered and the article body
> never came through. Recovered from the live page. Structured summary rather than a verbatim copy:
> all headings, the three measured dimensions, the full question set and every reported percentage
> are preserved, with short quotes where the exact wording carries a claim. The article's charts
> and the paired M2/M3 screenshots are not reproducible here and carry part of the argument.

May 13, 2024 — Posted by Nico Thornley (UX Researcher), Brenton Simpson (Senior UX Engineer, Material Design), Julia Feldman (Senior UX Researcher, Material Design), Michael Gilbert (Staff UX Researcher, Material Design).

*How we tested M2 and M3 interfaces to understand the impact of visual changes.*

## Framing

The article opens with the problem of redesigning at the scale of an entire design system: you have ideas but don't know how users will perceive them. Does the new design feel easier to use, or will the differences be overwhelming? Are critical user journeys still getting the right emphasis? How do the changes line up with brand voice?

The team interviewed Google designers to ask what interfaces are *intended* to accomplish, and users to understand what they *actually* accomplish. The finding that shaped everything after: apps rely heavily on visual cues to communicate important information. Specifically, interfaces need to communicate three things.

- **Hierarchy** — the relative importance of the different pieces of an app.
- **Utility** — what each piece does, and how to use it.
- **Style** — what its brand or "vibe" is; who made this, and who it's for.

This became the research framework: questions should directly measure a design's hierarchy, utility and style, letting participants compare designs and say which better accomplishes the design's intent. With a standardized question set they could gather feedback from hundreds of participants in a few hours, automate the parsing, and study the design system as a whole rather than individual changes.

## What did we ask, and why?

An important scope limit, stated by the authors: these questions don't tell us about behaviour, like whether users can complete important tasks — "That's what usability tests are for." They measure first impressions, like whether a design is welcoming or overwhelming.

**1. Hierarchy.** Effective hierarchy — through size, placement, contrast and motion — helps people know what is most important. They asked how "effectively" a design "draws your attention to the most important and useful features." Because hierarchy can also be inefficient (their example: a blank interface with a single giant button has clear hierarchy but wastes space), they also asked how "informative" each design is.

**2. Perceived utility.** Users learn the "language" of app design — click the blue link, tap the X to close — and leveraging that learned experience is a key benefit of a design system, since it lets interfaces spend space on content and action rather than instruction. But no designer can know every user's mental model, so they asked whether the design is "obvious to use" and whether it has a "clear main function."

**3. Style.** Style signals who made something, how they want you to feel, and whether you can trust the app with your data. They asked how "modern," "clean" and "visually appealing" a design feels.

Notably, their interviews found that **some people feel excited using colorful, loud interfaces, while others find parsing the same aesthetic draining.** So they asked how "energetic" and "emotive" a design is. The serious-to-fun spectrum emerged as critical, so they measured "positivity," "playfulness," "friendliness" and "creativity," and finally had participants rate "personality" and "vibe or feel" as holistic measures.

## Measuring Material 3

Participants compared Material 2 designs against their Material 3 counterparts across a range of sample use cases. In the reported experiment, **229 US-based participants** ranked M2 against M3 in the context of an email app. The chart's horizontal axis estimates the percent of the population that would choose each design per question; "*" marks a statistically significant difference.

## What did we learn?

**Hierarchy** — 81% felt the M3 version more effectively guided their attention; 92% found it more informative.

**Perceived utility** — 77% thought it was more obvious how to use the M3 design; 76% found its main function clearer.

**Style** — statistically significant differences in a few areas: 63% called the M3 version more creative, and 63% preferred its personality.

**The one reversal** — 65% of respondents thought the **Material 2** design was more playful.

## Where do we go from here?

The team's stated caveat: comparing totally different designs, like M2 to M3, is *exploratory* research intended to provoke questions about which changes matter to users. "It doesn't give us all the answers, but instead points us in the direction where we might find them."

Their hypotheses about which specific differences drove the results:

- The **Compose button** is bigger in the M3 design and includes a text label. "We hypothesize these changes make it more visible with a more obvious function."
- The M3 version makes the **names of people you're chatting with** more prominent — perhaps the most important characteristic of a conversation is who it's with.
- **Search** changed from a small icon button in M2 to a much larger search bar in M3, which may make it feel easier to find things, and more obvious to use.
- The M2 version featured a **colorful top app bar**, and playfulness was the only metric it won. The authors' advice: "If you want your app to feel playful, consider including big splashes of color."

## Final thoughts

Presented as a step in understanding what designs communicate through hierarchy, perceived utility and style, and as one example of how the team evaluates the evolution of Material Design — the same questions are being asked across a breadth of experiences.
