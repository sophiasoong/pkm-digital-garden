# Activity Log

Append-only. Each entry: `## [YYYY-MM-DD] <type> | <title>`
Types: `ingest`, `query`, `lint`, `update`, `note`

---

## [2026-07-07] ingest | LLM Wiki (Karpathy's original gist)
- Source: [[sources/karpathy-llm-wiki-gist-2026]]
- New pages: [[sources/karpathy-llm-wiki-gist-2026]]
- Updated pages: [[concepts/llm-wiki]], [[concepts/idea-file]], [[concepts/rag-retrieval]], [[concepts/memex]], [[entities/andrej-karpathy]], [[overview]], [[index]]
- Notes: Primary source now ingested. Key additions vs. the secondary source: (1) Karpathy's precise human/LLM division of labor quote; (2) explicit modularity — "everything is optional"; (3) the gist is itself an idea file, stated in the first line; (4) the Memex reference in the gist is brief (one paragraph) — the extended historical lineage in the Antigravity article was that source's own addition. All concept pages updated to list the primary source first.

---

## [2026-05-02] ingest | Karpathy's LLM Wiki: The Complete Guide to His Idea File
- Source: [[sources/antigravity-karpathy-llm-wiki-2026]]
- New pages: [[concepts/llm-wiki]], [[concepts/idea-file]], [[concepts/rag-retrieval]], [[concepts/memex]], [[entities/andrej-karpathy]], [[entities/vannevar-bush]]
- Updated pages: [[overview]], [[index]]
- Notes: First ingest. This is a secondary source (Antigravity.codes analyzing Karpathy's gist, not the gist itself). Central concept is the wiki-beats-RAG argument and the compounding-knowledge property. Notable secondary contribution: the "idea file" as a new format for sharing patterns in the LLM agent era. Historical thread (Memex → hypertext → web → LLM Wiki) is strong and well-sourced. Karpathy's original gist not yet ingested directly — flagged as a priority for next session.

---

## [2026-04-18] note | Wiki initialized
- Schema written to `CLAUDE.md`.
- Directory structure created: `wiki/sources/`, `wiki/entities/`, `wiki/concepts/`, `wiki/queries/`, `raw/assets/`.
- `index.md`, `log.md`, and `overview.md` initialized.
- Sources: 0 | Pages: 1
