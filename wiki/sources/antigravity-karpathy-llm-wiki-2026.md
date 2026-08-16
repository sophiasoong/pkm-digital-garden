---
type: source
title: "Karpathy's LLM Wiki: The Complete Guide to His Idea File"
author: "Antigravity.codes"
date: 2026-04-04
source_type: article
url: https://antigravity.codes/blog/karpathy-llm-wiki-idea-file
ingested: 2026-05-02
tags: [llm, knowledge-management, pkm, karpathy, rag, wiki]
---

## Summary

Antigravity.codes provides a comprehensive analysis of Andrej Karpathy's "LLM Wiki" idea file — a GitHub gist published April 4, 2026, following a viral tweet about using LLMs to build personal knowledge wikis. This is a secondary source: it is not Karpathy's original writing, but a third-party deep-dive that quotes him extensively and contextualizes the full architecture.

The core proposal contrasts the dominant RAG approach — where an LLM re-derives answers from raw documents on every query — with a wiki-based approach where an LLM incrementally compiles source documents into a persistent, structured, interlinked knowledge base. The key advantage is that knowledge accumulates over time rather than being rediscovered from scratch on every question.

Karpathy introduces a second concept alongside the wiki: the "idea file" — a structured markdown description of a pattern designed to be interpreted by an LLM agent rather than cloned as code. This meta-contribution may be as significant as the wiki pattern itself, representing a new format for sharing in the LLM agent era.

The article closes with a historical connection to Vannevar Bush's 1945 Memex, framing the LLM Wiki as finally solving the maintenance problem that prevented private, curated knowledge stores from becoming practical.

## Key Points

- RAG re-derives knowledge at query time; the LLM Wiki compiles knowledge at ingest time, enabling accumulation.
- Three-layer architecture: `raw/` (immutable sources), `wiki/` (LLM-maintained markdown files), schema (`CLAUDE.md` or `AGENTS.md`).
- Three core operations: ingest (process source, update all affected pages), query (synthesize from wiki, optionally file the answer), lint (health check for contradictions, orphans, gaps).
- At moderate scale (~100 sources), a well-maintained `index.md` is sufficient for navigation — no vector database required.
- The "idea file" format: share patterns rather than code, letting each person's LLM agent instantiate a custom version.
- Karpathy's analogy: "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."
- LLMs solve the maintenance problem that causes human-maintained wikis to fail: they don't get bored, don't forget cross-references, and can touch 15 files in one pass.
- Historical lineage: Vannevar Bush's Memex (1945) → Douglas Engelbart → Ted Nelson (hypertext) → Tim Berners-Lee (web) → LLM Wiki.

## Entities Mentioned

- [[entities/andrej-karpathy]] — Creator of the LLM Wiki pattern; co-founder of OpenAI, former AI lead at Tesla, coined "vibe coding."
- [[entities/vannevar-bush]] — Described the Memex in 1945; Karpathy identifies him as the direct intellectual ancestor of the LLM Wiki.
- Tobi Lutke — CEO of Shopify; creator of qmd, the local markdown search engine Karpathy recommends.
- Douglas Engelbart — Read Bush's 1945 article and went on to invent the mouse and personal computing.
- Ted Nelson — Coined "hypertext" in 1965, directly inspired by the Memex's associative trails.
- Tim Berners-Lee — Created the World Wide Web (1989), implementing hypertext at global scale.

## Concepts Mentioned

- [[concepts/llm-wiki]] — The central pattern: LLM-maintained personal knowledge wikis.
- [[concepts/idea-file]] — Karpathy's proposed new format for sharing patterns in the LLM agent era.
- [[concepts/rag-retrieval]] — The dominant approach being contrasted; retrieving from raw documents at query time.
- [[concepts/memex]] — Vannevar Bush's 1945 concept; intellectual predecessor of the LLM Wiki.

## Connections

- [[concepts/llm-wiki]] — Primary concept this source establishes in full detail.
- [[concepts/idea-file]] — Secondary concept introduced simultaneously in Karpathy's gist.
- [[concepts/memex]] — Historical predecessor; Karpathy explicitly invokes it to frame the problem.
- [[concepts/rag-retrieval]] — The contrasted approach; understanding RAG is necessary to understand the wiki's advantages.

## Quotes

> "The LLM is rediscovering knowledge from scratch on every question. There's no accumulation."

> "The knowledge is compiled once and then kept current, not re-derived on every query."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass. The wiki stays maintained because the cost of maintenance is near zero."

> "The document's only job is to communicate the pattern. Your LLM can figure out the rest."

> "Wholly new forms of encyclopedias will appear, ready-made with a mesh of associative trails running through them." — Vannevar Bush, 1945 (quoted by Karpathy)

## Questions Raised

- At what scale does `index.md` break down and require qmd or a proper vector search layer?
- How does the LLM Wiki handle the risk of summarization errors propagating across many linked pages?
- Could the idea file format evolve into a standardized schema with versioning and a community registry?
- Is the LLM Wiki more like Bush's Memex (user-directed associative trails) or something new (LLM-directed connections)?
