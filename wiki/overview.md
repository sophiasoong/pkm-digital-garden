---
type: overview
last_updated: 2026-07-07
source_count: 2
page_count: 10
---

## What This Wiki Is About

This wiki is about knowledge management in the LLM era — specifically, how to use LLM agents to build personal knowledge bases that compound over time rather than requiring knowledge to be re-derived on every query.

## Current Synthesis

The central thesis from the first source: **the wiki pattern beats RAG for deliberate, accumulating knowledge work**. The key insight is that knowledge should be compiled *once* at ingest time rather than re-derived on every query. When an LLM agent processes each source into a structured, interlinked wiki — updating concept pages, entity pages, and cross-references — the result is a persistent artifact that gets richer with every addition. This is the compounding property RAG lacks.

A secondary thesis from the same source: in the LLM agent era, **sharing ideas may be more useful than sharing code**. Karpathy's "idea file" format — structured markdown designed to be interpreted by an LLM agent rather than executed directly — represents a potential new format for open knowledge sharing.

Historically, this vision traces to Vannevar Bush's 1945 Memex. Bush's unsolved problem was maintenance: who keeps the associative trails current? LLMs answer that question.

## Established Facts

- RAG re-derives knowledge at query time; LLM Wikis compile knowledge at ingest time, enabling accumulation. ([[sources/antigravity-karpathy-llm-wiki-2026]])
- Three-layer architecture: immutable raw sources, LLM-maintained wiki, and a schema file that governs behavior across sessions. ([[sources/antigravity-karpathy-llm-wiki-2026]])
- At moderate scale (~100 sources), plain-text index navigation is sufficient — no vector database required. ([[sources/antigravity-karpathy-llm-wiki-2026]])
- The maintenance burden is the historical reason human-maintained wikis fail; LLMs solve this by being tireless and systematic. ([[sources/antigravity-karpathy-llm-wiki-2026]])

## Key Tensions

- **Index vs. search**: plain-text `index.md` navigation vs. vector/hybrid search (qmd) — unclear where the crossover point is.
- **Human involvement**: Karpathy prefers staying involved during ingest; fully automated batch ingestion is possible but trades off curation quality.
- **LLM-created vs. human-created trails**: the Memex imagined *user*-created associative links; the LLM Wiki has *LLM*-created links. Whether this is faithful to Bush's vision or a different kind of system is unresolved.
- **Summarization fidelity**: errors introduced during ingest can propagate across many linked pages; there's no automated verification mechanism.

## Biggest Gaps

- No sources yet on RAG systems, vector databases, or the tools in Karpathy's stack (qmd, Obsidian, Dataview).
- No sources on the broader PKM (personal knowledge management) landscape this sits in.
- Vannevar Bush's "As We May Think" (1945) has not been ingested directly — the Memex page draws from Karpathy's brief reference and the secondary analysis.
- No sources capturing real-world reports from people running LLM Wikis at scale.

## What to Investigate Next

- Ingest Vannevar Bush's "As We May Think" (1945) to build out the [[concepts/memex]] page from primary source.
- Find sources on RAG systems to give [[concepts/rag-retrieval]] a more balanced treatment.
- Look for evidence (positive or critical) of people actually running LLM Wikis at scale.
- Ingest the second Antigravity article (Part 1: the original viral tweet coverage) for additional framing.
