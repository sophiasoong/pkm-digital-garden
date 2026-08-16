---
type: concept
name: "Memex"
tags: [knowledge-management, history, hypertext, bush, associative-trails]
sources: [karpathy-llm-wiki-gist-2026, antigravity-karpathy-llm-wiki-2026]
---

## Definition

The Memex (memory + index) was a hypothetical desk-sized device described by [[entities/vannevar-bush]] in his 1945 *Atlantic* article "As We May Think." It would let an individual store all their books, records, and communications on microfilm, search them rapidly, and create **associative trails** — personally annotated, linked sequences of documents following the user's own logic rather than any hierarchical classification.

Bush's core insight: the human mind works by association, not alphabetical order. Rigid filing systems force categories that don't match how people actually think. The Memex would let users build their own paths through knowledge.

His famous line: "Wholly new forms of encyclopedias will appear, ready-made with a mesh of associative trails running through them."

## How It Appears in This Wiki

Referenced in [[sources/antigravity-karpathy-llm-wiki-2026]] as the direct intellectual predecessor of the [[concepts/llm-wiki]] pattern. Karpathy explicitly invokes Bush's vision and identifies the maintenance problem as the gap LLMs now solve.

## Key Sources

- [[sources/karpathy-llm-wiki-gist-2026]] — Karpathy's own brief statement of the connection (one paragraph at the end of the gist).
- [[sources/antigravity-karpathy-llm-wiki-2026]] — Secondary analysis that expands the Memex reference into a full historical lineage.

## Historical Lineage

The Memex directly inspired a chain of foundational computing work:

- **Douglas Engelbart** — Read "As We May Think" in 1945, "became infected with the idea," and went on to invent the computer mouse and the concept of personal computing.
- **Ted Nelson** — Coined "hypertext" in 1965, directly inspired by the Memex's associative trails.
- **Tim Berners-Lee** — Created the World Wide Web (1989), implementing hypertext at global scale.

But the web became *public and chaotic* rather than *private and curated*. Bush had imagined something personal — your knowledge, your connections, your trails.

## The Maintenance Gap

The critical unsolved problem in Bush's 1945 vision: **who does the maintenance?** Creating and sustaining associative trails, updating connections, keeping everything consistent — that's tedious, manual work. Humans abandon knowledge systems because the maintenance burden grows faster than the value.

Karpathy's answer, in his own words: "Bush's vision was closer to this than to what the web became: private, actively curated, with the connections between documents as valuable as the documents themselves. The part he couldn't solve was who does the maintenance. The LLM handles that."

## Related Concepts

- [[concepts/llm-wiki]] — The modern realization of Bush's vision; solves the maintenance problem via LLM.

## Tensions & Debates

The Memex and the LLM Wiki differ in one significant way: Bush imagined *human-created* associative trails — the user's own intellectual connections. The LLM Wiki has *LLM-created* connections. Whether this is a fulfillment of Bush's vision or a different kind of system is an open question.

## Open Questions

- Does having an LLM create the associative trails rather than the user fundamentally change the nature of the system?
- The Memex was explicitly personal and private; is the LLM Wiki equally so given it runs on cloud LLM infrastructure?
