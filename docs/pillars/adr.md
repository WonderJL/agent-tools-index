# ADR pillar

The ADR pillar is where the system's non-obvious choices get written down. It collects the architecture decision records and design specs that explain *why* the rest of the catalog looks the way it does — the integration model, the rendering boundary, the gating policy — so the shape of the system's evolution stays legible even though its internals are redacted. This is the pillar that makes [Philosophy principle 6](../../PHILOSOPHY.md) ("decisions are written down") concrete: the index surfaces each record's title and status without exposing the work it governs.

Records follow a light, consistent convention. Each opens with a one-line **Summary** and a **Status** field, then walks through **Context → Decision → Consequences** (specs add **Problem / Goals / Non-Goals**). The status vocabulary is what makes the timeline readable from outside — entries are marked **Proposed**, **Approved**, or **accepted**, so a reader can tell a settled foundation apart from a direction still in flight. Of the 53 records, all are authored (none vendored), split into 46 dated design **specs** and a smaller spine of numbered **ADRs** covering foundational architecture, repo-agentic setup, CLI design, and multi-agent orchestration. The load-bearing examples are `ADR-0001: Integration Architecture` (the manifest-driven, receipt-tracked package model the whole repo rests on), `ADR-0002` (deciding that repo-agentic setup is committed into each target repo with a portable source-of-truth folder), and `ADR-0004` (splitting an LLM "recommender" skill from a deterministic render CLI). Specs like `local-first-pr-review-index-design` and the `cli-ai-usage` design show the same discipline applied to individual tools before they were built.

```mermaid
flowchart LR
    P["Proposed"] --> A["Approved / accepted"]
    A --> B["Built capability<br/>(other pillars)"]
```

**See also:** [Catalog](../../CATALOG.md#adr) · [Flat catalog](../../manifest/catalog.flat.md) · [Architecture](../architecture.md) · [Philosophy](../../PHILOSOPHY.md)
