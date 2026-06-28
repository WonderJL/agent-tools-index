# Case study: one source, many agent hosts

**Problem.** The same capabilities must work across several coding-agent hosts, each with its own
on-disk schema for skills, sub-agents, commands, and policy files. Maintaining a copy per host
drifts immediately.

**Design.** Each capability is authored **once** in a portable source format. A deterministic
renderer transforms the source into each host's native schema and links it into that host's home
directory. Generated outputs are treated as build artifacts: committed for reproducibility, but
never hand-edited — editing the source and re-rendering is the only supported path.

**Why it works.** Adding a host is writing one adapter, not re-authoring every capability. A single
edit to the source propagates everywhere on the next render. Because the rendered form is
reproducible from the source, drift is detectable: a hand-edit to a generated file shows up as a
diff that the next render would erase.

**Trade-offs.** Contributors must learn "edit the source, not the rendered output," and the
renderer becomes a critical, well-tested integration point. The payoff is genuine host-agnosticism:
the same skill behaves consistently whether invoked from one agent or another.
