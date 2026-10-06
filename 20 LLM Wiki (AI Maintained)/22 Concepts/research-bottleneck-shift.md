---
type: concept
name: "Research Bottleneck Shift"
tags: [research, ai, publishing, academia, peer-review, mathematics]
sources: [tao-six-essentials-2026]
---

## Definition

A research bottleneck shift is what happens when a tool accelerates some stages of a pipeline and not others: the constraint moves rather than disappearing, and the system's output can fail to increase even though every accelerated component genuinely got faster. The general statement in this wiki's source is that individual steps of science can certainly be accelerated — experiments, code, papers — but science as a whole may not accelerate just because every single component gets faster [[23 Sources/tao-six-essentials-2026]].

The concept's value is that it converts a vague worry about AI and science into something with a named structure and a locatable constraint.

## The Proof Life Cycle

The source's model, which is what makes the argument checkable:

1. **Generate** a proposed proof or solution. Used to be hard. Automating fast.
2. **Verify** that it is correct. Used to be tedious. Automating fast.
3. **Write it readably.** Not automating.
4. **Get other people excited** — the peer-review stage, where referees decide whether a result helps them with their own problems or clarifies why a phenomenon holds. Not automating.
5. **Polish into textbook form** and teach it. Not automating.

Stages 1 and 2 are the ones that were scarce, so they are the ones the tools were pointed at. Stages 3 to 5 are now the constraint.

## Why the Late Stages Resist

The diagnosis is specific and is the most original thing in this source. AI-generated proofs are often unpleasant to read: they spend a lot of time on something trivial and very little on the most interesting part. The reason offered is that the system cannot distinguish hard from easy, because by brute force every step costs the same amount of effort — whereas a human who had to struggle at the hardest step of a paper naturally dwells there. The proportions of a human write-up carry information about the terrain, and a machine write-up does not have that information to carry.

A separate failure mode is orthogonal to quality: a paper can be correct, readable and perfectly fine while answering a question nobody cares about. Nothing in stages 1 and 2 filters for that.

## Proof Indigestion

The source's term for the resulting state. Solutions to major problems used to be rare enough that all the experts would drop everything to read one, because it was so rare and valuable that doing so was worth it. Now the pile of pending solutions that ought to be understood and absorbed exceeds anyone's capacity, so triage is required — and he says this has never had to happen before. He reports having personally stopped trying to stay current with all developments in his own field, and being unable to promise to read every one.

He is careful on two points. The volume problem predates AI and has been sharply accelerated by it rather than created by it. And it is a good problem to have — more food than you can eat beats too little — but it is still a problem, and what it demands is much better curation and filtering.

## The Seed Corn

The deeper version of the argument is about reproduction rather than throughput. The training problems given to graduate students as their first projects, for recognition and career experience, are exactly the papers AI can now replicate. Replace the students with the systems and you get the grad-student-level papers without getting the next generation of students. And if the digesting work that builds the next base of knowledge for humans and AIs to build on stops happening, the result may be stagnation — able to optimize everything current technology allows, while no longer developing genuinely original new ideas.

The source calls this a risky point in the structure of funding the scientific enterprise, because the outputs, or what look like the outputs, accelerate while the pipeline that produces people may not.

## How It Appears in This Wiki

Through one source, as a practitioner's report on his own field. It functions in this wiki mainly as the most specific available answer to questions the other two sources on AI and mathematics leave open — particularly what happens after a system produces a proof.

## Key Sources

- [[23 Sources/tao-six-essentials-2026]] — the life cycle, the proportions diagnosis, proof indigestion, and the seed-corn argument.

## Related Concepts

- [[22 Concepts/ai-in-mathematics]] — this page is the downstream half of that debate. One source there forecasts abundant automated problem-solving; this is an account of what abundance costs.
- [[22 Concepts/formalization]] — stage 2 of the life cycle. Formal verification delivers certainty about the statement and not the understanding that stages 3 to 5 produce.
- [[22 Concepts/failure-as-method]] — the mechanism the seed-corn worry is about. Graduate training is where failure is supposed to be formative.
- [[22 Concepts/status-economy-of-expertise]] — the same change described from the other side. Triage replacing drop-everything attention is a change in how recognition is allocated, and the apprenticeship now at risk is how practitioners entered the status economy at all.
- [[22 Concepts/hierarchy-utility-style]] — distant but real: another source in this wiki concerned with what a thing communicates as opposed to what it contains. A badly proportioned proof is a hierarchy failure.

## Tensions & Debates

**Asserted from one reading list.** Proof indigestion is evidenced by the experience of an unusually broad mathematician who reads more than most. No count of pending solutions is offered, and "I can no longer keep up" is a report about a reader as much as about a field.

**The bottleneck may be institutional rather than cognitive.** Peer review and textbook digestion are slow partly because they are unpaid, unrewarded and done by people with other jobs. If that is the binding constraint, the problem is funding and credit allocation, not a limit on what can be automated — and the source does not separate the two.

**The proportions diagnosis is testable and untested.** "The AI cannot tell what is hard because brute force makes every step cost the same" is a real mechanism, and it predicts that systems with explicit difficulty estimates would write better-proportioned proofs. Nobody in this wiki's material has tried.

**The seed-corn argument assumes the current apprenticeship is necessary.** It may only be customary. If graduate training could be restructured around problems AI cannot do — or around the digestion work that is now the bottleneck — the pipeline survives in a different shape. The source names the risk and does not consider the restructuring.

**It is in partial tension with the breadth thesis.** The same source argues elsewhere that AI's value is solving a small percentage of a very large number of problems, which is precisely a recipe for flooding the digestion stage. The two claims are consistent, but together they amount to saying the tool's main benefit is also the main cause of the problem — which is worth stating plainly, because the source states them in separate passages and never joins them.

## Open Questions

- Is there a measure of proof indigestion? Preprint counts, time-to-citation, time-to-textbook — something would make this checkable.
- Can digestion be automated later, or is it the irreducible part? The proportions diagnosis implies there is a reason it resists, and it is a reason about current systems.
- If curation and filtering become the scarce skill, who does it and what rewards it? Nothing currently credits the person who makes a flood legible.
- What is the actual replacement rate for graduate-student-level work? The seed-corn worry needs this number and the source does not have it.
- Does this generalize beyond mathematics? Fields whose bottleneck is already data collection or experiment rather than write-up would shift differently, and the wiki holds no other instance.
