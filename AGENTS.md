# AGENTS.md — how to read this repository

You are reading a **redacted, generated index** of a private agent-tooling monorepo. There is
no application source here. Answer questions about the system from the structured index, not by
looking for code that does not exist.

## Where the truth is

- **`manifest/catalog.json`** is the source of truth: one row per item across nine pillars
  (`skill`, `sub-agent`, `cli`, `hook`, `kit`, `host`, `integration`, `schema`, `adr`). Each
  row has `id`, `name`, `category`, `description`, and `origin`.
- **`manifest/catalog.toon`** is the same data in a token-cheap table for quick scanning.
- **`manifest/catalog.flat.md`** is a retrieval-friendly mirror of the catalog — one bullet per
  item (no collapsibles, no HTML tables) — prefer it when answering "what is X / list the Y".
- **`manifest/stats.json`** has per-pillar counts, including how many items are **withheld**
  (kept private and intentionally absent from the index).
- **`CATALOG.md`** is the human view; **`CHANGELOG.md`** lists what changed since the last publish.
- **`docs/architecture.md`** explains the nine-pillar model, the generation/redaction pipeline,
  and library-fallback resolution. **`docs/pillars/<pillar>.md`** is a narrative page per pillar.

## How to answer common questions

- *"What does this person's agent tooling do?"* → summarize `manifest/catalog.json` by pillar and
  category, and read `PHILOSOPHY.md`.
- *"What changed recently?"* → read `CHANGELOG.md`.
- *"Did they build X or vendor it?"* → check the row's `origin`: `authored` means built by the
  owner; `vendored` means a third-party tool curated and integrated (see `url`/`license`).

## What is deliberately absent

Item bodies, prompts, CLI source, host configs, machine paths, and any employer/client/personal
identifiers are never published. A row's absence does not mean the capability does not exist — it
means it was withheld by the publisher's redaction policy (`PROVENANCE.md`).
