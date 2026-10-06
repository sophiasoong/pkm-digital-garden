---
type: concept
name: "AI in Mathematics"
tags: [mathematics, ai, automation, research, forecasting]
sources: [szegedy-quo-vadis-mathematics-2026, ono-nine-lessons-2026, tao-six-essentials-2026]
---

## Definition

AI in mathematics is the question of what automated reasoning systems are doing to mathematical practice — not whether machines can do mathematics, which all three of this wiki's sources treat as settled, but what changes once they can. The three disagree about almost everything downstream of that: what the systems are good for, what the bottleneck is, what the right goal is, and what mathematicians should do about it.

All three voices are working mathematicians, and two of the three are employed on the AI side of the question, which is the single most important fact for reading them. None is a disinterested observer and none pretends to be.

## The Three Positions

### Szegedy — the trajectory

Automated reasoning is currently primitive, narrow, expensive and unreliable, and none of those are properties of the technology; they are properties of this moment in its development. The whole argument rests on rate of change rather than current capability. The organizing image is aviation: the Wright brothers' first flight lasted twelve seconds and covered less ground than a jumbo jet's wingspan, and that is roughly where AI in mathematics sits. Systems that until recently managed a few hundred metres at low altitude have in the last few months reached the range and reliability to enter difficult terrain without crashing, landing on several problems nobody had settled [[23 Sources/szegedy-quo-vadis-mathematics-2026]].

The forecast is staged and each stage is separately checkable:

1. **Primitive flight.** Short, low, expensive, narrow. Already past.
2. **Entering the terrain.** Enough range and reliability to work inside hard problems, plus the first settled conjectures. Claimed as of the last few months.
3. **Flag-planting as demonstration.** Labs targeting named open problems for publicity. Conceded to be PR, forecast to get old quickly.
4. **Cheap charter.** Anyone who can afford it lands on any problem; hand-honing methods by attacking conjectures loses its purpose.
5. **Satellites.** Systematic mapping of the whole terrain for anything valuable, then extraction. Messy, commercial, lucrative, resented.

What the source concedes: the planes fly for under half an hour, at low speed and altitude, cost far more than the artisan tools they replace, and cannot reach the real summits — the hardest problems and the construction of broad theories. The move is not to deny the limits but to deny they are informative, which is [[22 Concepts/static-thinking-fallacy]].

### Tao — complementarity

The difficulty axis is the error. Problems do not sit on one line from easy to hard; the useful picture is two-dimensional, and humans and machines occupy different regions of it. Humans go deep and narrow: one very hard problem, years, enormous context. AI goes broad and shallow: a small percentage of a very large number of problems, which was never economically viable before because you could not hire ten thousand graduate students to each try one thing. That is not a lesser version of what mathematicians do — it is a different shape of effort, and the value is in the breadth, not in eventually reaching the depth [[23 Sources/tao-six-essentials-2026]].

On current capability he is specific where Szegedy is not. The Erdős unit distance conjecture is the kind of problem being attacked. The cost of an attempt is undisclosed because the systems are privately owned — "a hundred thousand dollars? a million?" — the success rate is unknown, and possibly only around 1% of problems are amenable at all. He also uses the tools himself: literature search, proof-checking, code, proofreading.

His real claim is about what happens after a proof exists. See [[22 Concepts/research-bottleneck-shift]] for the proof life cycle and proof indigestion; the short form is that generation and verification are automating fast while readable write-up, peer interest and textbook digestion are not, so the constraint moves rather than lifting. And the training problems given to graduate students for their first papers are exactly what the systems now replicate, which puts the pipeline that produces mathematicians at risk — see [[22 Concepts/failure-as-method]].

### Ono — the wrong race

Szegedy's structural twin and his clearest opponent. Same position — a mathematician employed on the AI side, reporting the change first-hand — and an explicit rejection of Szegedy's axis: not a race for more compute but a race for more truth. The goal is not systems that produce more proofs faster; it is systems whose output can be trusted, which means formal verification. See [[22 Concepts/formalization]] [[23 Sources/ono-nine-lessons-2026]].

His analogy is chosen to foreground what Szegedy's foregrounds away. Not the Wright brothers but the sharecropper and the tractor: a trade that was genuinely displaced, by a machine that was genuinely better. He also names the Erdős unit distance conjecture, attributing the result to OpenAI, which is the one factual point on which all the specific claims in this wiki converge.

The second half of his position is about measurement rather than capability, and it is the part with the sharpest edge: benchmarks measuring human mathematical ability are the wrong instrument, applied to the wrong subject, for incentives that corrupt what they measure. See [[22 Concepts/benchmark-critique]].

## Where They Actually Disagree

**What the systems are for.** Szegedy: eventually everything, on a trajectory. Tao: breadth that humans cannot staff, permanently complementary rather than transitional. Ono: nothing worth having until the output is verifiable.

**Whether cost falls.** Szegedy's stage 4 forecasts cheap charter flights without saying what makes them cheap. Tao reports that nobody outside the labs knows the current cost, and that the owners are private companies with no obligation to say. This is a flat contradiction of a stage in the forecast, and it is the most load-bearing one, because stages 4 and 5 both presuppose access.

**What the real obstacle is.** Szegedy: capability, which time solves. Tao: digestion, which time does not — the volume problem predates AI and has been accelerated by it. Ono: trust, which only formalization solves.

**What mathematicians should do.** Szegedy: adapt, because the terrain is being mapped whether or not you consent. Tao: protect the parts that do not automate, particularly the training of the next generation. Ono: change what is measured and rewarded.

**Whether the job survives.** Ono says job losses will not be significant, immediately after the sharecropper analogy — a tension flagged on [[21 Entities/ken-ono]]. Tao does not forecast employment at all; his worry is about reproduction, not headcount. Szegedy forecasts a changed field whose current inhabitants resent the change.

## Where They Agree

- Something real changed in the last year or so, and recently rather than gradually.
- The Erdős unit distance conjecture is a genuine case (Tao and Ono both name it; Szegedy names nothing).
- Theory-building is the furthest thing from automation, and it is what mathematics mostly consists of.
- The institutions have not adjusted — on benchmarks and prestige for Ono, on funding and graduate training for Tao, on the status economy for Szegedy.
- All three use the tools or build them. Nobody in this wiki is arguing from the outside.

## How It Appears in This Wiki

Through three sources, all partisan, none independent of the thing described, and none citing anything. Two are machine-transcribed interviews; one is an uncited essay. What this page holds is therefore a well-mapped argument rather than a settled account of a field — but with three voices the disagreements are now locatable, which is a real improvement on holding one forecast and no way to check it.

The structural asymmetry worth keeping in view: Szegedy argues from where the curve is going, Tao from what his field's pipeline does, Ono from what he thinks the goal should be. They are not three answers to one question so much as three different questions, which is part of why the disagreement has not been resolved by anyone.

## Key Sources

- [[23 Sources/szegedy-quo-vadis-mathematics-2026]] — the aviation analogy, the staged forecast, the trajectory argument.
- [[23 Sources/tao-six-essentials-2026]] — complementarity, the two-dimensional picture, the proof life cycle, proof indigestion, cost opacity, the seed-corn worry.
- [[23 Sources/ono-nine-lessons-2026]] — truth over compute, formalization as the goal, the sharecropper analogy, the benchmark critique.

## Related Concepts

- [[22 Concepts/static-thinking-fallacy]] — Szegedy's argumentative engine, now contested: Tao's objection is not that the systems will stay as they are but that the single axis along which they are supposed to improve is the wrong axis.
- [[22 Concepts/formalization]] — Ono's answer, with Tao supplying the worked cases and the limits.
- [[22 Concepts/research-bottleneck-shift]] — Tao's answer, and the best available account of what happens after stage 2.
- [[22 Concepts/benchmark-critique]] — Ono's answer on measurement.
- [[22 Concepts/failure-as-method]] — what the tools may remove, from the same source as the complementarity argument.
- [[22 Concepts/status-economy-of-expertise]] — the consequence all three care about from different angles. This page is about the instrument; that page is about what the instrument does to a community's reward structure.
- [[22 Concepts/six-essentials-of-mathematics]] — the practice being changed, as described by one of the three.

## Tensions & Debates

**Szegedy's load-bearing claim is still uncited.** "We solved a few conjectures" names no conjecture, no system, no lab, no result. Two later sources partly rescue it — both name the Erdős unit distance conjecture, and Ono attributes it to OpenAI — but that is corroboration of a nearby claim by other interested parties, not verification of his. Stage 2 is now plausible rather than unverifiable.

**Stage 4 is directly contradicted.** Cheap charter requires falling costs; Tao reports that the cost is unknown outside the labs, the instruments are privately owned, and the amenable fraction of problems may be around 1%. Nothing in this wiki supports the cheapness and one source argues against the access.

**All three authors are inside the thing they describe.** Szegedy says "we" of the flag-planting companies. Ono's every claim about Axiom Math's results is an employee describing his employer with no paper or repository named — see [[21 Entities/axiom-math]]. Tao is the most independent of the three and is also a public collaborator with the labs and a benchmark co-designer. Three partisan accounts that disagree are more useful than one, but this is not the same as independent confirmation.

**The analogies do argumentative work that nobody has done.** Aviation improved for reasons specific to aviation; sharecropping ended for reasons specific to agriculture. Each picks a historical case that turned out the way its author expects and imports the ending. Technologies that stayed crude get no analogies named after them, and neither does a trade that survived mechanization. That these two analogies point in different directions from the same structural position is the clearest evidence that the analogy is not where the argument lives.

**Two transcripts and an essay.** Both interview sources are machine-generated transcripts with visible garbling, which is a real constraint on quoting precisely and on trusting any number that appears in them. Flagged on both source pages.

**The incentive objections remain unanswered by everyone.** Szegedy reported them and replied only with the trajectory argument: flags on in-progress problems deter other attempts, the targeted problems were not very interesting, some were already nearly climbed. Tao and Ono each address incentives in their own terms — digestion credit, benchmark corruption — but nobody in this wiki addresses the specific complaint about flag-planting on live problems.

## Open Questions

Four of the five questions this page carried when it held one source have been answered, and are recorded here with their answers because the answers all came from partisan sources:

- **Which conjectures, which systems?** Partly answered: the Erdős unit distance conjecture, attributed by Ono to OpenAI and named independently by Tao. Still no paper, no repository, no third-party confirmation in this wiki.
- **Who gets to explore if the instruments are expensive?** Answered against the forecast: cost undisclosed, owners private, success rate unknown, perhaps 1% of problems amenable.
- **What is the error profile?** Answered more interestingly than asked. The problem is not plausible wrong proofs but correct proofs nobody can read — long, badly proportioned, because brute force makes every step cost the same and the system cannot tell hard from easy.
- **Does the flight ceiling have a cause that scales away?** Answered by rejecting the question: the one-dimensional difficulty axis is the error, and the shape of the effort is the difference rather than its magnitude.
- **Theory-building.** Still open, and all three sources agree it is the furthest out of reach. Nobody has a mechanism or a timeline.

New questions this three-way disagreement raises:

- Is complementarity stable or transitional? Tao's two-dimensional picture is the strongest argument against the trajectory view, and nothing in it explains why the broad-and-shallow region should not extend into the deep one.
- What would settle the cost question? Until a lab discloses, stages 4 and 5 are unfalsifiable.
- Can formalized output be made readable, or does Ono's answer to the trust problem make Tao's digestion problem worse? Formal proofs are the least readable artifacts in mathematics.
- If all three are right about their own field of view, what does the field look like in ten years? Nobody has attempted the synthesis, and this wiki cannot do it from three partisan accounts.
