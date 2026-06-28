<p align="center">
  <a href="https://deepwiki.com/WonderJL/agent-tools-indexing"><img src="https://img.shields.io/badge/DeepWiki-Ask%20this%20repo-7c3aed?style=for-the-badge" alt="DeepWiki"></a>
  <a href="https://context7.com/WonderJL/agent-tools-indexing"><img src="https://img.shields.io/badge/Context7-Indexed-0ea5e9?style=for-the-badge" alt="Context7"></a>
</p>

<p align="center">
  <a href="https://github.com/WonderJL">Website</a> · <a href="CATALOG.md">Catalog</a> · <a href="AGENTS.md">AI agents</a> · <a href="https://context7.com/WonderJL/agent-tools-indexing">Context7</a> · <a href="https://deepwiki.com/WonderJL/agent-tools-indexing">DeepWiki</a> · <a href="PHILOSOPHY.md">Philosophy</a>
</p>

# agent-tools-indexing

A public, **redacted index** of a private agent-tooling monorepo — a machine-agnostic,
agent-agnostic system of reusable skills, sub-agents, CLIs, hooks, host integrations, and
architecture decisions used across Claude Code, Codex, Cursor, Gemini, OpenCode, and more.

This repository is **generated** from the private source by a re-runnable publisher and a
manually-triggered CI. It contains only metadata (names, one-line descriptions, counts,
categories) plus hand-written narrative — never source, prompts, configs, or secrets.

- **`CATALOG.md`** — the human catalog: headline counts, highlights, and full tables of
  publishable items, with a separate link-out section for vendored (curated) tools.
- **`manifest/catalog.json`** / **`catalog.toon`** — the machine index (the agent-readable core).
- **`PHILOSOPHY.md`** — the engineering principles behind the system.
- **`docs/`** — architecture summaries and flagship case studies.

Items are tagged **authored** (built by the owner) vs **vendored** (third-party tools curated
and integrated, with provenance + license). See `PROVENANCE.md` for how this repo is produced.
