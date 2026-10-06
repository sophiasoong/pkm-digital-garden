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
├── 10 Inbox & Raw/                  # Staging queue AND permanent raw archive
│   ├── Web Clips/                   # Clipped articles (markdown from Web Clipper)
│   ├── Book Quotes/                 # Transcribed passages from books
│   └── Fleeting Notes/              # The human's own quick notes and loose thoughts
│
├── 20 LLM Wiki (AI Maintained)/     # AGENT ZONE — agent writes, human reads
│   ├── _overview.md                 # Cross-source synthesis — the most important page
│   ├── _index.md                    # Master catalog of all wiki pages
│   ├── _log.md                      # Append-only activity log
│   ├── 21 Entities/                 # People, orgs, products, places
│   ├── 22 Concepts/                 # Ideas, frameworks, theories
│   └── 23 Sources/                  # One page per ingested source
│
├── 30 Zettelkasten (Human)/         # HUMAN ZONE — human writes, agent reads only
│
├── 35 Bridge/                       # SHARED ZONE — human writes; agent links & files queries
│   ├── Queries/                     # Filed answers and lint reports worth keeping
│   ├── Evergreen/                   # (not yet created) Permanent notes promoted for agent linking
│   └── MOCs/                        # (not yet created) Maps of Content — curated entry points
│
└── 40 Projects & Output/            # Working output — reference notes, drafts, published work
    └── Design/                      # Design-system reference notes
        ├── Layout/
        ├── Visual Design/
        └── Motion Design/
```

---

## Ownership Rules

| Zone | Folder | Owner | Other party |
|---|---|---|---|
| Agent zone | `20 LLM Wiki (AI Maintained)/` | Agent creates, edits, deletes freely | Human reads |
| Human zone | `30 Zettelkasten (Human)/` | Human writes and curates | Agent reads only — never modifies |
| Shared zone | `35 Bridge/` | Human writes and curates | Agent reads, cross-links, and can file query answers here |
| Staging | `10 Inbox & Raw/` | Human stages sources here | Agent reads during ingest; maintains `status:` and `wiki_source:` frontmatter. Never edits note bodies or deletes files |
| Output | `40 Projects & Output/` | Human owns and curates | Agent may create and edit notes here when asked. Never deletes |
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
4. `20 LLM Wiki (AI Maintained)/_overview.md` — the current cross-source synthesis
5. `35 Bridge/Queries/` — filed query answers and lint reports

**Resolved 2026-10-06:** root `CLAUDE.md` specifies an `overview.md` as the wiki's most
important page. It existed in the legacy `wiki/` directory, was not carried over in the
2026-10-01 migration, and has been rebuilt from the 11 sources on disk as
`20 LLM Wiki (AI Maintained)/_overview.md` — underscore-prefixed to match `_index.md`
and `_log.md`. It is maintained at the end of every ingest, per the root schema.

---

## Migration Note

Migration is **complete** as of 2026-10-01. The legacy flat `wiki/` and `raw/` directories
at the vault root have been deleted; `20 LLM Wiki (AI Maintained)/` and `10 Inbox & Raw/`
are now the only homes for wiki pages and staged sources respectively. Page formats, slug
conventions, and the ingest/query/lint workflows still come from root `CLAUDE.md` — only
the paths changed. One item did not survive the move and was rebuilt on 2026-10-06: see Session Start.
