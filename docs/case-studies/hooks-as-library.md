# Case study: automation hooks as a curated, dormant-by-default library

**Problem.** Lifecycle automation (format on edit, type-check at turn end, block writes to secret
files) is powerful but dangerous to enable globally: a surprise blocking hook can derail every
session on every machine.

**Design.** Hooks are a **curated library** of small, single-purpose intents, each with structured
metadata (event, matcher, tier) separate from its executable body. A deterministic CLI installs a
hook's intent and script into a target repository, stamps provenance, and gitignores a per-machine
opt-in marker. Installed hooks stay **dormant** until a teammate creates that marker locally, and
only one hook — the secret-write blocker — is allowed to actually block.

**Why it works.** The blast radius is controlled three ways: hooks are never hand-written into a
host's settings (a deterministic installer owns that), they do nothing until explicitly opted in
per machine, and all but one are non-blocking by contract. The metadata/body split means the public
index can describe a hook's intent without exposing its detection logic.

**Trade-offs.** The opt-in marker is one extra step before automation runs, and the "only one
blocking hook" rule must be enforced, not assumed. In return, shared automation is safe to commit:
it cannot ambush a machine that has not opted in.
