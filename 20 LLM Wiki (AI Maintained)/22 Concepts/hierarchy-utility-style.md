---
type: concept
name: "Hierarchy, Utility, Style"
tags: [design, ux, research, measurement, material-design]
sources: [material-design-testing-m3-2024]
---

## Definition

A three-dimension account of what a user interface communicates, developed by Material Design's research team as the basis for a measurement instrument:

- **Hierarchy** — the relative importance of the different pieces of an app.
- **Utility** — what each piece does, and how to use it.
- **Style** — what its brand or "vibe" is; who made this, and who it is for.

The framework's origin matters to what it is for. It came from interviewing Google designers about what interfaces are *intended* to accomplish and users about what they *actually* accomplish, and the three dimensions are the categories where those two accounts had to be compared [[23 Sources/material-design-testing-m3-2024]]. So this is not a theory of interface meaning arrived at analytically; it is a list of what turned out to be worth asking about, built so that design changes could be evaluated at the scale of a whole system rather than one component at a time.

Each dimension carries its own question set, and the construction of those sets is where the thinking shows:

- **Hierarchy** needs two questions, not one, because hierarchy can be unambiguous and still wasteful. A blank screen with a single giant button has perfect hierarchy. So "effectively draws your attention to the most important and useful features" is paired with "informative" to catch efficiency.
- **Utility** is asked as "obvious to use" and "clear main function," resting on the premise that users have learned a shared language of interface convention which a design system can draw on, letting screens spend space on content rather than instruction.
- **Style** gets the largest set — modern, clean, visually appealing, energetic, emotive, positivity, playfulness, friendliness, creativity — plus personality and vibe as holistic measures. The serious-to-fun spectrum was identified in interviews as the critical one.

## How It Appears in This Wiki

Introduced by [[23 Sources/material-design-testing-m3-2024]], where it is immediately put to work: 229 US participants compared an M2 email app with its M3 counterpart across all three dimensions, and M3 won every measure except playfulness.

The concept's value in this wiki is as a **measurement frame** rather than a design prescription, and it is the first of its kind here. Every other design page holds claims about what designers should do; this one holds a method for finding out whether any of it landed. That makes it the natural place to test the wiki's other design content, which is exactly what it does to [[22 Concepts/usability]].

Its most useful property is a boundary the authors draw explicitly: these questions measure **first impressions, not behaviour**. Task completion is handed off to usability testing in so many words. That single distinction is what exposes the gap between Material's confident usability guidance and the research behind it.

Worth noting for provenance: the human's fleeting note `UI communicates in 3 areas` is their own synthesis of this framework, written before the source was ingested — the idea entered this vault through the human first.

## Key Sources

- [[23 Sources/material-design-testing-m3-2024]] — sole source. Origin of the three dimensions, the question sets, and the M2/M3 results.

## Related Concepts

- [[22 Concepts/usability]] — **Deliberately distinct, and the distinction does work.** Usability as this wiki holds it is NN/g's five aspects, which are about what users can accomplish. These three dimensions are about what users perceive on first contact. The same team published both and separated them; the foundations page does not carry that separation forward.
- [[22 Concepts/color-stimulation]] — intersects at style. "Energetic" and "emotive" were measured precisely because interviews found loud interfaces excite some people and drain others, which is the stimulation model's central claim arrived at from a different direction.
- [[22 Concepts/liquid-glass]] — reaches the hierarchy dimension from the material side. Its first design principle — glass belongs to the layer floating above content, never to content itself — assigns a material to a position in the hierarchy, which is a stronger and more operable claim than this framework's dimension, since it tells a designer what to do rather than what to measure. Neither source connects them.

## Tensions & Debates

**The instrument is more careful than the guidance built on it.** The research is framed as exploratory, measuring first impressions, with element-level explanations offered as hypotheses. [[23 Sources/material-design-usability-2026]] converts this into unqualified instruction — larger key actions "dramatically increases usability," users "make fewer errors." Nothing in the research as described establishes the causal, behavioural claim. The tension is not between two positions but between a finding and its own restatement. Recorded in [[22 Concepts/usability]]. Unresolved as of 2026-10-05.

**Is style measurable by paired self-report?** Eleven adjectives against two screenshots produce clean percentages, and the cleanliness is itself a reason for suspicion: judgments of personality and vibe on first sight may not predict how an interface feels after a year of daily use. The source reports the method without defending it on this point.

**Two instruments, one team.** [[23 Sources/material-design-usability-2026]] adopts [[21 Entities/nielsen-norman-group]]'s five aspects; this source builds its own three dimensions and does not cite NN/g. Both are Material Design. Whether these are complementary layers or an unreconciled difference in what the team thinks should be measured is not addressed in either source.

## Open Questions

- Are the three dimensions general, or a description of what Material Design optimizes for? They were derived from Google designers and users of Google products.
- Do style judgments travel? The reported experiment is 229 US-based participants, and playfulness, friendliness and vibe are the most plausibly culture-bound measures in the set.
- The framework measures what an interface communicates but not whether the communication was *correct* — whether the design that reads as more informative is in fact better to use. The authors concede this by routing behaviour to usability testing, which leaves the two halves unjoined.
- What happened in the other sample contexts? The article says these questions were asked "across a breadth of experiences" but reports one email-app comparison.
