# Philosophy — best practices behind this system

This is a personal, multi-machine, multi-agent tooling system: one private repository, linked
into every coding agent's home, kept in sync across machines by git. A few principles shape it.

## 1. One source of truth, deterministic renderers

Anything consumed by more than one tool is authored once and *rendered* into each tool's native
format by a deterministic script — never hand-maintained per tool. Generated outputs are treated
as build artifacts: never edited by hand, always reproducible. This very repository is an example
— it is a rendered projection of the private source, regenerated rather than edited.

## 2. Allowlist, not denylist, at trust boundaries

When data crosses a boundary (especially private → public), the safe design extracts only an
explicit set of fields rather than copying everything and trying to strip secrets. A copy-then-
strip pipeline eventually leaks; an extract-only pipeline structurally cannot emit what it never
reads. A fail-closed scan over the final output is kept as a second wall, not the first.

## 3. On-demand libraries beat always-loaded context

Most capabilities live in on-demand libraries and load only when referenced, keeping the always-on
context small. A small live set covers the common path; a large library covers the long tail. A
resolution rule ("if it's not live, load it from the library before declaring it missing") makes
the two tiers feel like one to the agent.

## 4. Capabilities are curated libraries with provenance

Skills, sub-agents, and automation hooks are versioned, attributed, and installed deterministically
— including third-party tools, which are vendored with their license and upstream source recorded.
Authored work and vendored work are always distinguishable, so the system never overclaims.

## 5. Host-agnostic core, thin per-host adapters

The portable intent lives in the core; each host gets a minimal adapter. Adding a new agent host
means writing one adapter, not re-authoring the capabilities.

## 6. Decisions are written down

Non-obvious architectural choices are captured as short decision records. The index surfaces their
titles and status so the *shape* of the system's evolution is legible without exposing internals.

## 7. Ship behind fail-closed gates

Outward-facing or hard-to-reverse actions run behind gates that fail closed and, where it matters,
require a human to approve before the irreversible step. Verification is adversarial: assume the
naive path leaks or breaks, and prove otherwise before proceeding.
