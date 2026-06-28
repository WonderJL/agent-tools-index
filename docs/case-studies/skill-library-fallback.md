# Case study: a two-tier skill system that feels like one

**Problem.** An agent's system prompt has a token budget, but the useful skill set is large and
keeps growing. Loading every skill always is wasteful; loading too few makes the agent forget
capabilities exist.

**Design.** Skills live in two tiers:

- a small **live** set, auto-loaded into every session, covering the common path;
- a large **on-demand library**, not loaded until referenced.

A single resolution rule unifies them. When the user references a skill by name and it is not in
the live set, the agent must **load it from the library before declaring it missing** — never
answer "no such skill." A deterministic CLI fetches the archived definition and returns it for the
agent to follow inline.

**Why it works.** The always-on cost stays bounded by the live set, while the long tail remains one
hop away. The "library-first fallback" rule removes the failure mode where an agent refuses a real
capability just because it was not preloaded. The same pattern is reused for sub-agents and for
automation hooks.

**Trade-offs.** The library hop costs one tool round-trip and depends on the resolution rule being
stated firmly in the agent's instructions. In exchange, the system scales to a large catalog
without inflating every session.
