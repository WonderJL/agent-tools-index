# Provenance & redaction policy

## How this repository is produced

`agent-tools-indexing` is **generated**, never hand-edited. A publisher in the private source
repository extracts an allowlisted set of metadata fields, sanitizes them, renders the catalog and
narrative, and runs a fail-closed leak scan over the entire output. A manually-triggered CI job
runs the publisher and, only after a human approval step, pushes the result here.

## What is published

- Item **names**, one-line **descriptions**, **counts**, **categories**, and an `authored` /
  `vendored` origin tag — per pillar (`skill`, `sub-agent`, `cli`, `hook`, `kit`, `host`,
  `integration`, `schema`, `adr`).
- Hand-written narrative: this file, `PHILOSOPHY.md`, `AGENTS.md`, and `docs/`.
- For vendored items: provenance (upstream source + license) and a link out — never the upstream
  description text re-hosted.

## What is never published

Item bodies, prompts, CLI source, host configuration, machine-specific paths, credentials, and any
employer / client / personal identifiers. Items that would expose these are **withheld** (counted
in `manifest/stats.json`, never named) unless they have been hand-reviewed and rewritten to a
generic, scrubbed form.

## Accuracy

Counts and descriptions reflect the private source at the commit named in `manifest/stats.json`.
The catalog is regenerated on each publish; `CHANGELOG.md` records what changed.
