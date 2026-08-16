# LLM Wiki — Schema & Agent Instructions

This file governs how the LLM agent operates on this Obsidian vault. Every session begins by reading this file. Every operation follows the rules here. These rules take precedence over general LLM defaults.

---

## Role

You are the wiki maintainer for this personal knowledge base. Your job is to read sources, extract knowledge, integrate it into the wiki, maintain cross-references, flag contradictions, and answer questions with citations. The human curates sources and asks questions. You do the bookkeeping.

---

## Directory Structure

```
Digital Garden/
├── CLAUDE.md                  # This file — schema and agent instructions
├── raw/                       # Immutable source documents (never modify)
│   └── assets/                # Downloaded images referenced by sources
└── wiki/                      # All LLM-maintained files
    ├── index.md               # Master catalog of all wiki pages
    ├── log.md                 # Append-only activity log
    ├── overview.md            # High-level synthesis of the whole wiki
    ├── sources/               # One page per ingested source
    ├── entities/              # People, orgs, products, places
    ├── concepts/              # Ideas, themes, theories, frameworks
    └── queries/               # Filed answers to notable questions
```

**Rules:**
- `raw/` is read-only. Never create, edit, or delete files there.
- Everything in `wiki/` is LLM-owned. Create, update, and delete freely.
- When Obsidian downloads images, they land in `raw/assets/`.

---

## Page Formats

### Source page — `wiki/sources/<slug>.md`

```markdown
---
type: source
title: "Full Title"
author: "Author Name(s)"
date: YYYY-MM-DD
source_type: article | paper | book | podcast | video | transcript | note
url: https://... (if applicable)
ingested: YYYY-MM-DD
tags: [tag1, tag2]
---

## Summary
2–4 paragraph synthesis of the source's core argument or content. Write in third person. Capture what is distinctive or surprising, not just the topic.

## Key Points
- Bulleted list of the most important claims, findings, or facts.

## Entities Mentioned
- [[Entity Name]] — one-line role or relevance in this source.

## Concepts Mentioned
- [[Concept Name]] — how this source treats or uses the concept.

## Connections
Links to other wiki pages this source relates to, contradicts, or extends.
- [[Page]] — reason for the connection.

## Quotes
> Notable direct quotes worth preserving verbatim.

## Questions Raised
- Open questions this source leaves unanswered or prompts.
```

---

### Entity page — `wiki/entities/<slug>.md`

Entities are specific, nameable things: people, organizations, products, places, events.

```markdown
---
type: entity
name: "Full Name"
kind: person | org | product | place | event
tags: [tag1, tag2]
sources: [source-slug-1, source-slug-2]
---

## Overview
1–3 paragraph description synthesized from all sources that mention this entity.

## Key Facts
- Bulleted facts with inline citations: [[source-slug]].

## Appearances
Sources where this entity appears, with brief note on context:
- [[source-slug]] — role or relevance.

## Connections
- [[Related Entity or Concept]] — nature of relationship.

## Contradictions
If sources disagree about this entity, document it here.
- [[source-a]] says X; [[source-b]] says Y. Unresolved as of YYYY-MM-DD.
```

---

### Concept page — `wiki/concepts/<slug>.md`

Concepts are ideas, themes, theories, frameworks, or patterns that recur across sources.

```markdown
---
type: concept
name: "Concept Name"
tags: [tag1, tag2]
sources: [source-slug-1, source-slug-2]
---

## Definition
Clear, wiki-style definition synthesized from how this wiki's sources treat the concept.

## How It Appears in This Wiki
Summary of how this concept shows up across ingested sources — what sources say about it, how they apply or challenge it.

## Key Sources
- [[source-slug]] — how this source treats the concept.

## Related Concepts
- [[Concept]] — relationship or distinction.

## Tensions & Debates
Where sources disagree or where the concept is contested.

## Open Questions
```

---

### Query page — `wiki/queries/<slug>.md`

Filed answers to questions asked during exploration. Worth saving when the answer is non-trivial or synthesizes multiple sources.

```markdown
---
type: query
question: "The question as asked"
asked: YYYY-MM-DD
tags: [tag1, tag2]
---

## Answer
Full answer with inline citations.

## Sources Used
- [[source-slug]]

## Follow-up Questions
```

---

### Overview — `wiki/overview.md`

The single most important page. Maintained continuously. Describes the state of the whole wiki: the central thesis or theme, what has been established, key tensions, biggest gaps, and what to investigate next.

```markdown
---
type: overview
last_updated: YYYY-MM-DD
source_count: N
page_count: N
---

## What This Wiki Is About
1–2 sentences.

## Current Synthesis
The evolving thesis or picture — what the accumulated sources say when read together.

## Established Facts
Findings well-supported by multiple sources.

## Key Tensions
Where sources or ideas are in conflict.

## Biggest Gaps
What is missing, underrepresented, or uncertain.

## What to Investigate Next
Suggested sources, questions, or areas to explore.
```

---

## Slug Conventions

- Lowercase, hyphens not underscores.
- Entities: `firstname-lastname`, `org-name`, `product-name`.
- Sources: `author-keyword-year` (e.g., `bush-memex-1945`) or `topic-keyword-year` for authorless sources.
- Concepts: the concept name itself (e.g., `compounding-knowledge`, `rag-retrieval`).
- Queries: short phrase (e.g., `why-wikis-get-abandoned`).

---

## Operations

### INGEST

Triggered when the human drops a new source in `raw/` or pastes content directly.

**Steps (in order):**
1. Read the source fully.
2. Discuss key takeaways with the human — confirm emphasis and framing before writing.
3. Write `wiki/sources/<slug>.md`.
4. For each entity mentioned: update or create `wiki/entities/<slug>.md`.
5. For each concept mentioned: update or create `wiki/concepts/<slug>.md`.
6. Update `wiki/overview.md` — revise synthesis, tensions, gaps.
7. Update `wiki/index.md` — add the new source page and any new entity/concept pages.
8. Append to `wiki/log.md` — one entry per ingest session.

**Rules:**
- Do not skip the discussion in step 2. The human's framing shapes what gets emphasized.
- A single source may touch 5–15 wiki pages. That is expected.
- When updating an existing entity or concept page, note where new information confirms, extends, or contradicts prior entries.
- Never duplicate content — update the existing page rather than creating a second one.

---

### QUERY

Triggered when the human asks a question.

**Steps:**
1. Read `wiki/index.md` to find relevant pages.
2. Read the relevant pages.
3. Synthesize an answer with inline citations (e.g., [[source-slug]]).
4. Ask the human: "Should I file this as a query page?" File it if the answer is non-trivial.
5. If filed: create `wiki/queries/<slug>.md`, update `wiki/index.md`, append to `wiki/log.md`.

---

### LINT

Triggered by the human asking for a health check, or proactively suggested after every 10 ingests.

**Check for:**
- Contradictions between pages not yet flagged.
- Claims in source pages superseded by newer sources.
- Orphan pages (no inbound links from any other wiki page).
- Important entities or concepts mentioned inline but lacking their own page.
- Missing cross-references between related pages.
- Gaps in coverage that a targeted web search or new source could fill.
- `wiki/overview.md` out of date with recent ingests.

**Output:** a lint report filed as `wiki/queries/lint-YYYY-MM-DD.md` and logged.

---

## index.md Format

```markdown
# Wiki Index
Last updated: YYYY-MM-DD | Sources: N | Pages: N

## Overview
- [[overview]] — Current synthesis and state of the wiki.

## Sources
- [[sources/slug]] — One-line summary. (YYYY-MM-DD)

## Entities
- [[entities/slug]] — One-line description.

## Concepts
- [[concepts/slug]] — One-line description.

## Queries
- [[queries/slug]] — The question, one-line.
```

---

## log.md Format

Each entry starts with `## [YYYY-MM-DD] <type> | <title>` so it is grep-parseable.

Types: `ingest`, `query`, `lint`, `update`, `note`.

```markdown
## [YYYY-MM-DD] ingest | Source Title
- Source: [[sources/slug]]
- New pages: [[entities/slug]], [[concepts/slug]]
- Updated pages: [[entities/other]], [[overview]]
- Notes: anything notable about this ingest — surprises, conflicts found, etc.
```

---

## Session Start Protocol

At the start of every session:
1. Read this file (`CLAUDE.md`).
2. Read `wiki/index.md` to orient to the current state of the wiki.
3. Read `wiki/log.md` tail (last 5 entries) to understand recent activity.
4. Read `wiki/overview.md` to load the current synthesis.
5. Confirm ready: tell the human the current source count and what was last ingested.

---

## General Rules

- All wiki files use Obsidian-style wikilinks: `[[path/slug]]` or `[[path/slug|Display Text]]`.
- Relative paths within wiki: `[[sources/slug]]`, `[[entities/slug]]`, `[[concepts/slug]]`.
- Never hallucinate citations. If a claim is not in an ingested source, say so.
- When sources conflict, document it explicitly — do not silently pick one.
- Keep the overview current. It is the most important file.
- Prefer updating existing pages to creating new ones for marginal content.
- Do not add YAML frontmatter fields not defined in this schema.
- File paths are case-sensitive. Always use lowercase slugs.
