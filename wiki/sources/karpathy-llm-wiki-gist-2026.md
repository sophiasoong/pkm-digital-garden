---
type: source
title: "LLM Wiki"
author: "Andrej Karpathy"
date: 2026-04-04
source_type: note
url: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
ingested: 2026-07-07
tags: [llm, knowledge-management, pkm, wiki, rag, idea-file]
---

## Summary

Karpathy's GitHub gist is the primary source document for the LLM Wiki pattern. It is explicitly an "idea file" — designed to be copy-pasted to an LLM agent, which then instantiates a version customized to the user's environment. The document is intentionally abstract and modular: every element (image handling, search tooling, slide decks) is optional, and the right implementation depends on domain and preference.

The core argument is a direct contrast with RAG: instead of re-deriving knowledge at query time, an LLM agent incrementally compiles source documents into a persistent, interlinked wiki. Knowledge is "compiled once and then kept current." The wiki accumulates value with every ingest and every query; RAG starts fresh each time.

The gist defines a clean human/LLM division of labor: the human curates sources, directs analysis, and asks good questions; the LLM handles all the bookkeeping — summarizing, cross-referencing, filing, flagging contradictions, maintaining consistency. The reason this works is that the maintenance burden (updating cross-references, keeping summaries current) is exactly the work humans abandon but LLMs can sustain indefinitely.

Karpathy closes with a brief connection to Vannevar Bush's 1945 Memex — a personal, curated knowledge store with associative trails — and identifies the one problem Bush couldn't solve: who does the maintenance. The LLM handles that.

## Key Points

- **Wiki vs. RAG**: RAG re-derives knowledge at query time; the wiki compiles it at ingest time, creating a persistent, compounding artifact.
- **Three-layer architecture**: immutable raw sources, LLM-maintained wiki (markdown files), schema document (CLAUDE.md / AGENTS.md) that governs the LLM's behavior.
- **Three operations**: ingest (process source, touch 10–15 pages), query (synthesize from wiki; file good answers back), lint (health-check: contradictions, orphans, gaps).
- **index.md replaces RAG for navigation**: at ~100 sources / hundreds of pages, a well-maintained index is sufficient — no embedding infrastructure needed.
- **Explicit modularity**: all tools and techniques are optional. "Pick what's useful, ignore what isn't."
- **Division of labor**: the human curates sources, directs analysis, asks questions. "The LLM's job is everything else."
- **Memex connection**: Bush's 1945 vision of private, curated, associatively linked knowledge — the LLM solves his unsolved maintenance problem.
- **This document is itself an idea file**: "designed to be copy pasted to your own LLM Agent... The document's only job is to communicate the pattern."

## Entities Mentioned

- [[entities/andrej-karpathy]] — Author; his own practice and daily setup described.
- [[entities/vannevar-bush]] — Brief closing reference; intellectual ancestor of the pattern.

## Concepts Mentioned

- [[concepts/llm-wiki]] — The central pattern; this gist is the primary defining document.
- [[concepts/idea-file]] — This gist *is* an idea file; the concept is introduced in the first paragraph.
- [[concepts/rag-retrieval]] — The contrasted alternative; the opening section defines it as the problem.
- [[concepts/memex]] — Brief closing paragraph connecting the pattern to Bush's 1945 vision.

## Connections

- [[sources/antigravity-karpathy-llm-wiki-2026]] — Secondary source that analyzes this gist in depth, adds historical lineage detail, and includes community extensions.

## Quotes

> "The knowledge is compiled once and then kept current, not re-derived on every query."

> "The wiki is a persistent, compounding artifact."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

> "Bush's vision was closer to this than to what the web became: private, actively curated, with the connections between documents as valuable as the documents themselves. The part he couldn't solve was who does the maintenance. The LLM handles that."

> "The document's only job is to communicate the pattern. Your LLM can figure out the rest."

## Questions Raised

- How should the schema co-evolve with the wiki — what signals indicate it needs updating?
- At what point does the index approach break down and require a proper search layer (qmd)?
- How does the pattern change for domains with rapidly-shifting source material (vs. stable research topics)?
