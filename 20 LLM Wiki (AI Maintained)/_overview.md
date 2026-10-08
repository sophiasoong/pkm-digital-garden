---
type: overview
last_updated: 2026-10-06
source_count: 11
page_count: 45
---

## What This Wiki Is About

Three unconnected clusters, accumulated in roughly this order: **design** (color, usability, interface materials), **philosophy** (Stoic practice, Taoist non-dualism, Blake on attention), and **mathematics under automation** (what AI is doing to mathematical practice, and what mathematicians think it is for).

Nothing planned the three. They came from what the human clipped. But a thread has started to run between them that none of the individual sources is about, and holding that thread is what this page is for.

## Current Synthesis

**The thread: what a thing communicates versus what it contains, and what happens when the hard part gets removed.**

It shows up independently in all three clusters, which is why it is worth stating as the wiki's emerging thesis rather than as a coincidence.

In **design**, the recurring finding is that properties live in relationships, not in things. A color has no fixed appearance — the visual system exaggerates differences, and there is no neutral backdrop [[22 Concepts/color-relativity]]. Stimulation is not a property of a color but of a combination, and behaves like a budget rather than a value to maximize [[22 Concepts/color-stimulation]]. Liquid Glass is defined by optical behavior across frames and is nearly invisible in a still image [[22 Concepts/liquid-glass]]. Material Design's own research instrument measures what an interface *says* — hierarchy, utility, style — as distinct from what it does [[22 Concepts/hierarchy-utility-style]]. Four sources, one shape: the thing itself is the wrong unit of analysis.

In **philosophy**, two sources refuse a hierarchy that treats the immediate as lesser than something held elsewhere. Lao Tzu via Le Guin drops the mind/body split rather than adjudicating it — "you are your body" [[22 Concepts/mind-body]], [[22 Concepts/dualism]]. Blake locates the vast inside the small, available through attention rather than by going somewhere bigger [[22 Concepts/attentive-perception]]. The Stoic material adds the practical arm: chosen hardship as maintenance of capacity and reduction of dependency [[22 Concepts/voluntary-discomfort]], [[22 Concepts/stoicism]].

In **mathematics**, three partisan sources disagree about AI while agreeing on the structure of the problem: a field whose honors attach to the difficulty of a task rather than the value of the result, meeting a technology that removes the difficulty [[22 Concepts/status-economy-of-expertise]], [[22 Concepts/ai-in-mathematics]].

**And then the clusters touched.** Terence Tao, describing how mathematical research actually works, arrives at the voluntary-discomfort conclusion with no ethical vocabulary at all: the repeated failure is the mechanism, not the cost, and a tool that removes it removes what it was building. His image is hiking to a waterfall, getting lost, and seeing something on the way — against being flown there and back [[22 Concepts/failure-as-method]]. That is the Stoic argument reached from research methodology by someone who had no interest in making it, which is the strongest thing in this wiki, because nobody was aiming for it.

The synthesis, stated as plainly as the material supports: **across design, philosophy and research practice, this wiki's sources keep finding that the valuable property is in the process or the relationship rather than in the artifact — and that tools which deliver the artifact while skipping the process are therefore not neutral improvements.** This is a pattern across eleven sources, not a demonstrated claim. It should be treated as the wiki's working hypothesis and actively tested against the next source rather than confirmed by it.

## Established Facts

Well-supported means two or more independent sources here, which is a low bar the wiki clears rarely. Most of what follows is better described as well-documented than established.

- **Color appearance is contextual and no backdrop is neutral.** Two Duru sources, with the lineage credited to Josef Albers. The later source supersedes the earlier one's framework by the same author's own account [[22 Concepts/color-relativity]], [[22 Concepts/halfway-color-combinations]].
- **Usability has a five-aspect operational definition** (efficiency, errors, learnability, memorability, satisfaction) adopted by Material Design from NN/g, and it is distinct from accessibility rather than a synonym [[22 Concepts/usability]].
- **The Roman Stoic voluntary-discomfort practice is documented across argument, protocol and biography** — Musonius Rufus, Seneca's Letter 18, Cato's life. One source, but internally triangulated [[22 Concepts/voluntary-discomfort]].
- **Something changed in automated mathematical reasoning in 2025–2026, recently rather than gradually.** All three mathematics sources agree, and two independently name the Erdős unit distance conjecture as a real case, with one attributing it to OpenAI [[22 Concepts/ai-in-mathematics]].
- **Theory-building is the furthest thing from automation, and it is what mathematics mostly consists of.** All three mathematics sources agree. The only unanimous substantive claim in that cluster.
- **Liquid Glass forced a legibility retreat.** The material shipped and was then walked back under accessibility pressure, which is a fact about events rather than an interpretation [[22 Concepts/liquid-glass]].

## Key Tensions

**The wiki's first genuine multi-source dispute: what AI in mathematics is for.** Three working mathematicians, two employed on the AI side, no citations between them. Szegedy says trajectory — current limits are properties of the moment, not the technology. Tao says complementarity — the single difficulty axis is the error; humans go deep, machines go broad, and more breadth does not become depth. Ono says verifiability — not a race for compute but a race for truth, and output that cannot be checked is not worth having. Full map on [[22 Concepts/ai-in-mathematics]]; the sharpest collision is that Szegedy's forecast of cheap access is flatly contradicted by Tao's report that costs are undisclosed, instruments privately owned, and perhaps 1% of problems amenable.

**Hardship as capacity versus hardship as currency.** [[22 Concepts/voluntary-discomfort]] treats chosen difficulty as capacity-building and warns explicitly against practicing it for status. [[22 Concepts/status-economy-of-expertise]] describes a professional culture where difficulty *is* the status currency. Both are in this wiki, neither source knows about the other, and the tension is unresolved. Ono sharpens it further: he thinks the currency was corrupt to begin with, not merely about to collapse [[22 Concepts/benchmark-critique]].

**Expressive material versus measured usability.** Apple shipped a material whose defining property is also its failure mode; Material Design built an instrument to measure whether expressive changes cost comprehension. The two vendors are running opposite bets, and this wiki holds each one's own account of itself [[22 Concepts/liquid-glass]], [[22 Concepts/hierarchy-utility-style]].

**Precision through abstraction versus precision through attention.** Tao argues number is what lets you describe a quantity exactly to someone who never saw the thing, where poetic language blurs and degrades in transit. Blake argues close attention to the small is what reveals the vast. Both are claims about precision; they disagree about which register delivers it. A thin link, flagged on [[22 Concepts/attentive-perception]] and not yet built out.

**Every mathematics source is an interested party.** Three accounts of one field, none independent, none citing anything, two of them machine-generated transcripts with visible garbling. Three partisan accounts that disagree are more useful than one — but this is not confirmation, and the wiki should stop treating the disagreement as triangulation.

## Biggest Gaps

- **No source on formalization and AI safety.** The most specific gap, because the human has already made the connection in a permanent note that the wiki cannot support: formalization matters for safety and alignment in AI agents. Ono's case for formalization is epistemic, about trusting a proof. Extending it to agent behavior is a different object. Flagged on [[22 Concepts/formalization]]. One targeted source would settle whether this is a live bridge or a plausible guess.
- **No independent source on AI in mathematics.** Everything in the cluster comes from participants. A paper, a repository, a journalist, or a skeptic with standing would change how all three forecasts should be read — and would finally verify or sink the Erdős claim.
- **The status-economy pattern has three instances and all are mathematics.** The concept was written in general terms deliberately, to be linked from other domains. Nothing has linked to it from outside yet, so its portability is asserted and untested.
- **Design cluster is vendor-dominated.** Google and Apple describing their own design languages, plus one independent designer. No academic perception research, no critical voice, no practitioner who dislikes any of it.
- **Philosophy cluster is three sources and no modern treatment.** Stoicism via a content channel, Taoism via Le Guin, Blake via four lines. Nothing contemporary, nothing critical of any of it.
- **The cross-cluster thesis rests on one accidental convergence.** The Tao/Stoic agreement on failure is the only place the clusters actually touch on substance. One connection is a promising coincidence, not a thesis.
- **Nothing on mathematics education.** Surfaced by [[Queries/tao-on-learning-math]]: asked why Tao thinks learning mathematics matters now, the wiki found he never addresses it, and no other source does either. Ono comes closest but is about benchmarks, admissions and who gets identified as talented — selection, not teaching [[22 Concepts/benchmark-critique]]. The one education-adjacent claim the wiki holds, Tao's standards paradox, is asserted from personal experience by a single mathematician and would be exactly the kind of thing education research has studied.
- **QUERY is underused relative to INGEST.** Eleven sources have produced one filed answer and one lint report. The first real query immediately turned up a gap no amount of page-by-page ingesting had named, which is an argument for asking the wiki questions more often than it currently gets asked.

## What to Investigate Next

Ranked by how much each would change this page.

1. **A formalization-and-alignment source.** Closes the one gap the human has already walked into. Highest value per source in the wiki right now.
2. **An independent or skeptical source on AI in mathematics.** Ideally one that names results and systems. Would convert the cluster's central dispute from three assertions into something assessable.
3. **A non-mathematics instance of the status economy.** Any field whose honors attach to difficulty meeting a tool that removes it — medicine, translation, illustration, software. Would test whether the concept is portable or a mathematics artifact.
4. **A critical design source.** Something that pushes back on either vendor rather than explaining them. The cluster currently has no adversarial reading.
5. **Revisit Szegedy's forecast on schedule.** It commits to a months-scale timeline, which is unusual and checkable. Stages 2 and 4 are both dated and both now partly contradicted. This is the wiki's one falsifiable prediction and should be returned to deliberately rather than left standing.
6. **File some queries.** Asking the wiki a question that spans two clusters is the fastest way to find out whether the thread in Current Synthesis is real or whether it is a pattern this page talked itself into.

---

*Maintained per root `CLAUDE.md`. Page count matches [[_index]]: source + entity + concept pages in this folder (11 + 15 + 19). This page and `_index` / `_log` are infrastructure and not counted.*
