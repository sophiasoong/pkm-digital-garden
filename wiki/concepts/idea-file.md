---
type: concept
name: "Idea File"
tags: [knowledge-sharing, llm-agents, open-source, karpathy]
sources: [karpathy-llm-wiki-gist-2026, antigravity-karpathy-llm-wiki-2026]
---

## Definition

An idea file is a structured markdown document that describes a pattern, architecture, or workflow at a conceptual level — designed to be interpreted and instantiated by an LLM agent rather than executed directly as code. The format was introduced by Andrej Karpathy alongside his LLM Wiki gist (April 2026).

From the gist's opening line: "This is an idea file, it is designed to be copy pasted to your own LLM Agent (e.g. OpenAI Codex, Claude Code, OpenCode / Pi, or etc.). Its goal is to communicate the high level idea, but your agent will build out the specifics in collaboration with you."

From the secondary analysis, Karpathy's framing: "The idea of the idea file is that in this era of LLM agents, there is less of a point/need of sharing the specific code/app, you just share the idea, then the other person's agent customizes & builds it for your specific needs."

## How It Appears in This Wiki

The primary source ([[sources/karpathy-llm-wiki-gist-2026]]) is itself an idea file — the concept is both defined and demonstrated by the same document. Discussed further in [[sources/antigravity-karpathy-llm-wiki-2026]], which contextualizes it as a new open-source format for the LLM era.

## Key Sources

- [[sources/karpathy-llm-wiki-gist-2026]] — Primary source; this gist is itself an instance of the idea file format.
- [[sources/antigravity-karpathy-llm-wiki-2026]] — Secondary analysis contextualizing the format and its implications.

## Why This Differs from Code Sharing

Traditional open source shares *implementation*: a GitHub repo, an npm package, a Docker image. Recipients clone, configure, and run it. In the LLM agent era, sharing the *idea* is often more useful because:

- Code is implementation-specific (tied to OS, tools, preferences, environment)
- An idea file is portable — paste it to any LLM agent, and the agent builds a version customized to the user's setup
- The schema is intentionally "a little bit abstract/vague" so the agent fills in the specifics

Karpathy frames this as **open ideas** rather than open source. The gist's Discussion tab allows people to "adjust the idea or contribute their own" — a new kind of collaborative idea space.

## Community Extension

The gist's Discussion tab surfaced several extensions of the idea file concept:
- A `.brain` folder pattern for project-level persistent memory across AI sessions
- Using GitHub gists as agent-to-agent communication channels (not just human-to-agent)
- Connection to Karpathy's earlier "append-and-review note" concept as a precursor

## Related Concepts

- [[concepts/llm-wiki]] — The specific pattern introduced via idea file in Karpathy's gist.

## Open Questions

- Could the idea file format evolve into a standard schema with versioning and a registry?
- What is the right level of abstraction — too vague loses the pattern, too specific loses portability?
- How does this interact with `CLAUDE.md` / `AGENTS.md` conventions as those become standardized across LLM agents?
