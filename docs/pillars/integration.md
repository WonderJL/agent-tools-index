# Integration pillar

The integration pillar is how the system absorbs anything it did not author itself. Each integration is a small package that takes a third-party tool — or a first-party bundle that needs uniform placement across hosts — and installs it deterministically, recording its upstream source and license so that authored work and vendored work always stay distinguishable. It is the seam between "we wrote this" and "we depend on this," and it is what keeps the system from quietly overclaiming.

Every integration is described by a single `integration.yaml` manifest (`apiVersion: agent-tools/v1`, `kind: Integration`) that is schema-validated against the [integration.yaml schema](../../CATALOG.md#schema). A manifest declares its identity and `upstream` (`repo`, `license`); pinned `sources` (a git `ref` pinned by tag, or a `local` path); a `files` block that maps each source into a host home with an explicit placement `strategy` (`symlink`, `mirror`, or `copy`); optional lifecycle `hooks` (e.g. `post_apply` to register a plugin); and `verify` checks that confirm the install actually took. The pillar splits into a small set of items across three families: first-party core packages that fan one source out to many hosts, vendored agent frameworks pinned to upstream tags, and migrated vendor packages. Notable examples include `agents-md-core`, which symlinks one canonical operating doctrine into every supported agent CLI; `jq`, installed via a Homebrew formula and verified by running `jq --version`; and `superpowers-framework`, which mirrors a tag-pinned upstream skill-and-command bundle into one host while deliberately excluding another that already gets it through its own plugin.

```mermaid
flowchart LR
    up["upstream source<br/>(pinned ref · license)"] --> mf["integration.yaml<br/>(schema-validated)"]
    mf --> pl["files → host homes<br/>symlink · mirror · copy"]
    pl --> vf{"verify"}
    vf -- "pass" --> ok["installed + recorded"]
```

**See also:** [Catalog](../../CATALOG.md#integration) · [Flat catalog](../../manifest/catalog.flat.md) · [Architecture](../architecture.md) · [Philosophy](../../PHILOSOPHY.md)
