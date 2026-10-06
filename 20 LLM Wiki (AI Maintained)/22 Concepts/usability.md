---
type: concept
name: "Usability"
tags: [design, ux, usability]
sources: [material-design-usability-2026, duru-rethinking-color-theory-2026, material-design-testing-m3-2024, liquid-glass-explained-2026]
---

## Definition

Usability is how intuitive and easy to understand a product is for everyone using it. Per the Nielsen Norman Group's five-aspect definition (adopted by Material Design): a usable product lets users complete tasks **efficiently**, minimizes and eases recovery from **errors**, is quickly **learnable** even on first use, is **memorable** across return visits, and produces user **satisfaction**.

Usability is distinct from *accessibility*, which specifically targets people with disabilities (perceivable, operable, understandable, robust experiences, including assistive-technology support). Usability is the broader, universal goal; accessibility is a necessary subset of it, not a synonym.

## How It Appears in This Wiki

Introduced in [[23 Sources/material-design-usability-2026]], where it's treated less as an abstract quality and more as something *produced* — a definition (NN/g's five aspects) paired with a concrete method for achieving it (visual hierarchy, then expressive emphasis) and six named tactics for executing that method.

## Key Sources

- [[23 Sources/material-design-usability-2026]] — Primary source; frames usability operationally through Material Design's M3 Expressive tactics.
- [[23 Sources/material-design-testing-m3-2024]] — The same team's research arm. Does not define usability; supplies the measurement instrument behind the foundations page's claims, and the scope limits that qualify them.
- [[23 Sources/duru-rethinking-color-theory-2026]] — Contributes only a dissent, on the color tactic. Does not discuss usability as such, but argues directly against the vivid-by-default approach to color that the Material page treats as a usability asset.
- [[23 Sources/liquid-glass-explained-2026]] — Contributes a case, not a definition. A second vendor's expressive visual default running into legibility, and the retreat it shipped in response. See Tensions & Debates.

## Design Tactics

The source's central, actionable content — six tactics for producing usability, meant to be combined selectively rather than all at once:

- **Color & color contrast** — Use contrasting (not merely different) primary/secondary colors to create hierarchy and mark key actions, within accessible contrast ratios. Material's dynamic color roles automate this.
- **Containment & grouping** — Group related elements in subtle containers; break content into sections via containment, spacing, and headings.
- **Motion** — Emphasizes key moments, but is distracting if overused — the one tactic explicitly flagged for restraint.
- **Shape & shape morph** — Shape differentiates containers/buttons, signals interaction state, and sets emotional tone; morphing between shapes communicates state changes (selected, tap, swipe, release).
- **Size** — The most important action should be the largest element. Called out as unusually effective: larger key actions correlate with fewer errors and higher satisfaction and learnability. **Overstated by its own evidence** — see Tensions & Debates; [[23 Sources/material-design-testing-m3-2024]] is the research this rests on and it does not establish the causal claim.
- **Typography** — Font size/style separates information hierarchy; largest/most legible text signals the primary action, smaller text signals secondary/tertiary actions, and consistent style groups related content.

## Method: Hierarchy Before Emphasis

The page's prescribed order of operations: first build strong **visual hierarchy** (color, size, spacing, placement, containment) so the primary action is unambiguous; only then layer **expressive emphasis** (illustration, scale, shape morph) to celebrate success or progress. Emphasis without hierarchy is treated as noise, not usability.

This connects to a goals-based design approach: identify primary, secondary, and tertiary goals for a given screen, give the primary goal the strongest visual weight, simplify to one primary task per page, and keep secondary/tertiary goals discoverable but visually subordinate.

## Usability vs. Accessibility

Accessibility: perceivable, operable, understandable, robust — specifically for people with disabilities, including assistive-technology support.
Usability: intuitive and easy to understand — for everyone.

The source treats accessibility as a component within usability work (e.g., color choices must meet accessibility contrast guidelines) rather than a separate discipline.

## Related Concepts

- [[22 Concepts/color-stimulation]] — **In tension on the color tactic.** Where this page treats contrasting, eye-catching primary/secondary color as a usability asset, the stimulation model treats the vivid default as a trap and locates the useful range in the muted middle. See Tensions & Debates.
- [[22 Concepts/hierarchy-utility-style]] — **The companion frame, kept separate on purpose.** Usability here is NN/g's five aspects, about what users can accomplish. That concept is about what users perceive on first contact. Material Design published both and distinguished them; this page's own source does not carry the distinction forward.
- [[22 Concepts/color-relativity]] — unaddressed implication. The color tactic here assumes colors have stable, specifiable appearances; relativity holds that appearance shifts with surround, which complicates fixed color tokens and fixed contrast judgments.
- [[22 Concepts/liquid-glass]] — **The same argument in a different material.** Apple's translucent material is an expressive default whose legibility problem is documented and whose correction shipped. Its derived first principle — expressive material belongs to the floating layer, not to content — is a stricter version of this page's hierarchy-before-emphasis method, arrived at by a vendor that had already paid for getting it wrong.

## Tensions & Debates

**The size claim outruns its evidence.** [[23 Sources/material-design-usability-2026]] states without qualification that larger key actions "dramatically increases usability and makes products more efficient," that users "make fewer errors," and that products become "more learnable." It cites no study. [[23 Sources/material-design-testing-m3-2024]], published by the same team, is the research it appears to rest on, and it does not support the claim as worded:

- It is a **preference comparison between two whole designs** (Material 2 vs Material 3, an email app, 229 US-based participants), not an isolation of element size. Four changes differed simultaneously — button size and label, name prominence, search treatment, and the top app bar's color.
- Its measures are **first impressions, not behaviour.** The authors route task completion elsewhere in as many words: "That's what usability tests are for." Fewer errors and better learnability are behavioural outcomes the instrument was not built to detect.
- The authors label the work **exploratory**, say it "doesn't give us all the answers," and offer the Compose button explanation as a hypothesis — "We hypothesize these changes make it more visible with a more obvious function."

So the finding is real but narrower than its restatement: participants *preferred* and *perceived as clearer* a design in which the primary action was larger, among other changes. The error, satisfaction and learnability claims are an extrapolation. This replaces the open question previously logged on this page. Unresolved as of 2026-10-05, in the sense that no source closes the gap — though the gap itself is now documented rather than suspected.

**Vivid color: asset or trap?** [[23 Sources/material-design-usability-2026]] prescribes contrasting, eye-catching primary/secondary color to establish hierarchy and mark key actions, and M3 Expressive pushes dynamic, bold palettes further. [[23 Sources/duru-rethinking-color-theory-2026]] argues the opposite about the same tactic: that treating color as a binary of maximal-intensity "colorful" versus safe neutrals skips the middle of the intensity range where most usable color lives, and that overstimulation produces irritation and overwhelm rather than clarity.

A third Google source now bears on this empirically. [[23 Sources/material-design-testing-m3-2024]] found that the only measure on which Material 2 beat Material 3 was **playfulness**, at 65%, which its authors attribute to M2's colorful top app bar — and their design interviews recorded that loud, colorful interfaces excite some people while others find the same aesthetic draining. That is simultaneously evidence for color as an asset (it buys playfulness, and nothing else measured bought it) and for Duru's overstimulation concern (the cost is real and falls unevenly across users). It converts a flat disagreement into a trade-off with a known price.

A fourth source now puts the same question outside Google entirely — see the next block.

Both of the original sources are published by Google and neither addresses the other. The disagreement is not about whether color carries hierarchy — both assume it does — but about where the default intensity should sit. A partial reconciliation is available and worth noting: the Material page's claim is about *contrast between* the primary and secondary roles, which Duru's model also treats as a hierarchy tool via hue distance and light–dark contrast; what Duru rejects is spending the stimulation budget on overall intensity as well. Neither source says this, so it stays a reading rather than a resolution. Unresolved as of 2026-10-05. Recorded symmetrically in [[22 Concepts/color-stimulation]].

**The expressive default has now cost two vendors something measurable.** This is the reframing the wiki's material supports as of 2026-10-06, and it is a stronger statement than the color disagreement above.

Two independent instances, different companies, different materials, same shape:

- **Google.** [[23 Sources/material-design-testing-m3-2024]] compared M2 against M3 on eleven measures. M3 won ten. The single measure M2 won was playfulness, at 65%, which the researchers attribute to M2's colorful top app bar — so the expressive element bought one quality, and the researchers' own interviews recorded that loud interfaces excite some users while draining others.
- **Apple.** [[23 Sources/liquid-glass-explained-2026]] records that Liquid Glass drew sustained legibility criticism through its betas and that Apple used the 26.1 releases to add a more opaque tinted appearance alongside the default clear one. The concession is a shipped product change, not a paper.

What these jointly establish is narrower than "expressive design harms usability" and more useful than a disagreement: **an expressive visual default has a cost, the cost falls unevenly across users, and in both documented cases the vendor who shipped it subsequently paid for it in public.** Google's payment was a research finding its own guidance does not carry forward; Apple's was an engineering retreat in a point release.

What they do not establish: that restraint is optimal, that the costs outweigh what expressiveness buys, or that either vendor was wrong to ship. Apple kept clear glass as the default and made opacity the option. The debate above is therefore not resolved — it is better specified. The question is no longer whether expressive defaults carry a price but who pays it, how large it is, and whether a design system can know in advance. Neither source asks that, and [[22 Concepts/liquid-glass]] shows why it is hard: a material whose appearance is determined by its backdrop cannot be contrast-checked before the backdrop exists.

Recorded symmetrically in [[22 Concepts/color-stimulation]] and [[22 Concepts/liquid-glass]].

One live question not resolved by any of these sources: how do these tactics prioritize against each other when they conflict (e.g., an accessible-contrast color vs. an "eye-catching" emphasis color)?

## Open Questions

- ~~What is the actual evidence base for the size→usability claim?~~ **Answered 2026-10-05** by [[23 Sources/material-design-testing-m3-2024]]: a paired-preference study of first impressions, not a behavioural result. See Tensions & Debates.
- Does any Material Design guidance distinguish claims validated behaviourally from claims supported only by first-impression surveys? Its own research arm draws that line; the foundations page does not.
- Do these tactics generalize beyond consumer-app contexts (e.g., dense data dashboards, professional tools) or are they tuned specifically for Material Design's typical use cases?
- How does Material Design's operational definition of usability compare to Nielsen Norman Group's own primary material, once that's ingested directly rather than secondhand?
- Is there a vendor that shipped an expressive visual default and did *not* subsequently retreat? Two cases is a pattern worth testing rather than trusting, and the wiki has no counter-case either way.
- Does the color tactic survive [[22 Concepts/color-relativity]]? If a color's appearance depends on its surround, a palette specified as fixed roles may not deliver the intended hierarchy in every context in which the roles are used.
