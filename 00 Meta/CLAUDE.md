# Vault Governance — Two-Zone Ownership Model

This document describes the folder structure and ownership rules for this Obsidian vault. The root `CLAUDE.md` contains the agent's detailed operational schema (page formats, slug conventions, ingest/query/lint workflows). This file describes the higher-level organization.

---

## Folder Map

```
Digital Garden/
├── CLAUDE.md                        # Agent operational schema (root — do not move)
├── 00 Meta/                         # Vault infrastructure
│   ├── CLAUDE.md                    # This file — vault governance
│   └── Templates/                   # Note templates for both zones
│
├── 10 Inbox & Raw/                  # Human staging area
│   ├── Web Clips/                   # Clipped articles (markdown from Web Clipper)
│   ├── PDFs & EPUBs/                # Uploaded documents
│   └── Fleeting/                    # Quick notes, voice memos, loose thoughts
│
├── 20 LLM Wiki (AI Maintained)/     # AGENT ZONE — agent writes, human reads
│   ├── _index.md                    # Master catalog of all wiki pages
│   ├── _log.md                      # Append-only activity log
│   ├── 21 Entities/                 # People, orgs, products, places
│   ├── 22 Concepts/                 # Ideas, frameworks, theories
│   └── 23 Sources/                  # One page per ingested source
│
├── 30 Zettelkasten (Human)/         # HUMAN ZONE — human writes, agent reads only
│
├── 35 Bridge/                       # SHARED ZONE — human writes, agent reads & links
│   ├── Evergreen/                   # Refined permanent notes ready for synthesis
│   ├── Queries/                     # Filed answers worth keeping (from either zone)
│   └── MOCs/                        # Maps of Content — curated entry points
│
├── 40 Projects & Output/            # Human zone — drafts and published work
│   ├── Drafts/
│   └── Published/
│
├── raw/                             # Legacy immutable source documents (agent reads only)
└── wiki/                            # Legacy agent wiki (still active; see root CLAUDE.md)
```

---

## Ownership Rules

| Zone | Folder | Owner | Other party |
|---|---|---|---|
| Agent zone | `20 LLM Wiki (AI Maintained)/` | Agent creates, edits, deletes freely | Human reads |
| Human zone | `30 Zettelkasten (Human)/` | Human writes and curates | Agent reads only — never modifies |
| Shared zone | `35 Bridge/` | Human writes and curates | Agent reads, cross-links, and can file query answers here |
| Staging | `10 Inbox & Raw/` | Human stages sources here | Agent reads during ingest |
| Output | `40 Projects & Output/` | Human writes | Agent reads only |
| Infrastructure | `00 Meta/` | Human manages | Agent reads for configuration |

**The key rule:** The agent never modifies anything in `30 Zettelkasten (Human)/`. It may read Zettelkasten notes to find connections and may suggest links in its wiki pages, but it does not touch those files.

---

## The Two-Zone Idea

**30 Zettelkasten** is where the human thinks. Notes here are written in the human's voice, developed over time, and represent the human's own synthesis. The agent supports but does not intrude.

**20 LLM Wiki** is where the agent compiles. Pages here are generated from ingested sources — summaries, entity pages, concept pages — maintained systematically across sessions.

**35 Bridge** is where the two zones meet. When a Zettelkasten note is ready to be connected to the wiki, it moves or links through the Bridge. When the agent files an answer that's worth keeping, it lands in `35 Bridge/Queries/`. Evergreen notes here are permanent notes refined enough to anchor connections in both directions.

---

## Session Start (updated for new structure)

At the start of every session, the agent reads:
1. Root `CLAUDE.md` — operational schema
2. `20 LLM Wiki (AI Maintained)/_index.md` — current wiki state
3. `20 LLM Wiki (AI Maintained)/_log.md` (last 5 entries) — recent activity
4. `wiki/overview.md` — current synthesis (legacy wiki, still active)

---

## Migration Note

The `wiki/` and `raw/` directories at the vault root are the legacy structure from the original flat setup. They remain active. New ingests should continue using the existing agent schema (root `CLAUDE.md`). The `20 LLM Wiki` structure is the intended long-term home; migration from `wiki/` to `20 LLM Wiki/` is a future task.
