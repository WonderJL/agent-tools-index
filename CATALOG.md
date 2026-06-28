# Catalog

_Generated — do not edit by hand._

## Headline
- **skill**: 179 published (146 authored)
- **sub-agent**: 64 published (8 authored)
- **cli**: 49 published (49 authored)
- **hook**: 4 published (4 authored)
- **kit**: 7 published (7 authored)
- **host**: 14 published (14 authored)
- **integration**: 10 published (10 authored)
- **schema**: 6 published (6 authored)
- **adr**: 52 published (52 authored)

## Highlights
| id | name | description |
|---|---|---|
| `deep-research` | deep-research | Generate domain- and topic-specific deep-research prompt markdown files. Uses token-efficient lite template. Use when user wants a structured research prompt for architecture, strategy, policy, AI systems, security, economics, or any complex domain. Prompt is saved to output directory for copy/paste into an LLM. If result > 4900 chars, offers a trimmed version. |
| `diagnose` | diagnose | Disciplined diagnosis loop for hard bugs and performance regressions. Reproduce → minimise → hypothesise → instrument → fix → regression-test. Use when user says "diagnose this" / "debug this", reports a bug, says something is broken/throwing/failing, or describes a performance regression. |
| `no-mistakes` | no-mistakes | Ship-gate host: review, test, lint, docs, PR, CI. |
| `plan-master` | plan-master | Transform user task descriptions into comprehensive engineering plans following a structured PLAN-<slug>.md format. Use when user wants to create a detailed engineering plan from a task description, needs to break down complex tasks into actionable steps, or requires a production-grade plan document. |
| `plan-master` | plan-master | Engineering planning agent. Creates structured PLAN-<slug>.md implementation plans using the plan-master skill. Always runs on Opus to guarantee maximum planning quality and codebase reasoning. |
| `repo-agentic-setup` | repo-agentic-setup | Use to set up a target repo for agentic development (the four pillars - skills, sub-agents, slash-commands, hooks - plus model routing), or to update/migrate an already-configured repo to the latest kits. Detects the stack, composes kits, diagnoses gaps, prescribes library + bespoke artifacts, populates .agents/ and the root AGENTS.md, then shells out to cli-repo-agentic-sync to dry-run and render to all hosts. Triggered by /repo-agentic-setup. |
| `skill-library` | skill-library | Resolves `skill@<name>` references that are not in the active session: loads the archived skill from the on-demand library and follows it inline. The dynamic skill-loading backbone. |
| `sub-agent-library` | sub-agent-library | MANDATORY when the user writes `subagent@<name>` for any name that is not in the active sub-agent list. Resolves the host-appropriate flavor (cc on Claude Code, oc on OpenCode/Codex), runs `cli-sub-agent-library load <name>@<flavor>`, and dispatches the persona via the host's native sub-agent mechanism (or inline fallback). |

## Authored
### adr · CLI tool design
| id | name | description |
|---|---|---|
| `ADR-0004-recommender-skill-render-cli-split` | ADR-0004: Recommender (LLM skill) and Render (deterministic CLI) are split | ADR-0004: Recommender (LLM skill) and Render (deterministic CLI) are split |

### adr · foundational / architecture
| id | name | description |
|---|---|---|
| `ADR-0001-integration-architecture` | ADR-0001: Integration Architecture for `agent-tools` | ADR-0001: Integration Architecture for `agent-tools` |
| `ADR-0003-canonical-intent-per-host-adapter` | ADR-0003: Canonical intent + per-host adapters for format-divergent concerns | ADR-0003: Canonical intent + per-host adapters for format-divergent concerns |
| `ADR-0005-observability-debug-layer` | ADR-0005: Observability and debug via harness-transcript review, not a logging hook | ADR-0005: Observability and debug via harness-transcript review, not a logging hook |

### adr · multi-agent orchestration
| id | name | description |
|---|---|---|
| `ADR-0006-ai-crew-session-bus` | ADR-0006: ai-crew — a harness-agnostic agent session bus | ADR-0006: ai-crew — a harness-agnostic agent session bus |

### adr · repo-agentic setup
| id | name | description |
|---|---|---|
| `ADR-0002-repo-agentic-setup-storage-model` | ADR-0002: Repo agentic-setup writes into the target repo, with `.agents/` as a localized source of truth | ADR-0002: Repo agentic-setup writes into the target repo, with `.agents/` as a localized source of truth |
| `ADR-0007-monorepo-composition` | ADR-0007: Monorepo composition, precedence, routing merge, and hook path-scoping | ADR-0007: Monorepo composition, precedence, routing merge, and hook path-scoping |

### adr · spec
| id | name | description |
|---|---|---|
| `2026-05-04-zsh-alias-loader-design` | Zsh alias loader — design | Zsh alias loader — design |
| `2026-05-09-cli-anything-agent-first-help-design` | CLI-Anything Agent-First Help & Version Contract — Design | CLI-Anything Agent-First Help & Version Contract — Design |
| `2026-05-11-cli-ai-usage-design` | `cli-ai-usage` — Design Spec | `cli-ai-usage` — Design Spec |
| `2026-05-12-cli-ai-usage-login-import-design` | `cli-ai-usage` Login + Import Subcommands — Design Spec | `cli-ai-usage` Login + Import Subcommands — Design Spec |
| `2026-05-16-cli-proxy-wrapper-design` | cli-proxy-wrapper — design | cli-proxy-wrapper — design |
| `2026-05-17-cli-takeover-design` | cli-takeover — Cross-app session takeover | cli-takeover — Cross-app session takeover |
| `2026-05-18-opencode-claude-delegate-provider-design` | OpenCode Claude Delegate Provider Design | OpenCode Claude Delegate Provider Design |
| `2026-05-20-cf-page-manager-design` | cf-page-manager — Design | cf-page-manager — Design |
| `2026-05-20-opencode-superpowers-slash-discoverability-design` | 2026-05-20-opencode-superpowers-slash-discoverability-design | 2026-05-20-opencode-superpowers-slash-discoverability-design |
| `2026-05-21-add-omo-to-ai-heavy-design` | Add Oh My OpenAgent to ai-heavy | Add Oh My OpenAgent to ai-heavy |
| `2026-05-21-agent-onboarding-doctrine-design` | Agent Onboarding Doctrine Design | Agent Onboarding Doctrine Design |
| `2026-05-21-claude-opencode-bridge-reliability-design` | Claude OpenCode Bridge Reliability Design | Claude OpenCode Bridge Reliability Design |
| `2026-05-21-claude-opencode-interactive-bridge-design` | Claude OpenCode Interactive Bridge Design | Claude OpenCode Interactive Bridge Design |
| `2026-05-21-local-first-pr-review-index-design` | 2026-05-21-local-first-pr-review-index-design | 2026-05-21-local-first-pr-review-index-design |
| `2026-05-21-oh-my-openagent-integration-design` | Oh My OpenAgent Integration Design | Oh My OpenAgent Integration Design |
| `2026-05-21-sync-all-apply-ai-heavy-design` | sync-all Applies ai-heavy Integrations | sync-all Applies ai-heavy Integrations |
| `2026-05-23-cli-takeover-browse-design` | cli-takeover browse design | cli-takeover browse design |
| `2026-05-23-macos-app-proxy-wrapper-design` | cli-proxy-wrapper: macos-app subcommand — design | cli-proxy-wrapper: macos-app subcommand — design |
| `2026-05-23-omo-opt-out-and-uninstall-design` | OMO Opt-Out From sync-all and Manual Uninstall Design | OMO Opt-Out From sync-all and Manual Uninstall Design |
| `2026-05-29-setup-sh-decomposition-design` | setup.sh decomposition into characterization-tested `lib/` modules | setup.sh decomposition into characterization-tested `lib/` modules |
| `2026-05-31-proxy-cli-codex-cursor-design` | Design: proxy support in cli-codex and cli-cursor-agent | Design: proxy support in cli-codex and cli-cursor-agent |
| `2026-06-04-claude-interactive-delegate-prd` | Claude Interactive Delegate PRD | Claude Interactive Delegate PRD |
| `2026-06-11-notebooklm-watermark-remover-cli-design` | Design — `cli-notebooklm-watermark-remover` | Design — `cli-notebooklm-watermark-remover` |
| `2026-06-12-notebooklm-watermark-removal-skill-integration` | Design — Integrate `cli-notebooklm-watermark-remover` into the NotebookLM infographic flow | Design — Integrate `cli-notebooklm-watermark-remover` into the NotebookLM infographic flow |
| `2026-06-17-markitdown-ocr-llm-design` | MarkItDown OCR LLM Design | MarkItDown OCR LLM Design |
| `2026-06-18-ai-repo-eval-integration-design` | AI repo-eval integration design | AI repo-eval integration design |
| `2026-06-22-cli-notebooklm-style-wrapper-design` | cli-notebooklm Style Wrapper Design | cli-notebooklm Style Wrapper Design |
| `2026-06-23-axi-toon-fleet-migration-design` | AXI/TOON Fleet Migration — Design | AXI/TOON Fleet Migration — Design |
| `2026-06-23-power-machine-sync-tier-design` | Power-machine sync tier — design | Power-machine sync tier — design |
| `2026-06-24-agents-claude-symlink-consolidation-design` | Design — `.agents` source of truth, `.claude` → symlink | Design — `.agents` source of truth, `.claude` → symlink |
| `2026-06-24-chrome-devtools-axi-adoption-design` | chrome-devtools-axi Adoption — Design | chrome-devtools-axi Adoption — Design |
| `2026-06-24-self-host-html-render-design` | Self-host the HTML-review render — kill runtime npx | Self-host the HTML-review render — kill runtime npx |
| `2026-06-24-workspace-manager-design` | Workspace Manager — design | Workspace Manager — design |
| `2026-06-25-ai-crew-hardening-design` | ai-crew hardening round — design spec | ai-crew hardening round — design spec |
| `2026-06-25-ai-crew-multi-mode-design` | ai-crew multi-mode — `run` (one-shot exec) + Codex bus auto-completion | ai-crew multi-mode — `run` (one-shot exec) + Codex bus auto-completion |
| `2026-06-25-repo-agentic-routing-resolution-design` | Step 6 - Routing resolution + mechanical-tier offload (design) | Step 6 - Routing resolution + mechanical-tier offload (design) |
| `2026-06-25-repo-agentic-step4-overlays-design` | Repo Agentic-Setup - Step 4: `cli` + `data-ml` role overlays | Repo Agentic-Setup - Step 4: `cli` + `data-ml` role overlays |
| `2026-06-26-ai-crew-spawn-supervisor-design` | ai-crew spawn supervisor — design spec | ai-crew spawn supervisor — design spec |
| `2026-06-26-ai-git-auto-crew-escalation-ladder-design` | ai-git-auto crew escalation ladder — design | ai-git-auto crew escalation ladder — design |
| `2026-06-26-cli-full-vpn-wrapper-design` | cli-full-vpn-wrapper — design | cli-full-vpn-wrapper — design |
| `2026-06-26-cli-full-vpn-wrapper-doctor-design` | cli-full-vpn-wrapper `doctor` — connectivity probe design | cli-full-vpn-wrapper `doctor` — connectivity probe design |
| `2026-06-26-git-smart-multi-account-clone-design` | Design — `cli-git-smart` + `git-clone-smart` | Design — `cli-git-smart` + `git-clone-smart` |
| `2026-06-27-cli-full-vpn-wrapper-reset-interactive-design` | cli-full-vpn-wrapper `reset` + interactive profile selection — design | cli-full-vpn-wrapper `reset` + interactive profile selection — design |
| `2026-06-28-agent-tools-indexing-public-projection-design` | agent-tools-indexing — public projection of the private agent-tools monorepo | agent-tools-indexing — public projection of the private agent-tools monorepo |
| `2026-06-28-vendor-worktree-manager-and-strip-telemetry-design` | Truly-vendor a worktree manager from source and strip its analytics telemetry | Truly-vendor a worktree manager from source and strip its analytics telemetry |

### cli · ai / agent orchestration
| id | name | description |
|---|---|---|
| `agent-delegate` | cli-agent-delegate | CLI + MCP bridge for delegating OpenCode tasks to agent |
| `agent-parallel-manager` | cli-agent-parallel-manager | CLI-Anything harness for local parallel agent coordination |
| `ai-crew` | cli-ai-crew |  |
| `ai-git-auto` | cli-ai-git-auto | Non-interactive AI git automation (commit/merge/push) on top of cli-codex |
| `ai-html-chat` | cli-ai-html-chat | Open an agent-authored HTML artifact in a local browser for a human to review and annotate, then poll the annotations and layout warnings back — a human-in-the-loop review loop for HTML pages, reports, and mockups. |
| `ai-usage` | cli-ai-usage | Cron-safe AI provider usage tracker for Codex, Claude, Cursor, Gemini |
| `claude-opencode-bridge` | cli-claude-opencode-bridge | Local OpenAI-compatible bridge from OpenCode to Claude CLI |
| `cli-slack` | cli-slack | CLI-Anything harness for Slack (multi-workspace OAuth) |
| `cmux-manage` | cli-cmux-manage | CLI-Anything harness for OpenCode cmux notification plugin lifecycle |
| `codex` | cli-codex | CLI-Anything one-shot delegator to the codex exec binary |
| `cursor-agent` | cli-cursor-agent | CLI-Anything one-shot delegator to the Cursor `agent` binary (model pinned to auto) |
| `opencode-manager` | cli-opencode-manager | Umbrella CLI for OpenCode OpenAI, plugin, and session workflows |
| `skill-delegate` | cli-skill-delegate | Delegate prompts to agent-tools skills through cli-agent-delegate |
| `workspace-manager` | cli-workspace-manager | Orchestrate a crew of AI coding agents: a single point of contact that spawns, supervises, and tears down worker agents across projects via a workspace CLI — never doing the work itself. |

### cli · ci / devops
| id | name | description |
|---|---|---|
| `cli-staging-logs` | cli-staging-logs | CLI-Anything harness for staging log lookup by request id. |

### cli · data / extraction
| id | name | description |
|---|---|---|
| `cli-receipt-parser` | cli-receipt-parser | Install wrapper for a native Swift CLI that extracts structured fields from scanned receipts. |

### cli · data / scraping
| id | name | description |
|---|---|---|
| `cli-image-crawler` | cli-image-crawler | CLI-Anything harness for crawling product color-option images from an e-commerce site. |
| `cli-inventory-manager` | cli-inventory-manager | CLI-Anything harness for an inventory session with filters. |

### cli · diagram / media / render
| id | name | description |
|---|---|---|
| `chrome-devtools-axi` | cli-chrome-devtools-axi | Chrome DevTools driver host pin. |
| `excalidraw` | cli-excalidraw | CLI-Anything harness for rendering Excalidraw diagrams to PNG and SVG |
| `figma` | cli-figma | CLI-Anything harness for Figma |
| `macdown` | cli-macdown | CLI-Anything harness for MacDown window control |
| `mermaid-agent` | cli-mermaid-agent | Validate, repair, render, and lint AI-generated Mermaid diagrams via a wrapped mmdc. |
| `stitch` | cli-stitch | Pure CLI for Google Stitch over direct MCP HTTP |
| `typora` | cli-typora | CLI-Anything harness for Typora window control |

### cli · doc / OCR / conversion
| id | name | description |
|---|---|---|
| `markitdown-ocr-llm` | cli-markitdown-ocr-llm | Provider-aware MarkItDown OCR helper |
| `notebooklm` | cli-notebooklm | Agent-first NotebookLM prompt-style wrapper |
| `notebooklm-watermark-remover` | cli-notebooklm-watermark-remover | CLI-Anything wrapper that removes the NotebookLM watermark via Albonire/notebooklm-watermark-remover. |
| `safe-extract` | cli-safe-extract | Two-phase, default-deny safe archive extraction (inspect → manifest → promote) |

### cli · git / dev workflow
| id | name | description |
|---|---|---|
| `cli-worktree-manager` | cli-worktree-manager | Terminal CLI for managing isolated git worktrees: create, list, switch between, and tear down working trees (vendored from source, third-party telemetry stripped). |
| `git-smart` | cli-git-smart | Smart multi-account git clone: rewrite SSH host to per-account ssh-config alias |
| `gnhf` | cli-gnhf | Git helper utility CLI. |
| `local-pr-review` | cli-local-pr-review | Local-first PR review orchestration with GitNexus indexes |
| `takeover` | cli-takeover | Cross-app session takeover CLI (CLI-Anything) |

### cli · network / vpn
| id | name | description |
|---|---|---|
| `full-vpn-wrapper` | cli-full-vpn-wrapper | CLI-Anything wrapper that runs agent CLIs through a dedicated local VPN/proxy relay (TLS relay plus multiple transport protocols). |

### cli · productivity
| id | name | description |
|---|---|---|
| `cli-work-ledger` | cli-work-ledger | CLI-Anything harness for recording and finalizing per-session work receipts to a shared ledger. |

### cli · productivity / SaaS
| id | name | description |
|---|---|---|
| `cf-page-manager` | cli-cf-page-manager | CLI-Anything harness for Cloudflare Pages |
| `context7` | cli-context7 | CLI-Anything harness for Context7 |
| `linear` | cli-linear | CLI-Anything harness for Linear |
| `obsidian` | cli-obsidian | CLI-Anything harness for Obsidian vault operations |
| `reminders` | cli-reminders | CLI-Anything harness for Apple Reminders operations |

### cli · skill / agent infra
| id | name | description |
|---|---|---|
| `_shared` | cli-_shared | Shared Click primitives for cli-anything-agent-tools CLIs. |
| `aliases` | cli-aliases | CLI-Anything central shell-alias manager for the toolkit: register, list, and sync command shortcuts. |
| `cli-agent-tools-library` | cli-agent-tools-library | Unified search across the sub-agent and skill libraries via subprocess delegation. |
| `cli-hooks-library` | cli-hooks-library | Browse and install curated git/agent hooks from the hooks library into a target repo, with provenance stamping and a per-machine opt-in. |
| `cli-repo-agentic-debug` | cli-repo-agentic-debug | Review what a repo-agentic setup did, from the harness session log |
| `cli-repo-agentic-sync` | cli-repo-agentic-sync | Deterministic renderer: project .agents/ into per-host views (repo-agentic-setup) |
| `cli-skill-library` | cli-skill-library | Browse and load on-demand skills from the skill library — the fallback that resolves skill references not present in the active session. |
| `cli-sub-agent-library` | cli-sub-agent-library | Browse and load on-demand sub-agent personas from the sub-agent library, dispatching the archived persona when not live. |

### hook · build check
| id | name | description |
|---|---|---|
| `build-check-on-stop` | build-check-on-stop | Run cargo check / go vet + go build at turn end if configured; report errors, never block. |

### hook · format / lint
| id | name | description |
|---|---|---|
| `format-on-edit` | format-on-edit | Format the changed file with the project's configured formatter (prettier/ruff/gofmt/rustfmt); no-op if none is installed. |

### hook · secrets (blocking)
| id | name | description |
|---|---|---|
| `block-secrets` | block-secrets | Block writes to .env / secret-bearing files or content; the only blocking hook. |

### hook · typecheck
| id | name | description |
|---|---|---|
| `typecheck-on-stop` | typecheck-on-stop | Run tsc --noEmit / mypy (or pyright) at turn end if configured; report type errors, never block. |

### host · agent CLI drivers
| id | name | description |
|---|---|---|
| `claude` | claude | Claude Code |
| `codex` | codex | Codex |
| `cursor` | cursor | Cursor |
| `gemini` | gemini | Gemini CLI / Antigravity |
| `opencode` | opencode | OpenCode |
| `shell` | shell | Shell (PATH-level binaries and shared helpers) |

### host · cross-cutting (routing / gate)
| id | name | description |
|---|---|---|
| `global` | global | Cross-cutting global routing host. |
| `no-mistakes` | no-mistakes | Ship-gate host: review, test, lint, docs, PR, CI. |

### host · host
| id | name | description |
|---|---|---|
| `agent-multiplexer` | agent-multiplexer | Terminal-based AI-agent multiplexer host. |
| `worktree-manager` | worktree-manager | Git-worktree manager integrated as a host (vendored from source, telemetry stripped). |

### host · integration / tool pin
| id | name | description |
|---|---|---|
| `ai-crew` | ai-crew |  |
| `chrome-devtools-axi` | chrome-devtools-axi | Chrome DevTools driver host pin. |
| `openclaw` | openclaw | OpenClaw |
| `rtk` | rtk |  |

### integration · agent frameworks (vendored)
| id | name | description |
|---|---|---|
| `oh-my-openagent` | oh-my-openagent | Oh My OpenAgent / oh-my-opencode managed OpenCode integration |
| `superpowers-framework` | superpowers-framework | Superpowers skill + command bundle for OpenCode |

### integration · first-party core
| id | name | description |
|---|---|---|
| `agents-md-core` | agents-md-core | First-party AGENTS.md placement across host homes |
| `commands-core` | commands-core | First-party commands tree fanned out to command-aware host homes |
| `jq` | jq | jq — command-line JSON processor |
| `skills-core` | skills-core | First-party skills tree fanned out to skill-aware host homes |
| `sub-agents-core` | sub-agents-core | First-party sub-agents fanned out per host (Claude uses rendered tree) |

### integration · migrated vendor packages
| id | name | description |
|---|---|---|
| `vendor-agent-agency-agents` | vendor-agent-agency-agents | Migrated from legacy vendor: agent/agency-agents |
| `vendor-cli-notebooklm-py` | vendor-cli-notebooklm-py | Migrated from legacy vendor: cli/notebooklm-py |
| `vendor-skill-cli-anything` | vendor-skill-cli-anything | Migrated from legacy vendor: skill/cli-anything |

### kit · base
| id | name | description |
|---|---|---|
| `go` | Go (backend) | Go (backend) |
| `node-typescript` | Node / TypeScript (backend) | Node / TypeScript (backend) |
| `python` | Python (backend) | Python (backend) |
| `rust` | Rust (backend) | Rust (backend) |

### kit · overlay
| id | name | description |
|---|---|---|
| `cli` | CLI tool | CLI tool |
| `data-ml` | Data / ML | Data / ML |
| `frontend-react-nextjs` | Frontend — React / Next.js | Frontend — React / Next.js |

### schema · schema
| id | name | description |
|---|---|---|
| `agent-tools-catalog.schema.json` | agent-tools-indexing catalog |  |
| `integration.schema.json` | integration.yaml | Manifest schema for an agent-tools integration package. Normative per ADR-0001. |
| `work-ledger/export-review.schema.json` | Work Ledger Export Review Decision |  |
| `work-ledger/public-export.schema.json` | Work Ledger Public Export |  |
| `work-ledger/session-receipt.schema.json` | Work Ledger Session Receipt |  |
| `work-ledger/work-item-report.schema.json` | Work Ledger Work Item Report |  |

### skill · agent & skill meta-tooling
| id | name | description |
|---|---|---|
| `agent-team-orchestrator` | agent-team-orchestrator | Orchestrate team-lead and role-pane workflow for local multi-agent coordination in tmux AI CLI mode, including runtime selection, session bootstrap, and task orchestration. Use when the user asks to initialize, operate, or recover an agent-team session (for example init, tmux-bootstrap, status, or role coordination). |
| `code-doc-features-and-files` | code-doc-features-and-files | Produces a single FEATURES-AND-FILES.md file in a user-supplied target directory that maps project features to the files that implement or support them. Use when the user wants to document which files implement which features, create a feature-to-file map for a project, or generate FEATURES-AND-FILES.md in a given directory. Requires target directory each time; feature list is optional (if omitted, infer from codebase and ask for confirmation before writing). Manual activation only. General agent skill; usable by any skill-capable system. |
| `ponytail-help` | ponytail-help | Quick-reference card for all ponytail modes, skills, and commands. One-shot display, not a persistent mode. Trigger: /ponytail-help, "ponytail help", "what ponytail commands", "how do I use ponytail". |
| `skill-delegate-manager` | skill-delegate-manager | Manage skill-delegate aliases and generated zsh helper functions. |
| `skill-vender-manager` | skill-vender-manager | Manage typed vendor repositories (add, update, upstream-sync, bootstrap, link, unlink, remove), including managed bridges into the skills, commands, and CLI trees. |
| `tmux-background-worker` | tmux-background-worker | Run long-running shell tasks in named tmux sessions so the agent can return control immediately, monitor progress, and clean up completed sessions. Use when users ask to run builds, tests, servers, downloads, migrations, or other unpredictable tasks in the background or without blocking. |
| `workspace-manager` | workspace-manager | Orchestrate a crew of AI coding agents: a single point of contact that spawns, supervises, and tears down worker agents across projects via a workspace CLI — never doing the work itself. |

### skill · agent tooling
| id | name | description |
|---|---|---|
| `s-staging-version-checker` | s-staging-version-checker | Load the staging-version-checker skill on demand. |

### skill · ai / agent orchestration
| id | name | description |
|---|---|---|
| `agent-multiplexer-control` | agent-multiplexer-control | Control an agent multiplexer from inside it: manage workspaces and tabs, split panes, spawn agents, read output, and wait for state changes via CLI over a local unix socket. |

### skill · animation
| id | name | description |
|---|---|---|
| `animate` | animate | Review a feature and enhance it with purposeful animations, micro-interactions, and motion effects that improve usability and delight. |
| `cookbook-animation` | cookbook-animation | Load the animation cookbook skills on demand. Use when the user writes /cookbook-animation or needs GSAP, scroll animation, timeline sequencing, or WebGPU/Three.js guidance. |
| `design-engineering-emil` | design-engineering-emil | Encodes Emil Kowalski's design engineering philosophy — UI polish, component design, animation decisions, easing/duration heuristics, gesture interactions, and the invisible details that make software feel great. Use when reviewing UI code for craft/polish, designing animations, building components (buttons, toasts, popovers, drawers), or asking about taste-driven frontend decisions. |
| `optimize` | optimize | Improve interface performance across loading speed, rendering, animations, images, and bundle size. Makes experiences faster and smoother. |
| `s-code-review` | s-code-review | Review changes with three code-reviewer sub-agents and oracle validation. Use when the user writes /s-code-review or asks for this command. |
| `slack-daily-standup` | slack-daily-standup | Format rough standup notes into a three-section daily update (Yesterday / Today / Blockers), humanize each section via a text skill, preview locally, and post to a registered Slack conversation. |
| `ui-ux-pro-max` | ui-ux-pro-max | UI/UX design intelligence for web and mobile. Includes 50+ styles, 161 color palettes, 57 font pairings, 161 product types, 99 UX guidelines, and 25 chart types across 10 stacks (React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, Tailwind, shadcn/ui, and HTML/CSS). Actions: plan, build, create, design, implement, review, fix, improve, optimize, enhance, refactor, and check UI/UX code. Projects: website, landing page, dashboard, admin panel, e-commerce, SaaS, portfolio, blog, and mobile app. Elements: button, modal, navbar, sidebar, card, table, form, and chart. Styles: glassmorphism, claymorphism, minimalism, brutalism, neumorphism, bento grid, dark mode, responsive, skeuomorphism, and flat design. Topics: color systems, accessibility, animation, layout, typography, font pairing, spacing, interaction states, shadow, and gradient. Integrations: shadcn/ui MCP for component search and examples. |
| `webgpu-threejs-tsl` | webgpu-threejs-tsl | Comprehensive guide for developing WebGPU-enabled Three.js applications using TSL (Three.js Shading Language). Covers WebGPU renderer setup, TSL syntax and node materials, compute shaders, post-processing effects, and WGSL integration. Use this skill when working with Three.js WebGPU, TSL shaders, node materials, or GPU compute in Three.js. |

### skill · ci / devops
| id | name | description |
|---|---|---|
| `staging-log-debug` | staging-log-debug | Fetch staging logs for a required request id via the staging-logs CLI, then analyze them to report root cause plus follow-up actions. Use to debug a staging issue. |
| `staging-version-checker` | staging-version-checker | Check what a configured staging environment is running, what version is deployed, how far it is behind origin/main, and whether recent deployments passed — with failure-cause reporting. |

### skill · design & UI/UX
| id | name | description |
|---|---|---|
| `audit` | audit | Perform comprehensive audit of interface quality across accessibility, performance, theming, and responsive design. Generates detailed report of issues with severity ratings and recommendations. |
| `bolder` | bolder | Amplify safe or boring designs to make them more visually interesting and stimulating. Increases impact while maintaining usability. |
| `extract` | extract | Extract and consolidate reusable components, design tokens, and patterns into your design system. Identifies opportunities for systematic reuse and enriches your component library. |
| `onboard` | onboard | Design or improve onboarding flows, empty states, and first-time user experiences. Helps users get started successfully and understand value quickly. |
| `quieter` | quieter | Tone down overly bold or visually aggressive designs. Reduces intensity while maintaining design quality and impact. |

### skill · diagrams & visualization
| id | name | description |
|---|---|---|
| `ansanabria-skills-recharts` | ansanabria-skills-recharts | Build composable, responsive React charts with Recharts library. Use when creating data visualizations including line charts, area charts, bar charts, pie charts, scatter plots, and composed charts. Handles chart customization, responsive sizing, tooltips, legends, axes configuration, performance optimization, and accessibility. |
| `cookbook-diagram` | cookbook-diagram | Load the diagram cookbook skills on demand. Use when the user writes /cookbook-diagram or needs Mermaid, Excalidraw, or Draw.io diagram guidance. |
| `diagram-excalidraw` | diagram-excalidraw | Create Excalidraw diagram JSON files that make visual arguments. Use when the user wants to visualize workflows, architectures, or concepts. |
| `diagram-mermaid` | diagram-mermaid | Create Mermaid diagrams using the cli-mermaid-agent CLI — generate from a natural-language prompt, validate with mmdc, repair syntax errors via the agent repair loop, render to SVG/PNG/PDF, and lint layout/style. Use when the user asks to draw a flowchart, sequence diagram, class/state diagram, or architecture/process visualization, or asks for a Mermaid file from a description. |
| `notebooklm-infographic-generator` | notebooklm-infographic-generator | Generate NotebookLM infographic image assets from required text input by creating a notebook, adding the text as a source, and downloading one or more infographic variants when users or other skills need visual assets from a written brief. Downloaded infographics are de-watermarked with cli-notebooklm-watermark-remover when that tool is available, with graceful fallback to the original images. |
| `slides` | ckm:slides | Create strategic HTML presentations with Chart.js, design tokens, responsive layouts, copywriting formulas, and contextual slide strategies. |
| `study-plan-generator` | study-plan-generator | Generate a structured study plan for any topic, tailored for senior software engineers. Produces a self-contained folder with a phased PLAN.md, curriculum breakdown, curated resources, project-based exercises, progress tracker, and diagrams (Mermaid roadmap + timeline, Excalidraw concept map). Uses skill@superpowers:brainstorming to interrogate the topic, skill@diagram-mermaid for flowcharts and gantt timelines, and skill@diagram-excalidraw for concept maps. Plans land in a configurable target directory (default ~/study-plans/<category>/<topic-slug>/), not in the agent-tools repo. Use when the user wants to learn a new topic deeply and asks for a study plan, learning roadmap, curriculum, or self-taught course outline. |

### skill · engineering quality & debugging
| id | name | description |
|---|---|---|
| `agent-teams-core` | agent-teams-core | Provide shared filesystem protocol helpers for local multi-agent team skills in tmux AI CLI mode, including task, message, role, heartbeat, recovery, and config operations. Use when the user needs shell-callable core operations, session-state debugging, or config migration support for agent-team workflows. |
| `agent-tools-migration-doctor` | agent-tools-migration-doctor | Manage adoption of the new agent-tools integration architecture across multiple Macs. Provides a six-step doctor flow — status, plan, exec, health, verify, report. Use when bringing a fresh Mac onto the integration engine, when validating an already-migrated Mac is converged, or when diagnosing why a Mac fails strict-idempotent. Wraps the existing `agent-tools` CLI; never invents new install logic. |
| `ai-html-chat` | ai-html-chat | Open an agent-authored HTML artifact in a local browser for a human to review and annotate, then poll the annotations and layout warnings back — a human-in-the-loop review loop for HTML pages, reports, and mockups. |
| `ai-repo-eval` | ai-repo-eval | Evaluate a public AI-focused GitHub repo — security + architecture + adoption — and emit a single combined REPORT.md. Use when the user wants to decide whether (and how) to adopt a repo. Invoke as `skill@ai-repo-eval <github-url>`. |
| `analyze-logs` | analyze-logs | Analyze log files to identify patterns, anomalies, and potential issues. Use when user shares log content, mentions "logs", "log file", "analyze logs", or asks to debug application output. Provides reliability insights and actionable recommendations for general developers. |
| `chrome-devtools-axi` | chrome-devtools-axi | Control a Chrome browser session through the chrome-devtools-axi CLI - navigate, snapshot, click, fill forms, run JavaScript, inspect console and network, take screenshots, audit performance. Use whenever a task needs a real browser: opening or testing a web page, clicking through a flow, extracting page content, or debugging a website. |
| `code-refactor-backend-rust` | code-refactor-backend-rust | Refactor backend Rust files to team style using required file inputs, per-file pre-change summaries, confirmation-gated edits, and strict cargo check/clippy/test gates. |
| `code-refactor-backend-ts` | code-refactor-backend-ts | Refactor backend TypeScript files to team style using required file inputs, per-file pre-change summaries, confirmation-gated edits, and strict zero lint/type issues. |
| `command-creator-j` | command-creator-j | Create and manage long-lived custom command snippets by refining natural-language requirements (via a prompt-optimizer skill) into slug files wired into the global commands index. |
| `cookbook-engineering` | cookbook-engineering | Load the engineering quality cookbook skills on demand. Use when the user writes /cookbook-engineering or needs rigorous debugging, TDD, code review, or production-hardening guidance. |
| `critique` | critique | Evaluate design effectiveness from a UX perspective. Assesses visual hierarchy, information architecture, emotional resonance, and overall design quality with actionable feedback. |
| `deep-research` | deep-research | Generate domain- and topic-specific deep-research prompt markdown files. Uses token-efficient lite template. Use when user wants a structured research prompt for architecture, strategy, policy, AI systems, security, economics, or any complex domain. Prompt is saved to output directory for copy/paste into an LLM. If result > 4900 chars, offers a trimmed version. |
| `diagnose` | diagnose | Disciplined diagnosis loop for hard bugs and performance regressions. Reproduce → minimise → hypothesise → instrument → fix → regression-test. Use when user says "diagnose this" / "debug this", reports a bug, says something is broken/throwing/failing, or describes a performance regression. |
| `grill-with-docs` | grill-with-docs | Grilling session that challenges your plan against the existing domain model, sharpens terminology, and updates documentation (CONTEXT.md, ADRs) inline as decisions crystallise. Use when user wants to stress-test a plan against their project's language and documented decisions. |
| `harden` | harden | Improve interface resilience through better error handling, i18n support, text overflow handling, and edge case management. Makes interfaces robust and production-ready. |
| `improve-codebase-architecture` | improve-codebase-architecture | Find deepening opportunities in a codebase, informed by the domain language in CONTEXT.md and the decisions in docs/adr/. Use when the user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled modules, or make a codebase more testable and AI-navigable. |
| `interview-debrief-coach` | interview-debrief-coach | Turn a recorded interview transcript into a reconciled clean transcript plus a hiring-manager-perspective coaching report rendered as a reviewable HTML artifact. Use when the user provides an interview/recruiter-screen transcript (optionally with a raw auto-transcribed version) and wants a debrief, scorecard, "what I did well / badly", before/after suggested lines, vocabulary to use next time, and lessons learned. Outputs are written into the directory the skill is run from and previewed for human review via skill@ai-html-chat. |
| `linear-create-ticket` | linear-create-ticket | Create Linear tickets from prompt, document, or markdown input with template selection and preview confirmation. Use when user wants to create Linear tickets from natural language, documents, or structured markdown (e.g., "create a ticket for implementing user authentication", "skill@linear-create-ticket"). Supports single tickets, multiple tickets, and tickets with sub-issues. Generates preview file for review before submission to Linear. |
| `plan-software-architect` | plan-software-architect | Guide users through creating comprehensive, production-ready implementation plans by analyzing technical specifications, conducting iterative discovery through strategic multi-choice questions, and generating structured markdown implementation plans with clear milestones. Use when user wants to create an implementation plan from a technical specification, needs architectural guidance for a project, or requires a detailed plan with TDD approach and code samples. |
| `ponytail-audit` | ponytail-audit | Whole-repo audit for over-engineering. Like ponytail-review, but scans the entire codebase instead of a diff: a ranked list of what to delete, simplify, or replace with stdlib/native equivalents. Use when the user says "audit this codebase", "audit for over-engineering", "what can I delete from this repo", "find bloat", "ponytail-audit", or "/ponytail-audit". One-shot report, does not apply fixes. |
| `ponytail-review` | ponytail-review | Code review focused exclusively on over-engineering. Finds what to delete: reinvented standard library, unneeded dependencies, speculative abstractions, dead flexibility. One line per finding: location, what to cut, what replaces it. Use when the user says "review for over-engineering", "what can we delete", "is this over-engineered", "simplify review", or invokes /ponytail-review. Complements correctness-focused review, this one only hunts complexity. |
| `prompt-optimizer` | prompt-optimizer | Improve LLM prompts using proven prompt engineering strategies. Use when user wants to refine a prompt, make instructions clearer, optimize for better AI responses, or apply prompt engineering best practices. |
| `repo-agentic-debug` | repo-agentic-debug | Use to review whether a repo-agentic setup is working as expected. Runs the deterministic quick timeline (cli-repo-agentic-debug) and, with --deep, cross-checks it against .agents/, the rendered host files, and the manifest to judge drift, missing pillars, and failed or skipped steps. Triggered by /debug-repo-agentic-step. |
| `repo-agentic-setup` | repo-agentic-setup | Use to set up a target repo for agentic development (the four pillars - skills, sub-agents, slash-commands, hooks - plus model routing), or to update/migrate an already-configured repo to the latest kits. Detects the stack, composes kits, diagnoses gaps, prescribes library + bespoke artifacts, populates .agents/ and the root AGENTS.md, then shells out to cli-repo-agentic-sync to dry-run and render to all hosts. Triggered by /repo-agentic-setup. |
| `s-prompt-optimizer` | s-prompt-optimizer | Load prompt-optimizer on demand. Use when the user writes /s-prompt-optimizer, asks to optimize a prompt, or runs /use s-prompt-optimizer. |
| `security-check` | security-check | Generate secure-by-design questions from design or component descriptions. Produces a prioritized set of security questions grouped by theme (Architecture, Authentication, etc.) to ensure projects are built with security in mind from the start. Use when reviewing designs, drafting security checklists, asking for secure-by-design questions, or evaluating system security at the design level. |
| `superpower-grill` | superpower-grill | Load the Superpowers planning discipline, then grill the user relentlessly about a plan or design until shared understanding is reached. Combines /s-superpower (Superpowers framework bootstrap) with skill@grill-me. Use when the user wants a Superpowers-grade, adversarial stress-test of a plan — "grill me with superpowers", "superpower grill", or invokes /s-superpower-grill. |

### skill · git / PR / commit
| id | name | description |
|---|---|---|
| `code-feature-scoped-commit-porter` | code-feature-scoped-commit-porter | Creates feature-scoped local commits by porting changes from a newer commit range onto an older base with strict validation gates, optional feature map generation, and auditable phase-based reporting. |
| `code-reviewer` | code-reviewer | Perform comprehensive code reviews with severity-based prioritization. Use when the user wants code reviewed, shares code snippets or diffs, provides file paths for review, or shares GitHub URLs (PRs, files, folders). Supports local files, git diffs, inline code, and GitHub CLI (`gh`) integration for remote resources. |
| `code-tutor` | code-tutor | Collaborate on code and PR reviews through priority-sorted lockstep discussion, changed-line coverage tracking, zero-unknown ship readiness gates, and no-edit refactor planning. Use when users want to understand and validate code before opening or approving PRs. |
| `git-auto-commit` | git-auto-commit | Create a guarded local Git commit from staged changes by default, optionally include unstaged changes, and auto-generate a commit message when the user leaves it blank. Use when user wants Commit behavior with a required SUBMIT confirmation before committing. |
| `git-auto-commit-and-push` | git-auto-commit-and-push | Create a guarded local Git commit and then push the current branch, using staged changes by default, optionally including unstaged changes, and auto-generating a commit message when blank. Use when user wants Commit & push behavior with a required SUBMIT confirmation before commit or push. |
| `git-commit-message` | git-commit-message | Generate conventional commit messages from staged Git changes. Automatically reads git diff --staged, analyzes changes, and produces a properly formatted commit message with title, body, and breaking change footer. Use when user wants to generate a commit message, needs help writing a commit, or asks for a summary of staged changes. |
| `git-merge-ff` | git-merge-ff | Merge a target remote branch into the current local branch by defaulting to a temporary git worktree, resolving conflicts there, and fast-forwarding the original branch back only after success. Use when user invokes skill@git-merge-ff with an optional bare branch name such as main. |
| `git-pr-create-apps-monorepo` | git-pr-create-apps-monorepo | Create GitHub pull requests for a configured apps monorepo with automatic ticket extraction, base-branch detection, multi-component (apps/packages) detection, and a minimal structured description. |
| `git-pr-create-plugin` | git-pr-create-plugin | Create GitHub pull requests for a configured plugin repository with ticket extraction, base-branch detection, and PR-template population (Areas Affected, Verification). |
| `git-pr-create-webapp` | git-pr-create-webapp | Create GitHub pull requests for a configured web-app repository with automatic ticket-id extraction, base-branch detection, PR-template population, and preview confirmation. |
| `git-pr-reviewer` | git-pr-reviewer | Review GitHub Pull Requests using GitHub CLI (`gh`). Creates local review files for collaborative editing before posting comments to GitHub. Use when user wants to review a PR, check code changes, or analyze pull request quality. |
| `git-refactor-staged` | git-refactor-staged | Detect git-staged changes and generate a production-grade refactor plan via a planning skill (reads `git diff --cached`, emits a PLAN-refactor file). |
| `git-refactor-with-git` | git-refactor-with-git | Create production-grade refactor plans from git commit-range changes with semantic numbered refactor options and user multi-select flow. Supports start+end or start-only (end defaults to HEAD). |
| `git-scoped-commits` | git-scoped-commits | Create scoped commits in logical chunks for the current local git repo. Groups uncommitted changes by top-level directory, then commits each chunk via repo-local scripts/committer (when present) or git add + git commit. Use when user wants to commit working-tree changes in logical chunks. Local only—never push to remote. |
| `git-ssh-signing-setup` | git-ssh-signing-setup | Configure SSH commit signing for GitHub repos on Macs with multiple GitHub SSH host aliases. Use when a repo should auto-sign commits using the same account identity implied by its origin SSH alias in ~/.ssh/config, or when setting up/revalidating this behavior across Agent Tools machines. |
| `github-multi-account-doctor` | github-multi-account-doctor | Use when reviewing, initializing, auditing, fixing, or diagnosing a Mac's multi-GitHub-account Git and SSH setup, especially when standardizing account-specific SSH aliases, per-account Git identity, and safe config updates without deleting existing SSH keys. |
| `grill-me` | grill-me | Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when user wants to stress-test a plan, get grilled on their design, or mentions "grill me". |
| `linear-create-ticket-with-git` | linear-create-ticket-with-git | Create Linear tickets from Git branch context with requirement-first narrative generation and preview confirmation. Use when user wants to create a Linear ticket based on current branch changes while making the ticket read like planned requirements rather than implementation logs. |
| `linear-pr-comment-follow-up` | linear-pr-comment-follow-up | Create Linear tickets from GitHub PR comment links. Extracts comment content and PR context, then creates a follow-up Linear ticket using linear-create-ticket. After SUBMIT, posts the GitHub reply in the review discussion thread (in_reply_to) for |
| `linear-solve` | linear-solve | Automate the Linear ticket workflow: fetch ticket details, create a properly-named git branch, and generate a PLAN file via a planning skill. Use to start work on a ticket by id. |
| `linear-ticket-and-pr` | linear-ticket-and-pr | Create a Linear ticket AND a GitHub pull request for the current branch in one SUBMIT-gated workflow, then cross-link them both directions. Reuses a ticket-drafting skill and delegates PR creation. |
| `local-pr-review` | local-pr-review | Use when reviewing a GitHub pull request locally, especially when the user provides a PR URL and wants a read-only report without GitHub comments, checkout mutations, or remote writes. |
| `openclaw-local-deployment` | openclaw-local-deployment | Deploys OpenClaw from local source via pnpm build + ui:build and install (no reconfig by default); optional test; use --skip-test when invoking deploy.sh to avoid prompts. Safety checks for clean git status and repo presence. |
| `prototype` | prototype | Build a throwaway prototype to flesh out a design before committing to it. Routes between two branches — a runnable terminal app for state/business-logic questions, or several radically different UI variations toggleable from one route. Use when the user wants to prototype, sanity-check a data model or state machine, mock up a UI, explore design options, or says "prototype this", "let me play with it", "try a few designs". |
| `skill-creator-j` | skill-creator-j | Create and update agent skills programmatically with natural-language input parsing, interactive prompting, and automatic validation. Use to create a new skill (e.g., 'create a skill for PDF processing') or update an existing one. |
| `skill-delegate-shell-function` | skill-delegate-shell-function | Create new skill-delegate-powered shell functions following the ai-git-auto-commit pattern. Use when adding a new AI utility shell function that wraps skill-delegate, needs multi-step orchestration (stage, generate, commit), or requires option flags like --review and --push. skill-delegate-aliases.zsh is the central registry for all ai-* functions — simple pass-through wrappers and complex custom bodies both live there. |
| `skill-library` | skill-library | Resolves `skill@<name>` references that are not in the active session: loads the archived skill from the on-demand library and follows it inline. The dynamic skill-loading backbone. |
| `yesterday-linear-gh-cutoff` | yesterday-linear-gh-cutoff | Summarize the prior calendar day's Linear activity for the authenticated viewer and GitHub commits by the configured author; show a short bullet list and require an explicit cutoff before finalizing the narrative. |

### skill · misc / utility
| id | name | description |
|---|---|---|
| `ai-request-duration-tracker` | ai-request-duration-tracker | Track and report request/response timing for each conversation request with a Time Tracking Summary. Use when users want per-request timing, especially for large tasks. |
| `code-index-knowledge` | code-index-knowledge | Generate hierarchical AGENTS.md knowledge bases for code-focused repositories, including a root file and complexity-scored subdirectory documentation. Use when asked to create or update AGENTS.md files, knowledge bases, or codebase indexing documentation. |
| `code-repo-rules-to-mdc` | code-repo-rules-to-mdc | Analyze local or GitHub repositories to extract explicit and inferred best-practice rules and generate consolidated/split .mdc files plus a separate RULE_EVIDENCE_REPORT.md with citations. Use when users request AI IDE rule extraction for Cursor or Antigravity. |
| `crawler-medium-to-markdown` | crawler-medium-to-markdown | Convert one or more Medium article URLs into Markdown files via a local converter, writing outputs locally and returning a summary of file paths and errors. |
| `delight` | delight | Add moments of joy, personality, and unexpected touches that make interfaces memorable and enjoyable to use. Elevates functional to delightful. |
| `openclaw-model-switch` | openclaw-model-switch | Switch OpenClaw session gateway provider/model/thinking by direct target or numbered selection. |
| `safe-extract` | safe-extract | Advisory wrapper around the cli-safe-extract tool. Use when the user wants to safely extract an untrusted archive (zip/tar/7z/rar/etc.): inspect it in an isolated sandbox, read the JSON manifest, and recommend which files are safe to promote with reasoning. Drives `cli-safe-extract inspect` and `promote`; can auto-promote the SAFE tier with --auto. Cannot override the engine's HARD BLOCK rules (zip-slip, escaping symlinks, scan hits) — those are enforced in deterministic code. |

### skill · planning / research / prompts
| id | name | description |
|---|---|---|
| `d-session` | d-session | Initialize delegation sessions and route explicit prompts through agent-delegate using /d-session syntax. Use when users invoke skill@d-session or /d-session. |
| `plan-master` | plan-master | Transform user task descriptions into comprehensive engineering plans following a structured PLAN-<slug>.md format. Use when user wants to create a detailed engineering plan from a task description, needs to break down complex tasks into actionable steps, or requires a production-grade plan document. |
| `reverse-engineer-prompt` | reverse-engineer-prompt | Analyzes multi-turn conversations and reconstructs a single, self-contained prompt that would generate the final response in one interaction; supports saving markdown output with versioned filenames. |
| `skill-creator-j-repo` | skill-creator-j-repo | Create repo-local agent skills under ./.agents/skills by wrapping skill-creator-j with repo-aware prompts, explicit output paths, and repo-local ./.claude/skills symlinks for Claude Code. Use when user wants a new skill created inside the current repository instead of a home-directory skills folder. |

### skill · productivity
| id | name | description |
|---|---|---|
| `work-ledger-init` | work-ledger-init | Initialize a machine for work-ledger auto-finalize and optional auto-submit to a shared ledger repo, with verification steps suitable for repeating across machines. |

### skill · repo-agentic / infra tooling
| id | name | description |
|---|---|---|
| `ai-dir-init` | ai-dir-init | Creates standard per-directory AGENTS.md files for a target repo directory, supporting single-target initialization and guided --all multi-directory selection for monorepos. |
| `ai-dir-sync` | ai-dir-sync | Synchronize one project-local AI directory (.codex, .cursor, .claude, or .antigravity) to the other AI directories with a dry-run-first workflow, source-precedence conflict resolution, symlink preservation, and target-only file retention. Use when users ask to mirror or update AI tool directories inside the current repository. |
| `gitnexus-doctor` | gitnexus-doctor | Use when checking, initializing, refreshing, or troubleshooting GitNexus indexing for a repository, especially when mcp-router is the single active MCP server or a repo needs GitNexus analyze/status/list validation. |
| `mcp-router-hard-reset` | mcp-router-hard-reset | Hard reset mcp-router broker and session state by deleting the broker runtime directory (sockets, PID, pooled downstream state). Use when stale brokers, stuck sessions, or corrupted IPC require a clean runtime after confirming the active config path. |
| `opencode-plugin-manager` | opencode-plugin-manager | Manage OpenCode plugins with cli-opencode-manager plugin, including doctor/status checks and add, update, or delete plugin configuration. Use when user asks to inspect plugin health, add a supported plugin, refresh plugin bootstrap config, or remove an OpenCode plugin. |
| `ponytail-debt` | ponytail-debt | Harvest every `ponytail:` comment in the codebase into a debt ledger, so the deliberate shortcuts and deferrals ponytail leaves behind get tracked instead of rotting into "later means never". Use when the user says "ponytail debt", "/ponytail-debt", "what did ponytail defer", "list the shortcuts", "ponytail ledger", or "what did we mark to do later". One-shot report, changes nothing. |

### skill · resume toolkit
| id | name | description |
|---|---|---|
| `agent-team-coder` | agent-team-coder | Execute coder-role workflow for local multi-agent coordination in tmux AI CLI mode, with assigned-worktree implementation, recovery handling, messaging, and handoff continuity. Use when the user asks the coder role to register or resume, implement assigned tasks, validate worktree context, or request/apply recovery guidance. |
| `agent-team-planner` | agent-team-planner | Handle planner-role workflow for local multi-agent coordination in tmux AI CLI mode, including registration, planning artifacts, messaging, and continuity updates. Use when the user asks the planner role to register or resume, pick assigned planning tasks, or produce planning deliverables. |
| `agent-team-reviewer` | agent-team-reviewer | Perform reviewer-role workflow for local multi-agent coordination in tmux AI CLI mode, with findings-first review, messaging, and continuity-safe reporting. Use when the user asks the reviewer role to register or resume, review assigned outputs, or publish structured review findings and recommendations. |
| `agent-team-tester` | agent-team-tester | Run tester-role workflow for local multi-agent coordination in tmux AI CLI mode, including assigned-task validation, bug verification, messaging, and reporting outputs. Use when the user asks the tester role to register or resume, execute verification tasks, or produce regression and defect reports. |
| `cookbook-resume` | cookbook-resume | Load the resume toolkit cookbook skills on demand. Use when the user writes /cookbook-resume or needs resume diagnosis, rewriting, tailoring, or multi-perspective scoring. |
| `resume-diagnoser` | resume-diagnoser | Diagnose a resume beyond surface-level review. Scans the resume the way an Applicant Tracking System (ATS) and senior reviewer would, flagging vague phrasing, missing quantification, weak verbs, formatting that breaks parsers, role/responsibility/impact gaps, and unclear seniority signals. Produces a section-by-section critique with the exact issues found and specific instructions to fix them. Use when the user wants to audit a resume, find weaknesses, identify what is missing, or check ATS-readability before applying. |
| `resume-hiring-manager` | resume-hiring-manager | Act as a hiring manager for the user's target role and conduct a final review plus lifelike interview. Reviews the resume through a hiring manager's lens (leadership, team impact, scope of ownership, business outcomes, seniority calibration), then runs a mock interview with the hardest technical and behavioral questions in the field, rates each answer 0-10 with specific feedback, and ends with a hire/no-hire verdict plus the gaps the candidate must close. Use when the user wants a hiring-manager review, interview prep, mock interview, leadership/impact assessment, or a hire/no-hire verdict. |
| `resume-panel` | resume-panel | Run a full multi-persona hiring panel over a resume against one exact role/JD, then rewrite the weak parts. Four reviewers in one pass — ATS scanner, recruiter, hiring manager, and a domain Staff/Senior peer — each producing an independent match score (ATS /100, Recruiter /100, Hiring Manager /100). Then synthesizes the panel into top missing keywords, strengths, weaknesses, 10-second red flags, and skills to emphasize vs de-emphasize, and finally rewrites only the sections that need it using the Google XYZ formula — ATS-optimized, human-readable, truthful, no fluff. Use when the user wants the whole gauntlet at once (score + diagnose + HM review + rewrite) for a specific job, not a single-lens pass. |
| `resume-recruiter-scorer` | resume-recruiter-scorer | Score a resume the way a recruiter would using the find/attract/engage/hire lens. Compares the resume to typical job descriptions in the user's stated field (or against a provided JD/role), extracts the top keywords, skills, and signals recruiters search for, scores the resume against them (0-100 with subscores per lens), and lists the missing keywords/competencies plus a prioritized fix list. Use when the user wants a recruiter-style scorecard, keyword-gap analysis, JD match score, or to know whether a recruiter would shortlist them. |
| `resume-rewriter-xyz` | resume-rewriter-xyz | Rewrite resume bullets using the Google XYZ formula 'Accomplished [X] as measured by [Y], by doing [Z]'. Forces quantification of impact, surfaces missing metrics by asking targeted follow-up questions, applies patterns used by candidates landing roles at Meta, Google, and Fortune 500 companies, and returns before/after comparisons per bullet with the X/Y/Z components labeled. Use when the user wants to rewrite, strengthen, quantify, or punch up resume bullets/experience entries. |

### skill · session / interaction / logs
| id | name | description |
|---|---|---|
| `caveman` | caveman | Ultra-compressed communication mode. Cuts token usage ~75% by dropping filler, articles, and pleasantries while keeping full technical accuracy. Use when user says "caveman mode", "talk like caveman", "use caveman", "less tokens", "be brief", or invokes /caveman. |

### skill · writing / content
| id | name | description |
|---|---|---|
| `adapt` | adapt | Adapt designs to work across different screen sizes, devices, contexts, or platforms. Ensures consistent experience across varied environments. |
| `ai-handover` | ai-handover | Summarize AI agent conversations for handoff to another AI agent in a new session. Creates structured summaries with context, decisions, tasks, discoveries, technical details, metrics, and sentiment analysis. Use when user wants to summarize current chat session, create handoff notes, capture conversation context for continuation, or prepare session summary. |
| `ai-handover-prompt` | ai-handover-prompt | Generate a tight, copy-pasteable next-session bootstrap prompt (5-12 lines) that triggers the next planned task immediately in a fresh Claude Code session, with just-enough context and no recap noise. Use when the user wants a quick trigger prompt for the next task, a session bootstrap, a "drop this into the next session" prompt, or says "give me a prompt to start the next task". Companion to ai-handover (full 9-section record); this produces a single focused action prompt. |
| `ai-result-rating` | ai-result-rating | Evaluate AI output quality on a 1-100 scale with education-level equivalents. Analyzes AI responses against prompts and original content, providing detailed scores, deductions, and improvement suggestions. Use when you need to assess how well an AI performed a task, compare AI outputs, or identify areas for prompt improvement. |
| `ai-result-rating-lite` | ai-result-rating-lite | Rate AI-generated outputs on a letter grade scale (A+ to F) with justifications and numerical score. Use when user wants to evaluate AI response quality, compare AI output to expert-level work, get structured feedback on AI-generated content, or assess how well an AI performed a task. |
| `brand` | ckm:brand | Brand voice, visual identity, messaging frameworks, asset management, brand consistency. Activate for branded content, tone of voice, marketing assets, brand compliance, style guides. |
| `clarify` | clarify | Improve unclear UX copy, error messages, microcopy, labels, and instructions. Makes interfaces easier to understand and use. |
| `cli-anything-agent-tools` | cli-anything-agent-tools | Create or refine a CLI-Anything-derived CLI following repo conventions for layout, Python version, env vars, packaging, TOON output, and tests. |
| `colorize` | colorize | Add strategic color to features that are too monochromatic or lack visual interest. Makes interfaces more engaging and expressive. |
| `cookbook-content` | cookbook-content | Load the content and writing cookbook skills on demand. Use when the user writes /cookbook-content or needs writing quality, text refinement, presentation, or brand voice guidance. |
| `cookbook-design-craft` | cookbook-design-craft | Load the design-craft cookbook skills on demand. Use when the user writes /cookbook-design-craft or asks for design craft guidance. |
| `debate-analyzer` | debate-analyzer | Analyze debates and discussions to identify primary disagreements, extract arguments from each party, detect cognitive biases, and predict outcomes. Use when given debate transcripts, discussion threads, or argumentative content requiring structured analysis. |
| `distill` | distill | Strip designs to their essence by removing unnecessary complexity. Great design is simple, powerful, and clean. |
| `intent-layer` | intent-layer | Set up hierarchical Intent Layer (AGENTS.md files) for codebases. Use when initializing a new project, adding context infrastructure to an existing repo, user asks to set up AGENTS.md, add intent layer, make agents understand the codebase, or scaffolding AI-friendly project documentation. |
| `linkedin-post-engineer` | linkedin-post-engineer | Create production-ready LinkedIn posts for engineering audiences by collecting missing context one question at a time, researching X.com hot topics when needed, and applying a layered Web2.5 plus master style framework with mandatory skill@text-humanizer final pass. |
| `normalize` | normalize | Normalize design to match your design system and ensure consistency |
| `polish` | polish | Final quality pass before shipping. Fixes alignment, spacing, consistency, and detail issues that separate good from great. |
| `question-widget` | question-widget | Re-ask the most recent clarifying question using the host's native interactive question widget instead of plaintext A/B/C/D menus. Use when the user triggers `skill@question-widget` (typically after the agent just emitted a plaintext multiple-choice question), or any time a structured/multiple-choice question is about to be asked on a host that exposes a native question UI (Claude Code `AskUserQuestion`, OpenCode `question`, Codex structured question tool, Gemini `ask_user`). |
| `s-cli-anything` | s-cli-anything | Load cli-anything on demand. Use when the user writes /s-cli-anything, asks to run cli-anything, or runs /use s-cli-anything. |
| `s-executing-plans` | s-executing-plans | Load the Superpowers executing-plans skill on demand. Use when the user writes /s-executing-plans or runs /use s-executing-plans. |
| `s-grill-me` | s-grill-me | Load grill-me on demand. Use when the user writes /s-grill-me, asks to be grilled about a plan or design, or runs /use s-grill-me. |
| `s-grill-with-docs` | s-grill-with-docs | Load grill-with-docs on demand. Use when the user writes /s-grill-with-docs, asks to grill a plan against project docs, or runs /use s-grill-with-docs. |
| `s-superpower` | s-superpower | Load Superpowers on demand from skills-library. Use when the user writes /s-superpower, asks to use Superpowers, or runs /use s-superpower. |
| `s-superpower-grill` | s-superpower-grill | Load Superpowers and grill-me together on demand. Use when the user writes /s-superpower-grill or runs /use s-superpower-grill. |
| `s-takeover` | s-takeover | Resolve and ingest a previous session from another tool. Use when the user writes /s-takeover, /takeover, or runs /use s-takeover. |
| `s-text-humanizer` | s-text-humanizer | Load text-humanizer on demand. Use when the user writes /s-text-humanizer, asks to humanize text, or runs /use s-text-humanizer. |
| `sub-agent-library` | sub-agent-library | MANDATORY when the user writes `subagent@<name>` for any name that is not in the active sub-agent list. Resolves the host-appropriate flavor (cc on Claude Code, oc on OpenCode/Codex), runs `cli-sub-agent-library load <name>@<flavor>`, and dispatches the persona via the host's native sub-agent mechanism (or inline fallback). |
| `teach-impeccable` | teach-impeccable | One-time setup that gathers design context for your project and saves it to your AI config file. Run once to establish persistent design guidelines. |
| `text-humanizer` | text-humanizer | Transform AI-generated text into natural, human-sounding writing. Use when user wants to humanize AI output, make text sound more conversational, or reduce AI-detectable patterns in writing. Preserves meaning while improving authenticity and readability. |
| `text-refiner` | text-refiner | Refine and improve text for clarity, coherence, grammar, and style. Use when user wants to improve their writing, fix grammar issues, enhance clarity, or adjust tone and style of text. Prompts for preferences before refining and optionally shows what changed. |
| `to-prd` | to-prd | Turn the current conversation context into a PRD and publish it to the project issue tracker. Use when user wants to create a PRD from the current context. |

### sub-agent · delegation / coordination
| id | name | description |
|---|---|---|
| `btw-side` | btw-side | Side-channel quick-answer agent for quick questions: forks an existing session's context to answer without tools and without polluting the main transcript. |

### sub-agent · planning / strategy / advisory
| id | name | description |
|---|---|---|
| `plan-master` | plan-master | Engineering planning agent. Creates structured PLAN-<slug>.md implementation plans using the plan-master skill. Always runs on Opus to guarantee maximum planning quality and codebase reasoning. |
| `strategic-partner` | strategic-partner | High-level strategic thinking partner. Use when a request needs challenge, stress-testing, trade-off analysis, and decision-quality guidance before execution. |
| `strategic-partner-unlock` | strategic-partner-unlock | High-level strategic thinking partner with unrestricted tool access. Use when a request needs challenge, stress-testing, trade-off analysis, and decision-quality guidance with full environment access. |

### sub-agent · review / quality / security
| id | name | description |
|---|---|---|
| `cli-developer` | cli-developer | Language-agnostic CLI/TUI engineer. Designs commands, flags and subcommands (POSIX/GNU), help/usage text, exit-code contracts, stdout=data / stderr=diagnostics separation, pipe and streaming friendliness, TTY/NO_COLOR-aware output, machine-readable --json, shell completions, and packaging. Use for command-line tool feature work and UX review. |
| `code-reviewer` | code-reviewer | Reviews code for quality, bugs, security, and best practices |
| `oracle` | oracle | Principal engineering advisor for deep code reviews, architecture decisions, complex debugging, and planning. Delegates to a high-reasoning model for maximum depth. Prompt with a precise problem plus files; ask for concrete outcomes. |
| `parallel-manager` | parallel-manager | Primary coordination wrapper for same-repo parallel work. Apply worktree and lock policy first, then delegate to the best specialist agent for planning, implementation, review, or deep technical analysis. |

## Vendored (curated, not authored)
| name | origin | license | link |
|---|---|---|---|
| `diagram-drawio` | Agents365-ai/drawio-skill | MIT | [↗](https://github.com/Agents365-ai/drawio-skill) |
| `ponytail` | DietrichGebert/ponytail | MIT | [↗](https://github.com/DietrichGebert/ponytail) |
| `gsap-core` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-frameworks` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-performance` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-plugins` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-react` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-scrolltrigger` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-timeline` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `gsap-utils` | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| `frontend-design` | anthropics/skills | Apache-2.0 | [↗](https://github.com/anthropics/skills/tree/main/skills/frontend-design) |
| `design-system` | claudekit | MIT | [↗](https://docs.claudekit.cc/docs/marketing/skills/design-system/) |
| `teach` | mattpocock/skills | MIT | [↗](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach) |
| `ui-styling` | mrgoonie/claudekit-skills | MIT | [↗](https://github.com/mrgoonie/claudekit-skills) |
| `agency-agents-accessibility-auditor` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-ai-data-remediation-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-ai-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-api-tester` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-autonomous-optimization-architect` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-backend-architect` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-behavioral-nudge-engine` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-brand-guardian` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-cms-developer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-code-reviewer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-codebase-onboarding-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-data-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-database-optimizer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-devops-automator` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-email-intelligence-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-embedded-firmware-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-evidence-collector` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-experiment-tracker` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-feedback-synthesizer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-feishu-integration-developer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-filament-optimization-specialist` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-frontend-developer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-git-workflow-master` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-image-prompt-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-incident-response-commander` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-inclusive-visuals-specialist` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-jira-workflow-steward` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-minimal-change-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-mobile-app-builder` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-performance-benchmarker` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-product-manager` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-project-shepherd` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-rapid-prototyper` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-reality-checker` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-security-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-senior-developer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-senior-project-manager` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-software-architect` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-solidity-smart-contract-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-sprint-prioritizer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-sre-site-reliability-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-studio-operations` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-studio-producer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-technical-writer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-test-results-analyzer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-threat-detection-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-tool-evaluator` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-trend-researcher` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-ui-designer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-ux-architect` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-ux-researcher` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-visual-storyteller` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-voice-ai-integration-engineer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-wechat-mini-program-developer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-whimsy-injector` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `agency-agents-workflow-optimizer` | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| `banner-design` | nextlevelbuilder/ui-ux-pro-max-skill | MIT | [↗](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| `design` | nextlevelbuilder/ui-ux-pro-max-skill | MIT | [↗](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| `brainstorming` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `dispatching-parallel-agents` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `executing-plans` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `finishing-a-development-branch` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `receiving-code-review` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `requesting-code-review` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `subagent-driven-development` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `systematic-debugging` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `test-driven-development` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `using-git-worktrees` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `using-superpowers` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `verification-before-completion` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `writing-plans` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `writing-skills` | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| `ai-improve` | shadcn/improve | MIT | [↗](https://github.com/shadcn/improve) |
| `resume-tailoring` | varunr89/resume-tailoring-skill | MIT | [↗](https://github.com/varunr89/resume-tailoring-skill) |
| `react-best-practices` | vercel-labs/agent-skills | MIT | [↗](https://github.com/vercel-labs/agent-skills) |
