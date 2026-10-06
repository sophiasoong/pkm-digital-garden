---
type: concept
name: "Formalization"
tags: [mathematics, ai, verification, proof, safety]
sources: [ono-nine-lessons-2026, tao-six-essentials-2026]
---

## Definition

Formalization is the translation of ordinary mathematical or technical language into machine-checkable code, such that a claim's correctness becomes a thing a computer can establish rather than a thing a reader must be persuaded of. In the account this wiki holds, it has two faces. As a technique it produces certainty: once a proof is expressed in a proof-assistant language and checked, the statement is true, and if there is a mistake it is because the problem was framed wrong [[23 Sources/tao-six-essentials-2026]]. As a programme it is a claim about where effort should go — one source names it as a distinct third form of AI, alongside chatbots and machine-learning search, and locates nearly all his hope for the field's future in it [[23 Sources/ono-nine-lessons-2026]].

The second framing carries a less obvious claim. Formalizing a subject does not merely confirm what was already known; it reveals that the original framing was incomplete. The work is not transcription but reconstruction, and the reconstruction can change the result.

## How It Appears in This Wiki

Through two independent sources, which is unusual for this wiki's newest domain and worth stating plainly: formalization is the one thing both mathematicians discuss, and they do not contradict each other. They differ in what they want from it. Tao treats it as a stage in the life cycle of a proof and as the thing that finally settled a centuries-old conjecture. Ono treats it as an industrial programme, a jobs forecast, and a safety argument.

## The Two Worked Cases

**The Kepler conjecture, as the certainty case.** The claim that hexagonal close packing of spheres is optimal — about 76% efficient — was proposed by Kepler and resisted proof for centuries. Two dimensions fell around 1900; three dimensions was published in 1998 as one of the first computer-assisted proofs, and the referees reported that they could not verify all the computations, believed the strategy was correct, and left lingering doubts. Only around 2014 was the proof converted into a proof-assistant language, after which, on Tao's account, we are 100% certain it is true. There is still no simple proof a human can hold entire [[23 Sources/tao-six-essentials-2026]].

**Mathematical economics, as the revision case.** Ono's group at [[21 Entities/axiom-math]], working with a Harvard mathematical economist, reports that formalizing foundational theorems in economics showed that some were not accurately portrayed, implemented or applied. The stated example is Robert Aumann's theorem on whether parties reasoning from the same prior knowledge can agree to disagree — fifty years old in 2026. The theorem does not permit the thing its popular name describes: what actually happens is that the parties come to understand each other's perspectives. The subtleties live in the hypotheses, in particular what it means to share priors, and that is where formalization did its work. Ono describes the result as a viral moment in mathematical economics [[23 Sources/ono-nine-lessons-2026]].

## The Programme Argument

Ono's case for formalization as a direction, rather than a tool, has four parts:

1. **Verification is where AI is actually trustworthy.** Have the system examine the code for vulnerabilities, not the prose for plausibility.
2. **The surface area is enormous and growing.** A large and rising share of deployed code is not written by human programmers, and it is not perfect. Anything controlled by a mathematical language after translation is a candidate.
3. **It is a jobs forecast.** Cybersecurity needing legions of computer scientists, plus ethicists and lawyers; formalization specialists building the guardrails. His advice to students who want to be mathematicians is to start formalizing now, while allowing that they may still prove unsolved conjectures along the way.
4. **It reframes the race.** This is the point where his source and this wiki's other AI-and-mathematics source part company: he does not believe 2026 and 2027 should be a race for more compute, but a race for more truth, by means of formalization.

## Noted in the Zettelkasten

The human wrote a permanent note while watching [[23 Sources/ono-nine-lessons-2026]], timestamped between the two mathematics ingests of 2026-10-06: [[30 Zettelkasten (Human)/2026-10-06T150200 - AI formalization with math structures is important for safety and alignment issues in AI development|AI formalization with math structures is important for safety and alignment issues in AI development]].

It restates the definition above — translating human knowledge and reasoning into mathematical structures and code so computers can verify, process and perform — and then adds a claim that **is not in any source this wiki holds**: that formalization matters for safety and alignment in AI agents. Ono's case for formalization is epistemic, about whether a proof can be trusted. The note extends it to agent behavior, which is a different object. Recorded here as the human's own inference rather than as a finding, per the no-hallucinated-citations rule.

Worth flagging because the extension is a reasonable one and the wiki cannot currently support it. If it is right, formalization stops being a topic inside [[22 Concepts/ai-in-mathematics]] and becomes a bridge between this wiki's mathematics cluster and a safety literature it holds nothing from. That makes it the most specific gap on [[_overview]] — a targeted source would settle whether the connection is live or merely plausible.

## Key Sources

- [[23 Sources/ono-nine-lessons-2026]] — the programme, the taxonomy that makes formalization a form of AI in its own right, and the economics case.
- [[23 Sources/tao-six-essentials-2026]] — the Kepler conjecture case; formal verification as the end of a proof's doubt; and the observation that formal verification is a binary, not judgment.

## Related Concepts

- [[22 Concepts/ai-in-mathematics]] — formalization is Ono's alternative to the trajectory forecast, so it is a position in that debate, not just a technique.
- [[22 Concepts/research-bottleneck-shift]] — verification is one of the stages Tao says is automating. What formalization does *not* relieve is the digestion that comes after.
- [[22 Concepts/benchmark-critique]] — the same source's two halves. Benchmarks measure the wrong thing; formal verification measures the only thing that admits a yes or no.

## Tensions & Debates

**Certainty about the statement is not understanding of the proof.** The Kepler case is the clean illustration: formally verified, and still with no proof a human can grasp whole. Formalization converts "we believe this" into "this is true" without converting it into "we see why." Tao's own bottleneck argument implies that the part it does not deliver is the part that was scarce.

**Formal verification is not judgment, and the source says so.** Tao's framing is that a formally verified fact is a yes-no binary, and judgment is how people choose to act on information. Ono agrees independently — his line is that a large language model is the most incredible librarian, one who has read everything, but you would not want your librarian to be your neurosurgeon. So the programme's reach stops exactly where the stakes rise, which is an odd shape for a safety argument to have.

**Garbage in, formally verified garbage out.** If a mistake can only be a framing error, then framing carries the whole load, and nothing in either source addresses who checks the translation from natural language into code. The economics case cuts both ways here: it is offered as evidence that formalization catches errors, and it is equally evidence that a field's foundational statements had been mis-stated for fifty years by people reading the formal result in natural language.

**The programme is recommended by someone employed to run it.** Ono's answer to AI displacing mathematicians is a programme his own company pursues, and his advice to students is to enter it. The self-disclosure is partial — he says repeatedly that he works at an AI company — but the interview never turns the conflict-of-interest observation on this particular recommendation. See [[21 Entities/axiom-math]].

**One citation, one anniversary.** The Aumann finding is the only concrete evidence in this wiki that formalization revises foundations, it is reported by a participant, and no paper or repository is named.

## Open Questions

- Who is qualified to do this? It demands both domain mastery and proof-assistant fluency, a narrower population than either field alone — and Ono recommends students enter a pipeline whose existence the interview does not describe.
- What is the cost ratio? The Kepler conjecture went from computer-assisted proof in 1998 to formal verification around 2014. If that gap is typical, "verification is automating" and "verification is fast" are different claims.
- Does formalizing a field change what the field rewards? If a result's status no longer depends on a reader being convinced, the social machinery described in [[22 Concepts/status-economy-of-expertise]] loses one of its functions.
- Which of the economics theorems were mis-applied, and with what consequences downstream? A fifty-year misreading of a foundational theorem in a policy-adjacent field is either a big deal or a technicality, and this wiki cannot tell which.
- If AI writes most deployed code and AI checks it, what independent check remains? Ono's guardrail argument has AI guardrailing AI, and the human role he names is ethics and law rather than verification.
