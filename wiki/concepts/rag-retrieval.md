---
type: concept
name: "RAG (Retrieval-Augmented Generation)"
tags: [llm, knowledge-retrieval, search, vector-databases]
sources: [karpathy-llm-wiki-gist-2026, antigravity-karpathy-llm-wiki-2026]
---

## Definition

Retrieval-Augmented Generation (RAG) is the dominant pattern for connecting LLMs to private document collections. At query time, the system searches for relevant chunks from the document corpus (typically using vector/semantic search), feeds those chunks to the LLM in context, and generates an answer. Examples include Google NotebookLM, ChatGPT file uploads, and most enterprise AI search tools.

## How It Appears in This Wiki

Introduced in [[sources/antigravity-karpathy-llm-wiki-2026]] primarily as the contrasted alternative to the [[concepts/llm-wiki]] pattern. Karpathy's critique is the framing device for why the wiki approach is superior for knowledge accumulation.

## Key Sources

- [[sources/karpathy-llm-wiki-gist-2026]] — Karpathy's own framing; defines RAG as the problem the LLM Wiki solves.
- [[sources/antigravity-karpathy-llm-wiki-2026]] — Secondary analysis with side-by-side comparison table.

## RAG's Core Limitation (per Karpathy)

"The LLM is rediscovering knowledge from scratch on every question. There's no accumulation."

- Knowledge is processed at query time on every request, not at ingest time once
- Cross-document synthesis requires finding and assembling fragments on the fly, every time
- Contradictions between documents may go unnoticed
- Answers are ephemeral chat responses, not persistent artifacts

## When RAG Is Still Appropriate

RAG is not obsolete. It remains better suited when:
- The corpus changes too rapidly for wiki maintenance to keep up
- Documents are too numerous or low-quality to justify careful curation
- The use case is lookup/retrieval rather than synthesis and exploration over time
- Latency and infrastructure constraints favor a stateless retrieval approach

The LLM Wiki is better suited to deliberate knowledge accumulation over weeks or months on a focused topic.

## Related Concepts

- [[concepts/llm-wiki]] — The alternative pattern; processes knowledge at ingest time rather than query time.

## Open Questions

- At what corpus size does the LLM Wiki's index-based navigation start to require RAG-like infrastructure?
- Can hybrid approaches combine RAG's scalability with the wiki's compounding property?
