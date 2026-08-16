---
type: concept
name: "LLM Wiki"
tags: [knowledge-management, pkm, llm, rag, wiki, compounding-knowledge]
sources: [karpathy-llm-wiki-gist-2026, antigravity-karpathy-llm-wiki-2026]
---

## Definition

An LLM Wiki is a personal knowledge base where an LLM agent incrementally compiles source documents — articles, papers, notes, transcripts — into a structured, interlinked collection of markdown files. Unlike [[concepts/rag-retrieval]] systems that re-derive answers at query time, the LLM Wiki processes each source once at ingest time, building up persistent cross-references, concept pages, entity pages, and syntheses that compound in value over time.

The pattern was articulated by Andrej Karpathy in a GitHub gist published April 4, 2026 (following a viral tweet), and analyzed in depth in [[sources/antigravity-karpathy-llm-wiki-2026]].

## How It Appears in This Wiki

This concept is the primary subject of the first ingested source ([[sources/antigravity-karpathy-llm-wiki-2026]]). The wiki you are currently reading is itself an instantiation of this pattern.

## Key Sources

- [[sources/karpathy-llm-wiki-gist-2026]] — Karpathy's own gist; the primary defining document for this pattern.
- [[sources/antigravity-karpathy-llm-wiki-2026]] — Secondary analysis; covers architecture, tool stack, and historical context in greater depth.

## Architecture

The pattern has three distinct layers:

1. **Raw sources** (`raw/`) — Immutable source documents. The LLM reads but never modifies. This is the ground truth.
2. **Wiki** (`wiki/`) — LLM-maintained markdown files: source summaries, entity pages, concept pages, comparisons, an overview, an index, and a log. The LLM owns this layer entirely.
3. **Schema** (`CLAUDE.md`, `AGENTS.md`, etc.) — A document defining page formats, frontmatter conventions, and workflows. The schema makes the LLM a disciplined wiki maintainer across sessions rather than a generic chatbot. Karpathy: "You and the LLM co-evolve this over time."

Karpathy's analogy: "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

## Core Operations

- **Ingest**: Drop a source into `raw/`, tell the LLM to process it. The LLM reads it, discusses key takeaways, writes a summary page, updates all affected concept and entity pages, updates the index, and logs the activity. A single source may touch 10–15 pages.
- **Query**: Ask the LLM a question. It reads the index, drills into relevant pages, synthesizes an answer with citations. Good answers can be filed back as new wiki pages — explorations compound in the knowledge base just as ingested sources do.
- **Lint**: Periodic health check. The LLM flags contradictions between pages, stale claims, orphan pages (no inbound links), missing concept pages, and suggests new sources to investigate.

## Why Wiki Beats RAG

| Dimension | RAG | LLM Wiki |
|---|---|---|
| Knowledge processing | At query time, per question | At ingest time, once per source |
| Cross-references | Discovered ad-hoc | Pre-built and maintained |
| Contradictions | May go unnoticed | Flagged during ingest |
| Accumulation | None — starts fresh each query | Compounds with every source |
| Output format | Ephemeral chat responses | Persistent markdown files |
| Human role | Upload and query | Curate, explore, question |

At moderate scale (~100 sources), a well-maintained `index.md` is sufficient for navigation — no vector database required. The LLM reads the index to find relevant pages, then reads them directly.

## The Maintenance Insight

The reason human-maintained wikis fail — and why LLM wikis succeed — is the maintenance burden. Updating cross-references, keeping summaries current, flagging contradictions: this grows faster than the value delivered to any single person. LLMs don't get bored, don't forget cross-references, and can update 15 files in one pass. The maintenance cost is near zero.

Karpathy states the division precisely: "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## Modularity

The pattern is explicitly optional and modular — "pick what's useful, ignore what isn't." Image handling, search tooling (qmd), slide deck generation (Marp), frontmatter queries (Dataview) are all enhancements, not requirements. A wiki with text-only sources and no search engine is a valid, complete instantiation.

## Use Cases (from Karpathy)

- **Research**: Going deep on a topic over weeks or months, building an evolving thesis.
- **Personal knowledge**: Tracking goals, health, psychology, self-improvement over time.
- **Reading**: Filing chapters of a book, building character/theme/plot wikis as you read.
- **Business/team**: Internal wiki fed by Slack threads, meeting transcripts, project docs.
- **Everything else**: Competitive analysis, due diligence, course notes, hobby deep-dives.

## Related Concepts

- [[concepts/rag-retrieval]] — The dominant alternative; contrasted directly with LLM Wiki.
- [[concepts/idea-file]] — The format Karpathy used to share this pattern.
- [[concepts/memex]] — Vannevar Bush's 1945 precursor; LLM Wiki solves the maintenance problem Bush couldn't.

## Tensions & Debates

- **Index vs. search**: At what scale does `index.md` break down, requiring a tool like qmd? The source suggests "hundreds of pages" but this is vague.
- **Human involvement**: Karpathy prefers staying involved during ingest, reviewing summaries and guiding emphasis. The schema allows fully automated batch ingestion. Right balance depends on use case.
- **Summarization errors**: If the LLM introduces subtle errors during ingest, they can propagate across many linked pages. There is no automated verification against source truth.

## Open Questions

- What is the practical upper limit of plain-text index navigation?
- How does the pattern hold up when sources heavily contradict each other — does contradiction-flagging work in practice?
- Can the schema file format become a standard analogous to `package.json`?
