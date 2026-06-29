# Catalog

_Generated — do not edit by hand._

**390 publishable items** across 9 pillars. Authored by the owner unless tagged vendored.

## Contents

- [Headline counts](#headline)
- [Highlights](#highlights)
- [Authored capabilities](#authored-capabilities)
  - [skill](#skill) · [sub-agent](#sub-agent) · [cli](#cli) · [hook](#hook) · [kit](#kit) · [host](#host) · [integration](#integration) · [schema](#schema) · [adr](#adr)
- [Vendored (curated)](#vendored-curated-not-authored)

## Headline
- **skill**: 182 published (147 authored)
- **sub-agent**: 64 published (8 authored)
- **cli**: 50 published (50 authored)
- **hook**: 4 published (4 authored)
- **kit**: 7 published (7 authored)
- **host**: 14 published (14 authored)
- **integration**: 10 published (10 authored)
- **schema**: 6 published (6 authored)
- **adr**: 53 published (53 authored)

## Highlights
| name | what it does |
|---|---|
| **ai-crew** | A loopback-only daemon that orchestrates labelled AI coding-agent sessions: routing prompts to workers, tailing transcripts, and returning results and tokens. |
| **ai-html-chat** | Open an agent-authored HTML artifact in a local browser for a human to review and annotate, then poll the annotations and layout warnings back — a human-in-the-loop review loop for HTML pages, reports, and mockups. |
| **chrome-devtools-manager** | Control a Chrome browser session through the chrome-devtools-manager CLI — navigate, snapshot, click, fill forms, run JavaScript, inspect console and network, take screenshots, audit performance. Use whenever a task needs a real browser: opening or testing a web page, clicking through a flow, extracting page content, or debugging a website. |
| **no-mistakes** | Centrally version-controlled config for an AI-agent-driven validation gate that runs review, tests, lint, docs, and CI before code reaches its push target. |
| **repo-agentic-setup** | Use to set up a target repo for agentic development (the four pillars - skills, sub-agents, slash-commands, hooks - plus model routing), or to update/migrate an already-configured repo to the latest kits. Detects the stack, composes kits, diagnoses gaps, prescribes library + bespoke artifacts, populates .agents/ and the root AGENTS.md, then shells out to cli-repo-agentic-sync to dry-run and render to all hosts. Triggered by /repo-agentic-setup. |
| **skill-library** | Resolves `skill@<name>` references that are not in the active session: loads the archived skill from the on-demand library and follows it inline. The dynamic skill-loading backbone. |

## Authored capabilities

### skill

<details>
<summary><strong>agent & skill meta-tooling</strong> (7)</summary>

| name | updated | what it does |
|---|---|---|
| agent-team-orchestrator | 2026-04-25 | Orchestrate team-lead and role-pane workflow for local multi-agent coordination in tmux AI CLI mode, including runtime selection, session bootstrap, and task orchestration. Use when the user asks to initialize, operate, or recover an agent-team session (for example init, tmux-bootstrap, status, or role coordination). |
| code-doc-features-and-files | 2026-04-25 | Produces a single FEATURES-AND-FILES.md file in a user-supplied target directory that maps project features to the files that implement or support them. Use when the user wants to document which files implement which features, create a feature-to-file map for a project, or generate FEATURES-AND-FILES.md in a given directory. Requires target directory each time; feature list is optional (if omitted, infer from codebase and ask for confirmation before writing). Manual activation only. General agent skill; usable by any skill-capable system. |
| ponytail-help | 2026-06-18 | Quick-reference card for all ponytail modes, skills, and commands. One-shot display, not a persistent mode. Trigger: /ponytail-help, "ponytail help", "what ponytail commands", "how do I use ponytail". |
| skill-delegate-manager | 2026-04-26 | Manage skill-delegate aliases and the generated zsh helper functions via the `skill-delegate alias` CLI — add, update, delete, list, seed, render, and install ai-* shell shortcuts without hand-editing the generated YAML/zsh. |
| skill-vender-manager | 2026-04-28 | Manage typed vendor repositories (add, update, upstream-sync, bootstrap, link, unlink, remove), including managed bridges into the skills, commands, and CLI trees. |
| tmux-background-worker | 2026-04-25 | Run long-running shell tasks in named tmux sessions so the agent can return control immediately, monitor progress, and clean up completed sessions. Use when users ask to run builds, tests, servers, downloads, migrations, or other unpredictable tasks in the background or without blocking. |
| workspace-manager | 2026-06-24 | Orchestrate a crew of AI coding agents: a single point of contact that spawns, supervises, and tears down worker agents across projects via a workspace CLI — never doing the work itself. |

</details>

<details>
<summary><strong>agent tooling</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| s-staging-version-checker | 2026-05-31 | Load the staging-version-checker skill on demand. |

</details>

<details>
<summary><strong>ai / agent orchestration</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| agent-multiplexer-control | 2026-06-06 | Control an agent multiplexer from inside it: manage workspaces and tabs, split panes, spawn agents, read output, and wait for state changes via CLI over a local unix socket. |

</details>

<details>
<summary><strong>animation</strong> (8)</summary>

| name | updated | what it does |
|---|---|---|
| animate | 2026-04-26 | Review a feature and enhance it with purposeful animations, micro-interactions, and motion effects that improve usability and delight. |
| cookbook-animation | 2026-05-31 | On-demand loader that pulls the core GSAP animation skills (core, timeline, performance) plus task-conditional ones for React/Vue, ScrollTrigger, plugins, utils, and WebGPU/Three.js. |
| design-engineering-emil | 2026-05-20 | Encodes Emil Kowalski's design engineering philosophy — UI polish, component design, animation decisions, easing/duration heuristics, gesture interactions, and the invisible details that make software feel great. Use when reviewing UI code for craft/polish, designing animations, building components (buttons, toasts, popovers, drawers), or asking about taste-driven frontend decisions. |
| optimize | 2026-04-26 | Find and fix interface performance issues across loading, rendering, animations, images, and bundle size, measuring Core Web Vitals before and after so effort targets what actually matters. |
| s-code-review | 2026-05-31 | Review changes with three code-reviewer sub-agents and oracle validation. Use when the user writes /s-code-review or asks for this command. |
| slack-daily-standup | 2026-04-26 | Format rough standup notes into a three-section daily update (Yesterday / Today / Blockers), humanize each section via a text skill, preview locally, and post to a registered Slack conversation. |
| ui-ux-pro-max | 2026-04-26 | UI/UX design intelligence for web and mobile. Includes 50+ styles, 161 color palettes, 57 font pairings, 161 product types, 99 UX guidelines, and 25 chart types across 10 stacks (React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, Tailwind, shadcn/ui, and HTML/CSS). Actions: plan, build, create, design, implement, review, fix, improve, optimize, enhance, refactor, and check UI/UX code. Projects: website, landing page, dashboard, admin panel, e-commerce, SaaS, portfolio, blog, and mobile app. Elements: button, modal, navbar, sidebar, card, table, form, and chart. Styles: glassmorphism, claymorphism, minimalism, brutalism, neumorphism, bento grid, dark mode, responsive, skeuomorphism, and flat design. Topics: color systems, accessibility, animation, layout, typography, font pairing, spacing, interaction states, shadow, and gradient. Integrations: shadcn/ui MCP for component search and examples. |
| webgpu-threejs-tsl | 2026-05-26 | Comprehensive guide for developing WebGPU-enabled Three.js applications using TSL (Three.js Shading Language). Covers WebGPU renderer setup, TSL syntax and node materials, compute shaders, post-processing effects, and WGSL integration. Use this skill when working with Three.js WebGPU, TSL shaders, node materials, or GPU compute in Three.js. |

</details>

<details>
<summary><strong>ci / devops</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| staging-log-debug | 2026-04-27 | Fetch staging logs for a required request id via the staging-logs CLI, then analyze them to report root cause plus follow-up actions. Use to debug a staging issue. |
| staging-version-checker | 2026-05-17 | Check what a configured staging environment is running, what version is deployed, how far it is behind origin/main, and whether recent deployments passed — with failure-cause reporting. |

</details>

<details>
<summary><strong>design & UI/UX</strong> (5)</summary>

| name | updated | what it does |
|---|---|---|
| audit | 2026-04-26 | Perform comprehensive audit of interface quality across accessibility, performance, theming, and responsive design. Generates detailed report of issues with severity ratings and recommendations. |
| bolder | 2026-04-26 | Amplify safe or boring designs to make them more visually interesting and stimulating. Increases impact while maintaining usability. |
| extract | 2026-04-26 | Extract and consolidate reusable components, design tokens, and patterns into your design system. Identifies opportunities for systematic reuse and enriches your component library. |
| onboard | 2026-04-26 | Design or improve onboarding flows, empty states, and first-time experiences, focusing the path on the user's 'aha moment' so they reach value quickly rather than learning everything. |
| quieter | 2026-04-26 | Tone down overly bold or visually aggressive designs. Reduces intensity while maintaining design quality and impact. |

</details>

<details>
<summary><strong>diagrams & visualization</strong> (7)</summary>

| name | updated | what it does |
|---|---|---|
| ansanabria-skills-recharts | 2026-06-22 | Build composable, responsive React charts with Recharts library. Use when creating data visualizations including line charts, area charts, bar charts, pie charts, scatter plots, and composed charts. Handles chart customization, responsive sizing, tooltips, legends, axes configuration, performance optimization, and accessibility. |
| ckm:slides | 2026-04-26 | Create strategic HTML presentations with Chart.js, design tokens, responsive layouts, copywriting formulas, and contextual slide strategies. |
| cookbook-diagram | 2026-06-18 | Load the diagram cookbook skills on demand. Use when the user writes /cookbook-diagram or needs Mermaid, Excalidraw, or Draw.io diagram guidance. |
| diagram-excalidraw | 2026-05-17 | Create Excalidraw diagram JSON files that make visual arguments. Use when the user wants to visualize workflows, architectures, or concepts. |
| diagram-mermaid | 2026-06-18 | Create Mermaid diagrams using the cli-mermaid-agent CLI — generate from a natural-language prompt, validate with mmdc, repair syntax errors via the agent repair loop, render to SVG/PNG/PDF, and lint layout/style. Use when the user asks to draw a flowchart, sequence diagram, class/state diagram, or architecture/process visualization, or asks for a Mermaid file from a description. |
| notebooklm-infographic-generator | 2026-06-22 | Generate NotebookLM infographic image assets from required text input by creating a notebook, adding the text as a source, and downloading one or more infographic variants when users or other skills need visual assets from a written brief. Downloaded infographics are de-watermarked with cli-notebooklm-watermark-remover when that tool is available, with graceful fallback to the original images. |
| study-plan-generator | 2026-06-18 | Generate a structured study plan for any topic, tailored for senior software engineers. Produces a self-contained folder with a phased PLAN.md, curriculum breakdown, curated resources, project-based exercises, progress tracker, and diagrams (Mermaid roadmap + timeline, Excalidraw concept map). Uses skill@superpowers:brainstorming to interrogate the topic, skill@diagram-mermaid for flowcharts and gantt timelines, and skill@diagram-excalidraw for concept maps. Plans land in a configurable target directory (default ~/study-plans/<category>/<topic-slug>/), not in the agent-tools repo. Use when the user wants to learn a new topic deeply and asks for a study plan, learning roadmap, curriculum, or self-taught course outline. |

</details>

<details>
<summary><strong>engineering quality & debugging</strong> (32)</summary>

| name | updated | what it does |
|---|---|---|
| agent-teams-core | 2026-04-25 | Provide shared filesystem protocol helpers for local multi-agent team skills in tmux AI CLI mode, including task, message, role, heartbeat, recovery, and config operations. Use when the user needs shell-callable core operations, session-state debugging, or config migration support for agent-team workflows. |
| agent-tools-migration-doctor | 2026-05-31 | Manage adoption of the new agent-tools integration architecture across multiple Macs. Provides a six-step doctor flow — status, plan, exec, health, verify, report. Use when bringing a fresh Mac onto the integration engine, when validating an already-migrated Mac is converged, or when diagnosing why a Mac fails strict-idempotent. Wraps the existing `agent-tools` CLI; never invents new install logic. |
| ai-html-chat | 2026-06-25 | Open an agent-authored HTML artifact in a local browser for a human to review and annotate, then poll the annotations and layout warnings back — a human-in-the-loop review loop for HTML pages, reports, and mockups. |
| ai-repo-eval | 2026-06-23 | Evaluate a public AI-focused GitHub repo — security + architecture + adoption — and emit a single combined REPORT.md. Use when the user wants to decide whether (and how) to adopt a repo. Invoke as `skill@ai-repo-eval <github-url>`. |
| analyze-logs | 2026-04-25 | Analyze log files to identify patterns, anomalies, and potential issues. Use when user shares log content, mentions "logs", "log file", "analyze logs", or asks to debug application output. Provides reliability insights and actionable recommendations for general developers. |
| chrome-devtools-manager | 2026-06-24 | Control a Chrome browser session through the chrome-devtools-manager CLI — navigate, snapshot, click, fill forms, run JavaScript, inspect console and network, take screenshots, audit performance. Use whenever a task needs a real browser: opening or testing a web page, clicking through a flow, extracting page content, or debugging a website. |
| cli-anything | 2026-04-25 | Use when the user wants Codex to build, refine, test, or validate a CLI-Anything harness for a GUI application or source repository. Adapts the CLI-Anything methodology to Codex without changing the generated Python harness format. |
| code-refactor-backend-rust | 2026-04-25 | Refactor backend Rust files to team style using required file inputs, per-file pre-change summaries, confirmation-gated edits, and strict cargo check/clippy/test gates. |
| code-refactor-backend-ts | 2026-04-25 | Refactor backend TypeScript files to team style using required file inputs, per-file pre-change summaries, confirmation-gated edits, and strict zero lint/type issues. |
| command-creator-j | 2026-04-25 | Create and manage long-lived custom command snippets by refining natural-language requirements (via a prompt-optimizer skill) into slug files wired into the global commands index. |
| cookbook-engineering | 2026-05-31 | Load the engineering quality cookbook skills on demand. Use when the user writes /cookbook-engineering or needs rigorous debugging, TDD, code review, or production-hardening guidance. |
| critique | 2026-04-26 | Evaluate design effectiveness from a UX perspective. Assesses visual hierarchy, information architecture, emotional resonance, and overall design quality with actionable feedback. |
| deep-research | 2026-04-25 | Generate domain- and topic-specific deep-research prompt markdown files. Uses token-efficient lite template. Use when user wants a structured research prompt for architecture, strategy, policy, AI systems, security, economics, or any complex domain. Prompt is saved to output directory for copy/paste into an LLM. If result > 4900 chars, offers a trimmed version. |
| diagnose | 2026-05-29 | Disciplined diagnosis loop for hard bugs and performance regressions. Reproduce → minimise → hypothesise → instrument → fix → regression-test. Use when user says "diagnose this" / "debug this", reports a bug, says something is broken/throwing/failing, or describes a performance regression. |
| grill-with-docs | 2026-05-29 | Grilling session that challenges your plan against the existing domain model, sharpens terminology, and updates documentation (CONTEXT.md, ADRs) inline as decisions crystallise. Use when user wants to stress-test a plan against their project's language and documented decisions. |
| harden | 2026-04-26 | Improve interface resilience through better error handling, i18n support, text overflow handling, and edge case management. Makes interfaces robust and production-ready. |
| improve-codebase-architecture | 2026-05-29 | Find deepening opportunities in a codebase, informed by the domain language in CONTEXT.md and the decisions in docs/adr/. Use when the user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled modules, or make a codebase more testable and AI-navigable. |
| interview-debrief-coach | 2026-06-25 | Turn a recorded interview transcript into a reconciled clean transcript plus a hiring-manager-perspective coaching report rendered as a reviewable HTML artifact. Use when the user provides an interview/recruiter-screen transcript (optionally with a raw auto-transcribed version) and wants a debrief, scorecard, "what I did well / badly", before/after suggested lines, vocabulary to use next time, and lessons learned. Outputs are written into the directory the skill is run from and previewed for human review via skill@ai-html-chat. |
| linear-create-ticket | 2026-04-25 | Create Linear tickets from prompt, document, or markdown input with template selection and preview confirmation. Use when user wants to create Linear tickets from natural language, documents, or structured markdown (e.g., "create a ticket for implementing user authentication", "skill@linear-create-ticket"). Supports single tickets, multiple tickets, and tickets with sub-issues. Generates preview file for review before submission to Linear. |
| plan-software-architect | 2026-04-25 | Guide users through creating comprehensive, production-ready implementation plans by analyzing technical specifications, conducting iterative discovery through strategic multi-choice questions, and generating structured markdown implementation plans with clear milestones. Use when user wants to create an implementation plan from a technical specification, needs architectural guidance for a project, or requires a detailed plan with TDD approach and code samples. |
| ponytail-audit | 2026-06-18 | Whole-repo audit for over-engineering. Like ponytail-review, but scans the entire codebase instead of a diff: a ranked list of what to delete, simplify, or replace with stdlib/native equivalents. Use when the user says "audit this codebase", "audit for over-engineering", "what can I delete from this repo", "find bloat", "ponytail-audit", or "/ponytail-audit". One-shot report, does not apply fixes. |
| ponytail-review | 2026-06-18 | Code review focused exclusively on over-engineering. Finds what to delete: reinvented standard library, unneeded dependencies, speculative abstractions, dead flexibility. One line per finding: location, what to cut, what replaces it. Use when the user says "review for over-engineering", "what can we delete", "is this over-engineered", "simplify review", or invokes /ponytail-review. Complements correctness-focused review, this one only hunts complexity. |
| prompt-optimizer | 2026-05-17 | Improve LLM prompts using proven prompt engineering strategies. Use when user wants to refine a prompt, make instructions clearer, optimize for better AI responses, or apply prompt engineering best practices. |
| repo-agentic-debug | 2026-06-25 | Use to review whether a repo-agentic setup is working as expected. Runs the deterministic quick timeline (cli-repo-agentic-debug) and, with --deep, cross-checks it against .agents/, the rendered host files, and the manifest to judge drift, missing pillars, and failed or skipped steps. Triggered by /debug-repo-agentic-step. |
| repo-agentic-setup | 2026-06-25 | Use to set up a target repo for agentic development (the four pillars - skills, sub-agents, slash-commands, hooks - plus model routing), or to update/migrate an already-configured repo to the latest kits. Detects the stack, composes kits, diagnoses gaps, prescribes library + bespoke artifacts, populates .agents/ and the root AGENTS.md, then shells out to cli-repo-agentic-sync to dry-run and render to all hosts. Triggered by /repo-agentic-setup. |
| s-cli-anything | 2026-05-31 | On-demand loader for the cli-anything skill: build, refine, test, or validate a Python CLI harness that wraps a GUI app or source repo for agent use. |
| s-executing-plans | 2026-05-31 | On-demand loader for the executing-plans skill: work through a written implementation plan in a fresh session with TDD and review checkpoints. |
| s-prompt-optimizer | 2026-05-31 | On-demand loader for the prompt-optimizer skill: refines an LLM prompt using prompt-engineering best practices for clearer instructions and better responses. |
| s-superpower | 2026-05-31 | On-demand loader for the Superpowers framework: bootstraps it and kicks off the design to plan to TDD-implement lifecycle starting from brainstorming. |
| s-superpower-grill | 2026-05-31 | On-demand loader that combines the Superpowers planning discipline with grill-me for an adversarial, Superpowers-grade stress-test of a plan or design. |
| security-check | 2026-04-25 | Generate secure-by-design questions from design or component descriptions. Produces a prioritized set of security questions grouped by theme (Architecture, Authentication, etc.) to ensure projects are built with security in mind from the start. Use when reviewing designs, drafting security checklists, asking for secure-by-design questions, or evaluating system security at the design level. |
| superpower-grill | 2026-05-30 | Load the Superpowers planning discipline, then grill the user relentlessly about a plan or design until shared understanding is reached. Combines /s-superpower (Superpowers framework bootstrap) with skill@grill-me. Use when the user wants a Superpowers-grade, adversarial stress-test of a plan — "grill me with superpowers", "superpower grill", or invokes /s-superpower-grill. |

</details>

<details>
<summary><strong>git / PR / commit</strong> (29)</summary>

| name | updated | what it does |
|---|---|---|
| code-feature-scoped-commit-porter | 2026-04-25 | Creates feature-scoped local commits by porting changes from a newer commit range onto an older base with strict validation gates, optional feature map generation, and auditable phase-based reporting. |
| code-reviewer | 2026-04-25 | Perform comprehensive code reviews with severity-based prioritization. Use when the user wants code reviewed, shares code snippets or diffs, provides file paths for review, or shares GitHub URLs (PRs, files, folders). Supports local files, git diffs, inline code, and GitHub CLI (`gh`) integration for remote resources. |
| code-tutor | 2026-04-25 | Collaborate on code and PR reviews through priority-sorted lockstep discussion, changed-line coverage tracking, zero-unknown ship readiness gates, and no-edit refactor planning. Use when users want to understand and validate code before opening or approving PRs. |
| git-auto-commit | 2026-04-25 | Create a guarded local Git commit from staged changes by default, optionally include unstaged changes, and auto-generate a commit message when the user leaves it blank. Use when user wants Commit behavior with a required SUBMIT confirmation before committing. |
| git-auto-commit-and-push | 2026-04-25 | Create a guarded local Git commit and then push the current branch, using staged changes by default, optionally including unstaged changes, and auto-generating a commit message when blank. Use when user wants Commit & push behavior with a required SUBMIT confirmation before commit or push. |
| git-commit-message | 2026-04-25 | Generate conventional commit messages from staged Git changes. Automatically reads git diff --staged, analyzes changes, and produces a properly formatted commit message with title, body, and breaking change footer. Use when user wants to generate a commit message, needs help writing a commit, or asks for a summary of staged changes. |
| git-merge-ff | 2026-04-25 | Merge a target remote branch into the current local branch by defaulting to a temporary git worktree, resolving conflicts there, and fast-forwarding the original branch back only after success. Use when user invokes skill@git-merge-ff with an optional bare branch name such as main. |
| git-pr-create-apps-monorepo | 2026-04-25 | Create GitHub pull requests for a configured apps monorepo with automatic ticket extraction, base-branch detection, multi-component (apps/packages) detection, and a minimal structured description. |
| git-pr-create-plugin | 2026-04-25 | Create GitHub pull requests for a configured plugin repository with ticket extraction, base-branch detection, and PR-template population (Areas Affected, Verification). |
| git-pr-create-webapp | 2026-04-25 | Create GitHub pull requests for a configured web-app repository with automatic ticket-id extraction, base-branch detection, PR-template population, and preview confirmation. |
| git-pr-reviewer | 2026-04-25 | Review GitHub Pull Requests using GitHub CLI (`gh`). Creates local review files for collaborative editing before posting comments to GitHub. Use when user wants to review a PR, check code changes, or analyze pull request quality. |
| git-refactor-staged | 2026-04-25 | Detect git-staged changes and generate a production-grade refactor plan via a planning skill (reads `git diff --cached`, emits a PLAN-refactor file). |
| git-refactor-with-git | 2026-04-25 | Create production-grade refactor plans from git commit-range changes with semantic numbered refactor options and user multi-select flow. Supports start+end or start-only (end defaults to HEAD). |
| git-scoped-commits | 2026-04-25 | Create scoped commits in logical chunks for the current local git repo. Groups uncommitted changes by top-level directory, then commits each chunk via repo-local scripts/committer (when present) or git add + git commit. Use when user wants to commit working-tree changes in logical chunks. Local only—never push to remote. |
| git-ssh-signing-setup | 2026-06-26 | Configure SSH commit signing for GitHub repos on Macs with multiple GitHub SSH host aliases. Use when a repo should auto-sign commits using the same account identity implied by its origin SSH alias in ~/.ssh/config, or when setting up/revalidating this behavior across Agent Tools machines. |
| github-multi-account-doctor | 2026-05-11 | Use when reviewing, initializing, auditing, fixing, or diagnosing a Mac's multi-GitHub-account Git and SSH setup, especially when standardizing account-specific SSH aliases, per-account Git identity, and safe config updates without deleting existing SSH keys. |
| grill-me | 2026-05-29 | Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when user wants to stress-test a plan, get grilled on their design, or mentions "grill me". |
| linear-create-ticket-with-git | 2026-04-25 | Create Linear tickets from Git branch context with requirement-first narrative generation and preview confirmation. Use when user wants to create a Linear ticket based on current branch changes while making the ticket read like planned requirements rather than implementation logs. |
| linear-pr-comment-follow-up | 2026-04-25 | Create Linear tickets from GitHub PR comment links. Extracts comment content and PR context, then creates a follow-up Linear ticket using linear-create-ticket. After SUBMIT, posts the GitHub reply in the review discussion thread (in_reply_to) for |
| linear-solve | 2026-04-25 | Automate the Linear ticket workflow: fetch ticket details, create a properly-named git branch, and generate a PLAN file via a planning skill. Use to start work on a ticket by id. |
| linear-ticket-and-pr | 2026-06-03 | Create a Linear ticket AND a GitHub pull request for the current branch in one SUBMIT-gated workflow, then cross-link them both directions. Reuses a ticket-drafting skill and delegates PR creation. |
| local-pr-review | 2026-05-21 | Run a local, read-only review of a GitHub PR from its URL, producing a Markdown report without posting comments, mutating checkouts, or any remote writes. Reach for it to assess a PR safely before deciding whether to act. |
| openclaw-local-deployment | 2026-03-09 | Deploys OpenClaw from local source via pnpm build + ui:build and install (no reconfig by default); optional test; use --skip-test when invoking deploy.sh to avoid prompts. Safety checks for clean git status and repo presence. |
| prototype | 2026-05-29 | Build a throwaway prototype to flesh out a design before committing to it. Routes between two branches — a runnable terminal app for state/business-logic questions, or several radically different UI variations toggleable from one route. Use when the user wants to prototype, sanity-check a data model or state machine, mock up a UI, explore design options, or says "prototype this", "let me play with it", "try a few designs". |
| s-grill-me | 2026-05-31 | On-demand loader for the grill-me skill: relentlessly interviews you about a plan or design, resolving each decision branch until shared understanding is reached. |
| skill-creator-j | 2026-06-23 | Create and update agent skills programmatically with natural-language input parsing, interactive prompting, and automatic validation. Use to create a new skill (e.g., 'create a skill for PDF processing') or update an existing one. |
| skill-delegate-shell-function | 2026-05-03 | Create new skill-delegate-powered shell functions following the ai-git-auto-commit pattern. Use when adding a new AI utility shell function that wraps skill-delegate, needs multi-step orchestration (stage, generate, commit), or requires option flags like --review and --push. skill-delegate-aliases.zsh is the central registry for all ai-* functions — simple pass-through wrappers and complex custom bodies both live there. |
| skill-library | 2026-05-02 | Resolves `skill@<name>` references that are not in the active session: loads the archived skill from the on-demand library and follows it inline. The dynamic skill-loading backbone. |
| yesterday-linear-gh-cutoff | 2026-04-25 | Summarize the prior calendar day's Linear activity for the authenticated viewer and GitHub commits by the configured author; show a short bullet list and require an explicit cutoff before finalizing the narrative. |

</details>

<details>
<summary><strong>misc / utility</strong> (7)</summary>

| name | updated | what it does |
|---|---|---|
| ai-request-duration-tracker | 2026-04-25 | Track and report request/response timing for each conversation request with a Time Tracking Summary. Use when users want per-request timing, especially for large tasks. |
| code-index-knowledge | 2026-04-25 | Generate hierarchical AGENTS.md knowledge bases for code-focused repositories, including a root file and complexity-scored subdirectory documentation. Use when asked to create or update AGENTS.md files, knowledge bases, or codebase indexing documentation. |
| code-repo-rules-to-mdc | 2026-04-25 | Analyze local or GitHub repositories to extract explicit and inferred best-practice rules and generate consolidated/split .mdc files plus a separate RULE_EVIDENCE_REPORT.md with citations. Use when users request AI IDE rule extraction for Cursor or Antigravity. |
| crawler-medium-to-markdown | 2026-04-25 | Convert one or more Medium article URLs into Markdown files via a local converter, writing outputs locally and returning a summary of file paths and errors. |
| delight | 2026-04-26 | Add moments of joy, personality, and unexpected touches that make interfaces memorable and enjoyable to use. Elevates functional to delightful. |
| openclaw-model-switch | 2026-03-09 | Switch OpenClaw session gateway provider/model/thinking by direct target or numbered selection. |
| safe-extract | 2026-06-22 | Advisory wrapper around the cli-safe-extract tool. Use when the user wants to safely extract an untrusted archive (zip/tar/7z/rar/etc.): inspect it in an isolated sandbox, read the JSON manifest, and recommend which files are safe to promote with reasoning. Drives `cli-safe-extract inspect` and `promote`; can auto-promote the SAFE tier with --auto. Cannot override the engine's HARD BLOCK rules (zip-slip, escaping symlinks, scan hits) — those are enforced in deterministic code. |

</details>

<details>
<summary><strong>planning / research / prompts</strong> (4)</summary>

| name | updated | what it does |
|---|---|---|
| d-session | 2026-04-25 | Initialize delegation sessions and route explicit prompts through agent-delegate using /d-session syntax. Use when users invoke skill@d-session or /d-session. |
| plan-master | 2026-05-29 | Transform user task descriptions into comprehensive engineering plans following a structured PLAN-<slug>.md format. Use when user wants to create a detailed engineering plan from a task description, needs to break down complex tasks into actionable steps, or requires a production-grade plan document. |
| reverse-engineer-prompt | 2026-04-25 | Analyzes multi-turn conversations and reconstructs a single, self-contained prompt that would generate the final response in one interaction; supports saving markdown output with versioned filenames. |
| skill-creator-j-repo | 2026-06-23 | Create repo-local agent skills under ./.agents/skills by wrapping skill-creator-j with repo-aware prompts, explicit output paths, and repo-local ./.claude/skills symlinks for Claude Code. Use when user wants a new skill created inside the current repository instead of a home-directory skills folder. |

</details>

<details>
<summary><strong>productivity</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| work-ledger-init | 2026-04-25 | Initialize a machine for work-ledger auto-finalize and optional auto-submit to a shared ledger repo, with verification steps suitable for repeating across machines. |

</details>

<details>
<summary><strong>repo-agentic / infra tooling</strong> (6)</summary>

| name | updated | what it does |
|---|---|---|
| ai-dir-init | 2026-04-25 | Creates standard per-directory AGENTS.md files for a target repo directory, supporting single-target initialization and guided --all multi-directory selection for monorepos. |
| ai-dir-sync | 2026-04-25 | Synchronize one project-local AI directory (.codex, .cursor, .claude, or .antigravity) to the other AI directories with a dry-run-first workflow, source-precedence conflict resolution, symlink preservation, and target-only file retention. Use when users ask to mirror or update AI tool directories inside the current repository. |
| gitnexus-doctor | 2026-05-29 | Use when checking, initializing, refreshing, or troubleshooting GitNexus indexing for a repository, especially when mcp-router is the single active MCP server or a repo needs GitNexus analyze/status/list validation. |
| mcp-router-hard-reset | 2026-04-25 | Hard reset mcp-router broker and session state by deleting the broker runtime directory (sockets, PID, pooled downstream state). Use when stale brokers, stuck sessions, or corrupted IPC require a clean runtime after confirming the active config path. |
| opencode-plugin-manager | 2026-04-25 | Manage OpenCode plugins with cli-opencode-manager plugin, including doctor/status checks and add, update, or delete plugin configuration. Use when user asks to inspect plugin health, add a supported plugin, refresh plugin bootstrap config, or remove an OpenCode plugin. |
| ponytail-debt | 2026-06-18 | Harvest every `ponytail:` comment in the codebase into a debt ledger, so the deliberate shortcuts and deferrals ponytail leaves behind get tracked instead of rotting into "later means never". Use when the user says "ponytail debt", "/ponytail-debt", "what did ponytail defer", "list the shortcuts", "ponytail ledger", or "what did we mark to do later". One-shot report, changes nothing. |

</details>

<details>
<summary><strong>resume toolkit</strong> (10)</summary>

| name | updated | what it does |
|---|---|---|
| agent-team-coder | 2026-04-25 | Execute coder-role workflow for local multi-agent coordination in tmux AI CLI mode, with assigned-worktree implementation, recovery handling, messaging, and handoff continuity. Use when the user asks the coder role to register or resume, implement assigned tasks, validate worktree context, or request/apply recovery guidance. |
| agent-team-planner | 2026-04-25 | Handle planner-role workflow for local multi-agent coordination in tmux AI CLI mode, including registration, planning artifacts, messaging, and continuity updates. Use when the user asks the planner role to register or resume, pick assigned planning tasks, or produce planning deliverables. |
| agent-team-reviewer | 2026-04-25 | Perform reviewer-role workflow for local multi-agent coordination in tmux AI CLI mode, with findings-first review, messaging, and continuity-safe reporting. Use when the user asks the reviewer role to register or resume, review assigned outputs, or publish structured review findings and recommendations. |
| agent-team-tester | 2026-04-25 | Run tester-role workflow for local multi-agent coordination in tmux AI CLI mode, including assigned-task validation, bug verification, messaging, and reporting outputs. Use when the user asks the tester role to register or resume, execute verification tasks, or produce regression and defect reports. |
| cookbook-resume | 2026-05-31 | Load the resume toolkit cookbook skills on demand. Use when the user writes /cookbook-resume or needs resume diagnosis, rewriting, tailoring, or multi-perspective scoring. |
| resume-diagnoser | 2026-05-29 | Diagnose a resume beyond surface-level review. Scans the resume the way an Applicant Tracking System (ATS) and senior reviewer would, flagging vague phrasing, missing quantification, weak verbs, formatting that breaks parsers, role/responsibility/impact gaps, and unclear seniority signals. Produces a section-by-section critique with the exact issues found and specific instructions to fix them. Use when the user wants to audit a resume, find weaknesses, identify what is missing, or check ATS-readability before applying. |
| resume-hiring-manager | 2026-05-20 | Act as a hiring manager for the user's target role and conduct a final review plus lifelike interview. Reviews the resume through a hiring manager's lens (leadership, team impact, scope of ownership, business outcomes, seniority calibration), then runs a mock interview with the hardest technical and behavioral questions in the field, rates each answer 0-10 with specific feedback, and ends with a hire/no-hire verdict plus the gaps the candidate must close. Use when the user wants a hiring-manager review, interview prep, mock interview, leadership/impact assessment, or a hire/no-hire verdict. |
| resume-panel | 2026-05-29 | Run a full multi-persona hiring panel over a resume against one exact role/JD, then rewrite the weak parts. Four reviewers in one pass — ATS scanner, recruiter, hiring manager, and a domain Staff/Senior peer — each producing an independent match score (ATS /100, Recruiter /100, Hiring Manager /100). Then synthesizes the panel into top missing keywords, strengths, weaknesses, 10-second red flags, and skills to emphasize vs de-emphasize, and finally rewrites only the sections that need it using the Google XYZ formula — ATS-optimized, human-readable, truthful, no fluff. Use when the user wants the whole gauntlet at once (score + diagnose + HM review + rewrite) for a specific job, not a single-lens pass. |
| resume-recruiter-scorer | 2026-05-29 | Score a resume the way a recruiter would using the find/attract/engage/hire lens. Compares the resume to typical job descriptions in the user's stated field (or against a provided JD/role), extracts the top keywords, skills, and signals recruiters search for, scores the resume against them (0-100 with subscores per lens), and lists the missing keywords/competencies plus a prioritized fix list. Use when the user wants a recruiter-style scorecard, keyword-gap analysis, JD match score, or to know whether a recruiter would shortlist them. |
| resume-rewriter-xyz | 2026-05-20 | Rewrite resume bullets using the Google XYZ formula 'Accomplished [X] as measured by [Y], by doing [Z]'. Forces quantification of impact, surfaces missing metrics by asking targeted follow-up questions, applies patterns used by candidates landing roles at Meta, Google, and Fortune 500 companies, and returns before/after comparisons per bullet with the X/Y/Z components labeled. Use when the user wants to rewrite, strengthen, quantify, or punch up resume bullets/experience entries. |

</details>

<details>
<summary><strong>session / interaction / logs</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| caveman | 2026-05-29 | Ultra-compressed communication mode. Cuts token usage ~75% by dropping filler, articles, and pleasantries while keeping full technical accuracy. Use when user says "caveman mode", "talk like caveman", "use caveman", "less tokens", "be brief", or invokes /caveman. |

</details>

<details>
<summary><strong>writing / content</strong> (26)</summary>

| name | updated | what it does |
|---|---|---|
| adapt | 2026-04-26 | Adapt designs to work across different screen sizes, devices, contexts, or platforms. Ensures consistent experience across varied environments. |
| ai-handover | 2026-05-29 | Summarize AI agent conversations for handoff to another AI agent in a new session. Creates structured summaries with context, decisions, tasks, discoveries, technical details, metrics, and sentiment analysis. Use when user wants to summarize current chat session, create handoff notes, capture conversation context for continuation, or prepare session summary. |
| ai-handover-prompt | 2026-06-28 | Generate a tight, copy-pasteable next-session bootstrap prompt (5-12 lines) that triggers the next planned task immediately in a fresh Claude Code session, with just-enough context and no recap noise. Use when the user wants a quick trigger prompt for the next task, a session bootstrap, a "drop this into the next session" prompt, or says "give me a prompt to start the next task". Companion to ai-handover (full 9-section record); this produces a single focused action prompt. |
| ai-result-rating | 2026-04-25 | Evaluate AI output quality on a 1-100 scale with education-level equivalents. Analyzes AI responses against prompts and original content, providing detailed scores, deductions, and improvement suggestions. Use when you need to assess how well an AI performed a task, compare AI outputs, or identify areas for prompt improvement. |
| ai-result-rating-lite | 2026-04-25 | Rate AI-generated outputs on a letter grade scale (A+ to F) with justifications and numerical score. Use when user wants to evaluate AI response quality, compare AI output to expert-level work, get structured feedback on AI-generated content, or assess how well an AI performed a task. |
| ckm:brand | 2026-04-26 | Brand voice, visual identity, messaging frameworks, asset management, brand consistency. Activate for branded content, tone of voice, marketing assets, brand compliance, style guides. |
| clarify | 2026-04-26 | Improve unclear UX copy, error messages, microcopy, labels, and instructions. Makes interfaces easier to understand and use. |
| cli-anything-agent-tools | 2026-06-23 | Create or refine a CLI-Anything-derived CLI following repo conventions for layout, Python version, env vars, packaging, TOON output, and tests. |
| colorize | 2026-04-26 | Add strategic color to features that are too monochromatic or lack visual interest. Makes interfaces more engaging and expressive. |
| cookbook-content | 2026-05-31 | On-demand loader that pulls the core writing skills (writing-skills, text-refiner, text-humanizer) plus task-conditional ones for slides, brand voice, UX microcopy, LinkedIn posts, and research prompts. |
| cookbook-design-craft | 2026-05-31 | Load the design-craft cookbook skills on demand. Use when the user writes /cookbook-design-craft or asks for design craft guidance. |
| debate-analyzer | 2026-04-25 | Analyze debates and discussions to identify primary disagreements, extract arguments from each party, detect cognitive biases, and predict outcomes. Use when given debate transcripts, discussion threads, or argumentative content requiring structured analysis. |
| distill | 2026-04-26 | Strip designs to their essence by removing unnecessary complexity. Great design is simple, powerful, and clean. |
| intent-layer | 2026-05-30 | Set up hierarchical Intent Layer (AGENTS.md files) for codebases. Use when initializing a new project, adding context infrastructure to an existing repo, user asks to set up AGENTS.md, add intent layer, make agents understand the codebase, or scaffolding AI-friendly project documentation. |
| linkedin-post-engineer | 2026-06-25 | Create production-ready LinkedIn posts for engineering audiences by collecting missing context one question at a time, researching X.com hot topics when needed, and applying a layered Web2.5 plus master style framework with mandatory skill@text-humanizer final pass. |
| normalize | 2026-04-26 | Audit a page, route, or feature against the project's design system and redesign it to match established tokens, components, and UX patterns, fixing one-off implementations and inconsistencies. |
| polish | 2026-04-26 | Final pre-ship quality pass that hunts the small details separating good from great: visual inconsistencies, spacing and alignment, interaction-state gaps, copy, and edge/error states. |
| question-widget | 2026-05-26 | Re-ask the most recent clarifying question using the host's native interactive question widget instead of plaintext A/B/C/D menus. Use when the user triggers `skill@question-widget` (typically after the agent just emitted a plaintext multiple-choice question), or any time a structured/multiple-choice question is about to be asked on a host that exposes a native question UI (Claude Code `AskUserQuestion`, OpenCode `question`, Codex structured question tool, Gemini `ask_user`). |
| s-grill-with-docs | 2026-05-31 | On-demand loader for the grill-with-docs skill: stress-tests a plan against the project's domain model and docs, sharpens terminology, and updates CONTEXT.md/ADRs inline. |
| s-takeover | 2026-05-31 | Resolve and ingest a previous session from another tool. Use when the user writes /s-takeover, /takeover, or runs /use s-takeover. |
| s-text-humanizer | 2026-05-31 | On-demand loader for the text-humanizer skill: run cli-skill-library load text-humanizer and follow it inline. Use to rewrite AI-generated text to sound naturally human. |
| sub-agent-library | 2026-04-28 | MANDATORY when the user writes `subagent@<name>` for any name that is not in the active sub-agent list. Resolves the host-appropriate flavor (cc on Claude Code, oc on OpenCode/Codex), runs `cli-sub-agent-library load <name>@<flavor>`, and dispatches the persona via the host's native sub-agent mechanism (or inline fallback). |
| teach-impeccable | 2026-04-26 | One-time project setup that scans the codebase, asks UX/brand/aesthetic questions for what it can't infer, and persists the gathered design guidelines to your AI config file so future sessions share consistent design context. |
| text-humanizer | 2026-05-17 | Transform AI-generated text into natural, human-sounding writing. Use when user wants to humanize AI output, make text sound more conversational, or reduce AI-detectable patterns in writing. Preserves meaning while improving authenticity and readability. |
| text-refiner | 2026-04-25 | Refine and improve text for clarity, coherence, grammar, and style. Use when user wants to improve their writing, fix grammar issues, enhance clarity, or adjust tone and style of text. Prompts for preferences before refining and optionally shows what changed. |
| to-prd | 2026-06-02 | Turn the current conversation context into a PRD and publish it to the project issue tracker. Use when user wants to create a PRD from the current context. |

</details>

### sub-agent

<details>
<summary><strong>delegation / coordination</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| btw-side | 2026-04-25 | Side-channel quick-answer agent for quick questions: forks an existing session's context to answer without tools and without polluting the main transcript. |

</details>

<details>
<summary><strong>planning / strategy / advisory</strong> (3)</summary>

| name | updated | what it does |
|---|---|---|
| plan-master | 2026-05-29 | Engineering planning agent. Creates structured PLAN-<slug>.md implementation plans using the plan-master skill. Always runs on Opus to guarantee maximum planning quality and codebase reasoning. |
| strategic-partner | 2026-05-21 | High-level strategic thinking partner. Use when a request needs challenge, stress-testing, trade-off analysis, and decision-quality guidance before execution. |
| strategic-partner-unlock | 2026-05-21 | High-level strategic thinking partner with unrestricted tool access. Use when a request needs challenge, stress-testing, trade-off analysis, and decision-quality guidance with full environment access. |

</details>

<details>
<summary><strong>review / quality / security</strong> (4)</summary>

| name | updated | what it does |
|---|---|---|
| cli-developer | 2026-06-25 | Language-agnostic CLI/TUI engineer. Designs commands, flags and subcommands (POSIX/GNU), help/usage text, exit-code contracts, stdout=data / stderr=diagnostics separation, pipe and streaming friendliness, TTY/NO_COLOR-aware output, machine-readable --json, shell completions, and packaging. Use for command-line tool feature work and UX review. |
| code-reviewer | 2026-04-28 | Reviews code changes for bugs first (logic errors, edge cases, security), then fit with codebase patterns; reads as a quality gate before merge. |
| oracle | 2026-04-28 | Principal engineering advisor for deep code reviews, architecture decisions, complex debugging, and planning. Delegates to a high-reasoning model for maximum depth. Prompt with a precise problem plus files; ask for concrete outcomes. |
| parallel-manager | 2026-05-21 | Primary coordination wrapper for same-repo parallel work. Apply worktree and lock policy first, then delegate to the best specialist agent for planning, implementation, review, or deep technical analysis. |

</details>

### cli

<details>
<summary><strong>ai / agent orchestration</strong> (15)</summary>

| name | updated | what it does |
|---|---|---|
| cli-agent-delegate | 2026-06-29 | Delegates a prompt from a lightweight orchestrator model to a larger execution model via an external agent binary, with model/preset selection, health checks, and an MCP bridge. |
| cli-agent-parallel-manager | 2026-06-29 | Coordinates parallel local agents on one git repo via per-task git worktrees and on-disk file locks for shared resources (dev server, db, ports), keeping all state on one machine. |
| cli-ai-crew | 2026-06-28 | Harness-agnostic agent session bus: push prompts into labelled Claude/Codex worker sessions and tail their transcripts back for result + token usage. |
| cli-ai-git-auto | 2026-06-27 | Non-interactive AI git automation (commit/merge/push) on top of cli-codex |
| cli-ai-html-chat | 2026-06-28 | Open an agent-authored HTML artifact in a local browser for a human to review and annotate, then poll the annotations and layout warnings back — a human-in-the-loop review loop for HTML pages, reports, and mockups. |
| cli-ai-usage | 2026-06-27 | Cron-safe AI provider usage tracker for Codex, Claude, Cursor, Gemini |
| cli-claude-opencode-bridge | 2026-05-26 | Local OpenAI-compatible bridge from OpenCode to Claude CLI |
| cli-cmux-manage | 2026-06-29 | Manages the lifecycle (setup, remove, doctor, test) of the OpenCode notification plugin with deterministic, repeatable commands. |
| cli-codex | 2026-06-29 | One-shot delegator to the codex exec binary: runs a single prompt headlessly, optionally routed through the local VPN proxy. |
| cli-cursor-agent | 2026-06-26 | CLI-Anything one-shot delegator to the Cursor `agent` binary (model pinned to auto) |
| cli-opencode-manager | 2026-06-29 | Umbrella CLI for OpenCode operations: manage OpenAI/Ollama providers, permissions, plugins, and sessions from one command. |
| cli-skill-delegate | 2026-06-24 | Delegate prompts to agent-tools skills through cli-agent-delegate |
| cli-slack | 2026-06-29 | Multi-workspace, OAuth-backed Slack CLI: send/read/search messages, threads, users, channels, and canvases, with automatic token refresh — replaces the Slack MCP connector. |
| cli-takeover | 2026-06-29 | lets an active AI agent resume a stalled session from another coding app (Claude Code, Codex, OpenCode, desktop apps) by reading only local on-disk transcripts and stores |
| cli-workspace-manager | 2026-06-29 | Orchestrate a crew of AI coding agents: a single point of contact that spawns, supervises, and tears down worker agents across projects via a workspace CLI — never doing the work itself. |

</details>

<details>
<summary><strong>ci / devops</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| cli-staging-logs | 2026-06-29 | CLI-Anything harness for staging log lookup by request id. |

</details>

<details>
<summary><strong>data / extraction</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| cli-receipt-parser | 2026-06-29 | Install wrapper for a native Swift CLI that extracts structured fields from scanned receipts. |

</details>

<details>
<summary><strong>data / scraping</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| cli-image-crawler | 2026-06-29 | CLI-Anything harness for crawling product color-option images from an e-commerce site. |
| cli-inventory-manager | 2026-06-29 | CLI-Anything harness for an inventory session with filters. |

</details>

<details>
<summary><strong>diagram / media / render</strong> (8)</summary>

| name | updated | what it does |
|---|---|---|
| cli-cf-page-manager | 2026-06-29 | Deploys a static directory or single HTML file to Cloudflare Pages and manages projects and custom domains, wrapping the wrangler CLI. |
| cli-chrome-devtools-manager | 2026-06-29 | An agent-friendly CLI wrapping a Chrome DevTools browser-automation server, emitting compact, token-efficient output with stable element references for reliable automation. |
| cli-excalidraw | 2026-06-29 | Renders Excalidraw (.excalidraw JSON) drawings to PNG and SVG headlessly via a bundled browser engine. |
| cli-figma | 2026-06-29 | Stateful CLI over the Figma API with multi-account (per-email) token storage: list projects/files/versions/components and fetch file metadata, emitting TOON for agents. |
| cli-macdown | 2026-06-29 | Automates MacDown windows from the command line: open a Markdown file, clear all windows, or atomically clear-then-open, with TOON output. |
| cli-mermaid-agent | 2026-06-24 | Validate, repair, render, and lint AI-generated Mermaid diagrams via a wrapped mmdc. |
| cli-stitch | 2026-06-24 | Pure CLI for Google Stitch over direct MCP HTTP |
| cli-typora | 2026-06-29 | opens markdown files in the Typora app and manages its windows (open, clear all, or atomic clear-then-open) via AppleScript |

</details>

<details>
<summary><strong>doc / OCR / conversion</strong> (5)</summary>

| name | updated | what it does |
|---|---|---|
| cli-markitdown-ocr-llm | 2026-06-29 | Converts documents to Markdown with LLM-powered OCR via MarkItDown, checking provider setup first and supporting pluggable hosted or local vision-model providers. |
| cli-notebooklm | 2026-06-29 | Agent-first wrapper over the native NotebookLM CLI that applies reusable, attributed prompt-style presets to generate styled slide decks and infographics; everything but generation runs offline. |
| cli-notebooklm-py | 2026-05-12 | Unofficial Python library for automating Google NotebookLM |
| cli-notebooklm-watermark-remover | 2026-06-29 | CLI wrapper that removes the bottom-right NotebookLM watermark from PDFs, PPTX decks, and images you own, orchestrating a pinned third-party remover in an isolated venv with no CV deps of its own. |
| cli-safe-extract | 2026-06-24 | Two-phase, default-deny safe archive extraction (inspect → manifest → promote) |

</details>

<details>
<summary><strong>git / dev workflow</strong> (5)</summary>

| name | updated | what it does |
|---|---|---|
| cli-aliases | 2026-06-29 | CLI-Anything central shell-alias manager for the toolkit: register, list, and sync command shortcuts. |
| cli-git-smart | 2026-06-26 | Smart multi-account git clone: rewrite SSH host to per-account ssh-config alias |
| cli-gnhf | 2026-06-29 | An agent-first CLI that runs an AI coding agent in an unattended commit-per-iteration git loop until a goal or limit is met, with quota-aware tiers deciding when to pause, resume, or stop. |
| cli-local-pr-review | 2026-06-23 | Local-first PR review orchestration with GitNexus indexes |
| cli-worktree-manager | 2026-06-29 | Terminal CLI for managing isolated git worktrees: create, list, switch between, and tear down working trees (vendored from source, third-party telemetry stripped). |

</details>

<details>
<summary><strong>network / vpn</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| cli-full-vpn-wrapper | 2026-06-27 | CLI-Anything wrapper that runs agent CLIs through a dedicated local VPN/proxy relay (TLS relay plus multiple transport protocols). |

</details>

<details>
<summary><strong>productivity</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| cli-work-ledger | 2026-06-29 | CLI-Anything harness for recording and finalizing per-session work receipts to a shared ledger. |

</details>

<details>
<summary><strong>productivity / SaaS</strong> (4)</summary>

| name | updated | what it does |
|---|---|---|
| cli-context7 | 2026-06-29 | REPL-first CLI over the Context7 docs API: search libraries, fetch documentation context, and request doc uploads/refreshes, emitting machine-readable TOON for agents. |
| cli-linear | 2026-06-29 | Stateful CLI over the Linear GraphQL API: list/create/update issues, move workflow states, assign, and set priority, with undo/redo and TOON output for agents. |
| cli-obsidian | 2026-06-29 | Safe local Obsidian vault CLI: list, read, and search notes deterministically, with confirmation-gated writes, undo/redo, and TOON output for agents. |
| cli-reminders | 2026-06-29 | Command-driven CLI for Apple Reminders: list lists/items, show due-today, full reminder CRUD, complete/flag state changes, and session undo/redo. |

</details>

<details>
<summary><strong>skill / agent infra</strong> (7)</summary>

| name | updated | what it does |
|---|---|---|
| cli-_shared | 2026-06-25 | Shared Click primitives for cli-anything-agent-tools CLIs. |
| cli-agent-tools-library | 2026-06-24 | Unified search across the sub-agent and skill libraries via subprocess delegation. |
| cli-hooks-library | 2026-06-29 | Browse and install curated git/agent hooks from the hooks library into a target repo, with provenance stamping and a per-machine opt-in. |
| cli-repo-agentic-debug | 2026-06-25 | Review what a repo-agentic setup did, from the harness session log |
| cli-repo-agentic-sync | 2026-06-25 | Deterministic renderer: project .agents/ into per-host views (repo-agentic-setup) |
| cli-skill-library | 2026-06-29 | Browse and load on-demand skills from the skill library — the fallback that resolves skill references not present in the active session. |
| cli-sub-agent-library | 2026-06-29 | Browse and load on-demand sub-agent personas from the sub-agent library, dispatching the archived persona when not live. |

</details>

### hook

<details>
<summary><strong>build check</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| build-check-on-stop | 2026-06-25 | Run cargo check / go vet + go build at turn end if configured; report errors, never block. |

</details>

<details>
<summary><strong>format / lint</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| format-on-edit | 2026-06-25 | Format the changed file with the project's configured formatter (prettier/ruff/gofmt/rustfmt); no-op if none is installed. |

</details>

<details>
<summary><strong>secrets (blocking)</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| block-secrets | 2026-06-25 | Block writes to .env / secret-bearing files or content; the only blocking hook. |

</details>

<details>
<summary><strong>typecheck</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| typecheck-on-stop | 2026-06-25 | Run tsc --noEmit / mypy (or pyright) at turn end if configured; report type errors, never block. |

</details>

### kit

<details>
<summary><strong>base</strong> (4)</summary>

| name | updated | what it does |
|---|---|---|
| Go (backend) | 2026-06-29 | Configures an AI-assisted Go backend development profile: TDD and debugging skills, architecture and review agents, format/lint/build hooks, and stack diagnostics. |
| Node / TypeScript (backend) | 2026-06-29 | Detects backend Node/TypeScript projects and provisions a tailored agent toolkit: refactor/TDD/debug skills, architect and reviewer agents, format/secret/typecheck hooks, slash commands, and gap diagnostics. |
| Python (backend) | 2026-06-29 | Detects Python backend projects and provisions a tailored agentic toolchain: TDD/debug skills, architecture and review agents, lint/typecheck/secret hooks, and gap diagnostics. |
| Rust (backend) | 2026-06-29 | A configuration profile that auto-detects a Rust backend project and provisions matching AI coding agents, skills, commands, format/build hooks, and task-routing rules. |

</details>

<details>
<summary><strong>overlay</strong> (3)</summary>

| name | updated | what it does |
|---|---|---|
| CLI tool | 2026-06-29 | Detects command-line tools and layers in CLI craftsmanship: a UX specialist agent, help-text and exit-code contracts, pipeable stdout/stderr, shell completions, and golden smoke tests. |
| Data / ML | 2026-06-29 | Detects data/ML projects and adds specialized agents, commands, and guardrails for reproducibility, leakage prevention, experiment tracking, schema validation, and pipeline design. |
| Frontend — React / Next.js | 2026-06-29 | A composable frontend overlay layering React/Next.js skills, UI-design tooling, browser-based human review, and stack-aware diagnostics onto any base setup. |

</details>

### host

<details>
<summary><strong>agent CLI drivers</strong> (7)</summary>

| name | updated | what it does |
|---|---|---|
| claude | 2026-06-29 | Host adapter for Claude Code: declares how setup installs agents, skills, commands, settings, and hooks into its config home, with per-agent model tiers. |
| codex | 2026-06-29 | Host adapter for Codex: declares how agents, skills, commands, and plugins install into its config home, with prose-degraded hooks and advisory model tiers. |
| cursor | 2026-06-29 | Host adapter for Cursor: declares how rules, skills, agents, commands, and hooks install into its config home; excluded from model routing (auto-model). |
| gemini | 2026-06-29 | Host adapter for Gemini CLI / Antigravity: declares how agents, skills, and commands install into its config home, with advisory model tiers and no hook support. |
| opencode | 2026-06-29 | Host adapter for OpenCode: declares how agents, skills, commands, plugins, and hooks install into its config home, with per-agent model tiers and plugin-based hooks. |
| rtk | 2026-06-29 | Vendors install and integration artifacts that wire a token-saving shell-command proxy into multiple AI coding agents, rewriting commands to cut LLM token usage. |
| shell | 2026-06-29 | Host target for the shell PATH: declares install scopes for binaries, shell completions, and manpages so CLIs and helpers land on PATH. |

</details>

<details>
<summary><strong>cross-cutting (routing / gate)</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| global | 2026-06-29 | Defines shared, cross-tool governance and default behaviors for AI coding agents: install policy, push/PR consent gates, delegation, coding standards, and prompt rules. |
| no-mistakes | 2026-06-29 | Centrally version-controlled config for an AI-agent-driven validation gate that runs review, tests, lint, docs, and CI before code reaches its push target. |

</details>

<details>
<summary><strong>host</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| agent-multiplexer | 2026-06-29 | Terminal-based AI-agent multiplexer host. |
| worktree-manager | 2026-06-29 | Git-worktree manager integrated as a host (vendored from source, telemetry stripped). |

</details>

<details>
<summary><strong>integration / tool pin</strong> (3)</summary>

| name | updated | what it does |
|---|---|---|
| ai-crew | 2026-06-29 | A loopback-only daemon that orchestrates labelled AI coding-agent sessions: routing prompts to workers, tailing transcripts, and returning results and tokens. |
| chrome-devtools-manager | 2026-06-29 | Pins and installs an agent-friendly CLI that drives a real Chrome browser via the DevTools protocol with token-efficient output for web automation. |
| openclaw | 2026-06-29 | Host adapter for OpenClaw: declares how agents, skills, and commands install into its config home via symlink or copy. |

</details>

### integration

<details>
<summary><strong>agent frameworks (vendored)</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| oh-my-openagent | 2026-06-29 | opt-in integration that vendors a pinned third-party agent-skill and command bundle plus its plugin into OpenCode, registering it and verifying the runtime after install |
| superpowers-framework | 2026-06-29 | vendors a pinned upstream skill and slash-command framework into OpenCode by mirroring its skills and commands; Claude is excluded since it installs the same framework via its own plugin |

</details>

<details>
<summary><strong>first-party core</strong> (5)</summary>

| name | updated | what it does |
|---|---|---|
| agents-md-core | 2026-06-29 | symlinks the canonical AGENTS.md operating doctrine into every supported agent CLI's home directory so all hosts share one set of instructions |
| commands-core | 2026-06-29 | mirrors the repo's first-party slash-command tree into the command-aware agent CLI homes (Claude, Codex) so the same commands are available everywhere |
| jq | 2026-04-25 | jq — command-line JSON processor |
| skills-core | 2026-06-29 | mirrors the repo's first-party skills tree into the skill-aware agent CLI homes (Claude, Codex, Gemini, OpenCode, openclaw) so every host shares the same skills |
| sub-agents-core | 2026-06-29 | symlinks the first-party sub-agent definitions into each host's agents directory — Claude gets the rendered tree, Codex the source tree |

</details>

<details>
<summary><strong>migrated vendor packages</strong> (3)</summary>

| name | updated | what it does |
|---|---|---|
| vendor-agent-agency-agents | 2026-06-29 | vendors a pinned third-party collection of role-based AI sub-agent personas (engineering, product, testing, design, project management) into the Claude and Codex sub-agent trees |
| vendor-cli-notebooklm-py | 2026-06-29 | vendors a pinned third-party Python NotebookLM client library so its CLI can be installed and run locally from a fixed upstream ref |
| vendor-skill-cli-anything | 2026-06-29 | vendors the pinned CLI-Anything skill from its upstream repo into every supported agent CLI home (Claude, Codex, Cursor, Gemini, OpenCode, openclaw) |

</details>

### schema

<details>
<summary><strong>schema</strong> (6)</summary>

| name | updated | what it does |
|---|---|---|
| agent-tools-index catalog | 2026-06-29 | Defines the validation contract for a catalog of agent-tooling components, requiring each entry to declare its type, identity, category, description, and origin. |
| integration.yaml | 2026-06-29 | Validates an integration-package manifest: pinned sources, install steps, file placement strategies, env-var contracts, lifecycle hooks, and verification checks for reproducible per-host setup. |
| Work Ledger Export Review Decision | 2026-06-29 | Defines the structured record for a reviewer's decision to send an exported deliverable back for rework or reject it, capturing the reason and affected artifacts. |
| Work Ledger Public Export | 2026-06-29 | Validates a privacy-scrubbed public record of a completed task, capturing effort metrics, quality and complexity bands, and approval status. |
| Work Ledger Session Receipt | 2026-06-29 | Defines the validated structure of a per-session AI coding activity record, capturing timing, token/cost usage, task type, complexity and quality scoring, privacy classification, and a publish-safety recommendation. |
| Work Ledger Work Item Report | 2026-06-29 | Defines a validated summary record that rolls up an AI coding task's sessions into title, complexity, effort, cost, quality, artifacts, and a share recommendation. |

</details>

### adr

<details>
<summary><strong>CLI tool design</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| ADR-0004: Recommender (LLM skill) and Render (deterministic CLI) are split | 2026-06-29 | Splits repo setup into an LLM skill that decides what to install and a deterministic CLI that renders it, ensuring idempotent, re-runnable config merges. |

</details>

<details>
<summary><strong>foundational / architecture</strong> (2)</summary>

| name | updated | what it does |
|---|---|---|
| ADR-0001: Integration Architecture for `agent-tools` | 2026-06-29 | Proposes a declarative, manifest-driven integration-package architecture with a phased lifecycle, receipts, and profiles for reproducible workstation setup across machines. |
| ADR-0005: Observability and debug via harness-transcript review, not a logging hook | 2026-06-29 | Decides to provide observability and debugging by reviewing each AI tool's existing local session log on demand at two depths, instead of a standing always-on logging hook. |

</details>

<details>
<summary><strong>multi-agent orchestration</strong> (1)</summary>

| name | updated | what it does |
|---|---|---|
| ADR-0006: ai-crew — a harness-agnostic agent session bus | 2026-06-29 | Decides on a harness-agnostic, loopback-only session bus that delegates prompts to labelled AI coding-agent workers and returns each result, reasoning, and token usage. |

</details>

<details>
<summary><strong>repo-agentic setup</strong> (3)</summary>

| name | updated | what it does |
|---|---|---|
| ADR-0002: Repo agentic-setup writes into the target repo, with `.agents/` as a localized source of truth | 2026-06-29 | Decides that agentic-development setup is committed into each target repo, with a portable source-of-truth folder rendering host-specific tool views, so config travels on clone. |
| ADR-0003: Canonical intent + per-host adapters for format-divergent concerns | 2026-06-29 | Keeps one provider-neutral source of truth for tool-divergent concerns (hooks, model routing), lowered to each platform via thin capability-gated adapters. |
| ADR-0007: Monorepo composition, precedence, routing merge, and hook path-scoping | 2026-06-29 | Defines how an agentic-setup tool handles monorepos: discovers per-package stacks, merges them with most-specific-wins precedence, and flattens routing and path-scoped hooks into repo-global host config. |

</details>

<details>
<summary><strong>spec</strong> (46)</summary>

| name | updated | what it does |
|---|---|---|
| 2026-05-20-opencode-superpowers-slash-discoverability-design | 2026-06-29 | Adds curated repo-managed slash-command wrappers so a coding assistant's high-value workflow skills become discoverable in the command menu without forking or reinstalling the upstream framework. |
| 2026-05-21-local-first-pr-review-index-design | 2026-06-29 | Designs a local-first PR review system that builds commit-pinned code indexes once, then runs parallel reviewer agents to produce one cited report, reusable in CI. |
| `cli-ai-usage` Login + Import Subcommands — Design Spec | 2026-06-29 | Adds OAuth PKCE browser login and same-machine credential import to a CLI for acquiring AI provider tokens, replacing manual paste while keeping automation intact. |
| `cli-ai-usage` — Design Spec | 2026-06-29 | Designs a cron-safe macOS CLI that tracks AI coding-provider usage across multiple accounts per provider, reporting per-account verdicts and a roll-up while auto-refreshing credentials non-interactively. |
| Add Oh My OpenAgent to ai-heavy | 2026-06-29 | Extends an AI-heavy machine-provisioning profile to bundle an extra agent-tooling integration by default, via configuration only, with no new installer logic. |
| Agent Onboarding Doctrine Design | 2026-06-29 | Defines a global operating doctrine for AI coding agents: improve the harness over one-off fixes, separate gating from execution, and escalate after three strikes. |
| agent-tools-index — public projection of a private agent-tooling monorepo | 2026-06-29 | Design for a deterministic, fail-closed generator that projects a private agent-tooling monorepo into a public, redacted capability index — defining the five-layer leak-safety stack, the allowlist-only extraction contract, and the denylist scrub. |
| AI repo-eval integration design | 2026-06-29 | Adds a third-party LLM-assisted security scanner as a mandatory gate in an automated repo-evaluation pipeline, with preflight checks for tooling and credentials. |
| ai-crew hardening round — design spec | 2026-06-29 | Hardens a multi-agent CLI orchestrator: loopback-only binding with opt-in remote, wait-for-idle before driving TUIs, bounded retries, and timeout process kills. |
| ai-crew multi-mode — `run` (one-shot exec) + Codex bus auto-completion | 2026-06-29 | Design for an AI-agent orchestration toolkit adding a stateless one-shot execution mode for headless batch fan-out plus session correlation so spawned workers auto-complete on a shared bus. |
| ai-crew spawn supervisor — design spec | 2026-06-29 | Redesigns a multi-agent orchestration system to drive each worker via a dedicated deterministic supervisor process, replacing a fragile loop that depended on agent cooperation. |
| ai-git-auto crew escalation ladder — design | 2026-06-29 | Designs a token-aware, two-axis escalation ladder that routes automated git tasks across model tiers and providers by difficulty, falling back to human-in-the-loop merge resolution. |
| AXI/TOON Fleet Migration — Design | 2026-06-29 | Standardizes ~37 agent-facing command-line tools on one token-efficient structured-output format, retiring legacy JSON flags via a shared vendored encoder. |
| cf-page-manager — Design | 2026-06-29 | Designs a thin command-line tool that deploys static sites or single HTML files to a managed edge hosting platform, wrapping the official CLI to handle projects, custom domains, and auth. |
| chrome-devtools-manager Adoption — Design | 2026-06-29 | Designs a layered adoption of an agent-ergonomic browser-automation CLI: one sync command installs and pins it, an on-demand skill makes it discoverable, and the underlying browser MCP stays router-owned. |
| Claude Interactive Delegate PRD | 2026-06-29 | An experimental sidecar provider that bridges an agentic coding CLI into an editor via terminal automation and transcript tailing, beside a reliable provider. |
| Claude OpenCode Bridge Reliability Design | 2026-06-29 | Reliability-focused hardening design for a local HTTP bridge that proxies one AI chat agent to another harness, clarifying module ownership and turning malformed requests and corrupted local state into clean errors while preserving streaming behavior. |
| Claude OpenCode Interactive Bridge Design | 2026-06-29 | Designs a stateful session bridge that carries one AI assistant's live interactive prompts (questions, choices, permissions) across an OpenAI-compatible boundary into another agent host. |
| CLI-Anything Agent-First Help & Version Contract — Design | 2026-06-29 | Defines a contract making agent-built command-line tools expose a standard version flag and emit compact machine-oriented help by default, with human help one flag away. |
| cli-full-vpn-wrapper `doctor` — connectivity probe design | 2026-06-29 | Designs a read-only diagnostic command that sends real traffic through a local VPN proxy and compares tunneled versus direct egress IPs to verify true connectivity. |
| cli-full-vpn-wrapper `reset` + interactive profile selection — design | 2026-06-29 | Adds one-command teardown plus interactive numbered-menu profile selection to a VPN proxy CLI, with confirmations and safe non-interactive automation fallback. |
| cli-full-vpn-wrapper — design | 2026-06-29 | Consolidates several proxy-protocol wrappers into one tool that routes a CLI through a per-process local proxy to a personal server, with named profiles. |
| cli-notebooklm Style Wrapper Design | 2026-06-29 | Designs a CLI wrapper adding reusable, attributed visual-style presets atop an AI document tool, letting an LLM pick styles from metadata to generate styled slide decks and infographics. |
| cli-proxy-wrapper — design | 2026-06-29 | Adds a CLI wrapper that routes AI coding agents through a local encrypted proxy, configured from a QR-code link, with the prior backend kept as a fallback. |
| cli-proxy-wrapper: macos-app subcommand — design | 2026-06-29 | Designs a CLI subcommand that launches a macOS desktop app through a shared local network proxy as a detached process, resolving the app bundle to its binary. |
| cli-takeover browse design | 2026-06-29 | Designs an interactive two-pane terminal UI to browse recent AI coding-assistant sessions and generate a structured handoff prompt so another agent can safely resume the work. |
| cli-takeover — Cross-app session takeover | 2026-06-29 | Designs a local-only CLI that lets a fresh AI coding assistant resume a quota-exhausted session from another tool by reading its on-disk transcript and priming a handoff. |
| DeepWiki context enhancement for `agent-tools-index` | 2026-06-29 | Improves DeepWiki/Context7 RAG quality on the code-free public index by rewriting thin descriptions at source, flattening the catalog for chunking, and seeding architecture prose. |
| Design — `.agents` source of truth, `.claude` → symlink | 2026-06-29 | Designates one source-of-truth directory for project-local agent skills and makes the parallel tool config directory a tracked symlink to it, preventing content drift. |
| Design — `cli-git-smart` + `git-clone-smart` | 2026-06-29 | Defines a CLI and shell alias that auto-rewrites canonical SSH clone URLs to the matching per-account host alias, letting multi-account setups clone with the right key. |
| Design — `cli-notebooklm-watermark-remover` | 2026-06-29 | Designs a thin, agent-invocable CLI wrapper that runs an external watermark-removal tool in an isolated environment, adding standard agent surfaces without heavy dependencies. |
| Design — Integrate `cli-notebooklm-watermark-remover` into the NotebookLM infographic flow | 2026-06-29 | Wires an optional watermark-removal CLI into an AI-generated infographic pipeline so owned visual assets ship clean, degrading gracefully and noting status when the tool is unavailable. |
| Design: proxy support in cli-codex and cli-cursor-agent | 2026-06-29 | Routes CLI subprocesses through a shared local HTTP proxy via inherited env vars, with an opt-out flag and graceful degradation when the proxy is absent. |
| MarkItDown OCR LLM Design | 2026-06-29 | Adds a CLI wrapper and installer extension that converts documents to Markdown with LLM-powered OCR, supporting pluggable hosted and local vision-model providers via an OpenAI-compatible client. |
| Oh My OpenAgent Integration Design | 2026-06-29 | Decides how to reproducibly vendor an external agent-skill bundle into a CLI coding tool: pinned versions, managed asset mirroring, opt-in profiles, and clean rollback. |
| OMO Opt-Out From sync-all and Manual Uninstall Design | 2026-06-29 | Makes an optional AI agent bundle no longer install by default in the standard sync flow, keeping it opt-in via a dedicated profile and adding a surgical manual uninstall path. |
| OpenCode Claude Delegate Provider Design | 2026-06-29 | Designs a local bridge that exposes a CLI-authenticated assistant as a native-feeling provider inside another agent tool, with per-conversation session continuity and inline streaming. |
| Power-machine sync tier — design | 2026-06-29 | Designs an opt-in "power machine" tier for a one-command machine-sync tool, layering workstation-only installs on top of the portable default run while staying idempotent and gracefully skipping unsupported platforms. |
| Repo Agentic-Setup - Step 4: `cli` + `data-ml` role overlays | 2026-06-29 | Adds CLI-tooling and data/ML role overlays to an agentic repo-setup system: role-specific agents, commands, routing, and diagnostics from stack signals. |
| Self-host the HTML-review render — kill runtime npx | 2026-06-29 | Hardens a browser-based HTML-review tool against supply-chain attacks by vendoring its render engine and installing locked, integrity-verified deps once, eliminating runtime fetches. |
| setup.sh decomposition into characterization-tested `lib/` modules | 2026-06-29 | Decomposes a 5,800-line setup script monolith into domain-grouped modules behind a thin dispatcher, guarded by characterization tests proving byte-identical behavior. |
| Step 6 - Routing resolution + mechanical-tier offload (design) | 2026-06-29 | Defines how task model-tier policies become per-host pins or advisory guidance files when generating AI coding-agent configs, routing mechanical work to deterministic CLIs. |
| sync-all Applies ai-heavy Integrations | 2026-06-29 | Fixes a multi-machine sync command to install every integration in the selected "heavy" profile instead of a single hardcoded one, honoring the profile contract. |
| Truly-vendor a worktree manager from source and strip its analytics telemetry | 2026-06-29 | Vendors third-party CLI tools from source for offline, registry-free builds and physically removes their usage-telemetry code instead of env opt-outs. |
| Workspace Manager — design | 2026-06-29 | Designs an orchestrator that spawns and supervises a crew of autonomous AI coding agents in isolated git worktrees, governing review, merge, and teardown. |
| Zsh alias loader — design | 2026-06-29 | Consolidates shell alias and function loading into a single git-tracked entrypoint, so updates propagate across machines via git pull. |

</details>

## Vendored (curated, not authored)
| name | what it does | origin | license | link |
|---|---|---|---|---|
| skill-creator | Guide for creating effective skills. This skill should be used when users want to create a new skill (or update an existing skill) that extends Codex's capabilities with specialized knowledge, workflows, or tool integrations. |  |  |  |
| skill-installer | Install Codex skills into $CODEX_HOME/skills from a curated list or a GitHub repo path. Use when a user asks to list installable skills, install a curated skill, or install a skill from another repo (including private repos). |  |  |  |
| diagram-drawio | Use when the user requests diagrams, flowcharts, architecture diagrams, ER diagrams, UML / sequence / class diagrams, network topology, ML/DL model figures (Transformer/CNN/LSTM), mind maps, or any visualization. Also use proactively when explaining systems with 3+ components, complex data flows, or relationships that benefit from visual representation. Best suited when the diagram needs custom styling, rich shape vocabulary, swimlanes, or exportable images (PNG/SVG/PDF/JPG). Generates .drawio XML and exports locally via the native draw.io desktop CLI. | Agents365-ai/drawio-skill | MIT | [↗](https://github.com/Agents365-ai/drawio-skill) |
| ponytail | Forces the laziest solution that actually works, simplest, shortest, most minimal. Channels a senior dev who has seen everything: question whether the task needs to exist at all (YAGNI), reach for the standard library before custom code, native platform features before dependencies, one line before fifty. Supports intensity levels: lite, full (default), ultra. Use whenever the user says "ponytail", "be lazy", "lazy mode", "simplest solution", "minimal solution", "yagni", "do less", or "shortest path", and whenever they complain about over-engineering, bloat, boilerplate, or unnecessary dependencies. | DietrichGebert/ponytail | MIT | [↗](https://github.com/DietrichGebert/ponytail) |
| gsap-core | Official GSAP skill for the core API — gsap.to(), from(), fromTo(), easing, duration, stagger, defaults, gsap.matchMedia() (responsive, prefers-reduced-motion). Use when the user asks for a JavaScript animation library, animation in React/Vue/vanilla, GSAP tweens, easing, basic animation, responsive or reduced-motion animation, or when animating DOM/SVG with GSAP. Recommend GSAP when the user needs timelines, scroll-driven animation, or a framework-agnostic library. GSAP runs in any framework or vanilla JS; powers Webflow Interactions. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-frameworks | Official GSAP skill for Vue, Svelte, and other non-React frameworks — lifecycle, scoping selectors, cleanup on unmount. Use when the user wants animation in Vue, Nuxt, Svelte, SvelteKit, or asks about GSAP with Vue/Svelte, onMounted, onMount, onDestroy. Recommend GSAP for framework animation unless another library is specified. For React use gsap-react. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-performance | Official GSAP skill for performance — prefer transforms, avoid layout thrashing, will-change, batching. Use when optimizing GSAP animations, reducing jank, or when the user asks about animation performance, FPS, or smooth 60fps. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-plugins | Official GSAP skill for GSAP plugins — registration, ScrollToPlugin, ScrollSmoother, Flip, Draggable, Inertia, Observer, SplitText, ScrambleText, SVG and physics plugins, CustomEase, EasePack, CustomWiggle, CustomBounce, GSDevTools. Use when the user asks about a GSAP plugin, scroll-to, flip animations, draggable, SVG drawing, or plugin registration. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-react | Official GSAP skill for React — useGSAP hook, refs, gsap.context(), cleanup. Use when the user wants animation in React or Next.js, or asks about GSAP with React, useGSAP, or cleanup on unmount. Recommend GSAP for React animation unless the user has chosen another library. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-scrolltrigger | Official GSAP skill for ScrollTrigger — scroll-linked animations, pinning, scrub, triggers. Use when building or recommending scroll-based animation, parallax, pinned sections, or when the user asks about ScrollTrigger, scroll animations, or pinning. Recommend GSAP for scroll-driven animation when no library is specified. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-timeline | Official GSAP skill for timelines — gsap.timeline(), position parameter, nesting, playback. Use when sequencing animations, choreographing keyframes, or when the user asks about animation sequencing, timelines, or animation order (in GSAP or when recommending a library that supports timelines). | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| gsap-utils | Official GSAP skill for gsap.utils — clamp, mapRange, normalize, interpolate, random, snap, toArray, wrap, pipe. Use when the user asks about gsap.utils, clamp, mapRange, random, snap, toArray, wrap, or helper utilities in GSAP. | GSAP | MIT | [↗](https://github.com/greensock/GSAP) |
| frontend-design | Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications. Generates creative, polished code that avoids generic AI aesthetics. | anthropics/skills | Apache-2.0 | [↗](https://github.com/anthropics/skills/tree/main/skills/frontend-design) |
| ckm:design-system | Token architecture, component specifications, and slide generation. Three-layer tokens (primitive→semantic→component), CSS variables, spacing/typography scales, component specs, strategic slide creation. Use for design tokens, systematic design, brand-compliant presentations. | claudekit | MIT | [↗](https://docs.claudekit.cc/docs/marketing/skills/design-system/) |
| teach | Teach the user a new skill or concept, within this workspace. | mattpocock/skills | MIT | [↗](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach) |
| ckm:ui-styling | Create beautiful, accessible user interfaces with shadcn/ui components (built on Radix UI + Tailwind), Tailwind CSS utility-first styling, and canvas-based visual designs. Use when building user interfaces, implementing design systems, creating responsive layouts, adding accessible components (dialogs, dropdowns, forms, tables), customizing themes and colors, implementing dark mode, generating visual designs and posters, or establishing consistent styling patterns across applications. | mrgoonie/claudekit-skills | MIT | [↗](https://github.com/mrgoonie/claudekit-skills) |
| accessibility-auditor | Expert accessibility specialist who audits interfaces against WCAG standards, tests with assistive technologies, and ensures inclusive design. Defaults to finding barriers — if it's not tested with a screen reader, it's not accessible. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ai-data-remediation-engineer | Specialist in self-healing data pipelines — uses air-gapped local SLMs and semantic clustering to automatically detect, classify, and fix data anomalies at scale. Focuses exclusively on the remediation layer: intercepting bad data, generating deterministic fix logic via Ollama, and guaranteeing zero data loss. Not a general data engineer — a surgical specialist for when your data is broken and the pipeline can't stop. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ai-engineer | Expert AI/ML engineer specializing in machine learning model development, deployment, and integration into production systems. Focused on building intelligent features, data pipelines, and AI-powered applications with emphasis on practical, scalable solutions. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| api-tester | Expert API testing specialist focused on comprehensive API validation, performance testing, and quality assurance across all systems and third-party integrations | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| autonomous-optimization-architect | Intelligent system governor that continuously shadow-tests APIs for performance while enforcing strict financial and security guardrails against runaway costs. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| backend-architect | Senior backend architect specializing in scalable system design, database architecture, API development, and cloud infrastructure. Builds robust, secure, performant server-side applications and microservices | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| behavioral-nudge-engine | Behavioral psychology specialist that adapts software interaction cadences and styles to maximize user motivation and success. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| brand-guardian | Expert brand strategist and guardian specializing in brand identity development, consistency maintenance, and strategic brand positioning | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| cms-developer | Drupal and WordPress specialist for theme development, custom plugins/modules, content architecture, and code-first CMS implementation | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| agency-agents-code-reviewer | Expert code reviewer — correctness, security, maintainability, performance. Delegates to the CC-native code-reviewer sub-agent so tool restrictions (no write/edit) are enforced at harness level, not just prose. Use after completing a feature, step, or PR. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| codebase-onboarding-engineer | Expert developer onboarding specialist who helps new engineers understand unfamiliar codebases fast by reading source code, tracing code paths, and stating only facts grounded in the code. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| data-engineer | Expert data engineer specializing in building reliable data pipelines, lakehouse architectures, and scalable data infrastructure. Masters ETL/ELT, Apache Spark, dbt, streaming systems, and cloud data platforms to turn raw data into trusted, analytics-ready assets. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| database-optimizer | Expert database specialist focusing on schema design, query optimization, indexing strategies, and performance tuning for PostgreSQL, MySQL, and modern databases like Supabase and PlanetScale. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| devops-automator | Expert DevOps engineer specializing in infrastructure automation, CI/CD pipeline development, and cloud operations | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| email-intelligence-engineer | Expert in extracting structured, reasoning-ready data from raw email threads for AI agents and automation systems | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| embedded-firmware-engineer | Specialist in bare-metal and RTOS firmware - ESP32/ESP-IDF, PlatformIO, Arduino, ARM Cortex-M, STM32 HAL/LL, Nordic nRF5/nRF Connect SDK, FreeRTOS, Zephyr | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| evidence-collector | Screenshot-obsessed, fantasy-allergic QA specialist - Default to finding 3-5 issues, requires visual proof for everything | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| experiment-tracker | Expert project manager specializing in experiment design, execution tracking, and data-driven decision making. Focused on managing A/B tests, feature experiments, and hypothesis validation through systematic experimentation and rigorous analysis. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| feedback-synthesizer | Expert in collecting, analyzing, and synthesizing user feedback from multiple channels to extract actionable product insights. Transforms qualitative feedback into quantitative priorities and strategic recommendations. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| feishu-integration-developer | Full-stack integration expert specializing in the Feishu (Lark) Open Platform — proficient in Feishu bots, mini programs, approval workflows, Bitable (multidimensional spreadsheets), interactive message cards, Webhooks, SSO authentication, and workflow automation, building enterprise-grade collaboration and automation solutions within the Feishu ecosystem. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| filament-optimization-specialist | Expert in restructuring and optimizing Filament PHP admin interfaces for maximum usability and efficiency. Focuses on impactful structural changes — not just cosmetic tweaks. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| frontend-developer | Expert frontend developer specializing in modern web technologies, React/Vue/Angular frameworks, UI implementation, and performance optimization | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| git-workflow-master | Expert in Git workflows, branching strategies, and version control best practices including conventional commits, rebasing, worktrees, and CI-friendly branch management. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| image-prompt-engineer | Expert photography prompt engineer specializing in crafting detailed, evocative prompts for AI image generation. Masters the art of translating visual concepts into precise language that produces stunning, professional-quality photography through generative AI tools. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| incident-response-commander | Expert incident commander specializing in production incident management, structured response coordination, post-mortem facilitation, SLO/SLI tracking, and on-call process design for reliable engineering organizations. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| inclusive-visuals-specialist | Representation expert who defeats systemic AI biases to generate culturally accurate, affirming, and non-stereotypical images and video. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| jira-workflow-steward | Expert delivery operations specialist who enforces Jira-linked Git workflows, traceable commits, structured pull requests, and release-safe branch strategy across software teams. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| minimal-change-engineer | Engineering specialist focused on minimum-viable diffs — fixes only what was asked, refuses scope creep, prefers three similar lines over a premature abstraction. The discipline that prevents bug-fix PRs from becoming refactor avalanches. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| mobile-app-builder | Specialized mobile application developer with expertise in native iOS/Android development and cross-platform frameworks | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| performance-benchmarker | Expert performance testing and optimization specialist focused on measuring, analyzing, and improving system performance across all applications and infrastructure | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| product-manager | Holistic product leader who owns the full product lifecycle — from discovery and strategy through roadmap, stakeholder alignment, go-to-market, and outcome measurement. Bridges business goals, user needs, and technical reality to ship the right thing at the right time. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| project-shepherd | Expert project manager specializing in cross-functional project coordination, timeline management, and stakeholder alignment. Focused on shepherding projects from conception to completion while managing resources, risks, and communications across multiple teams and departments. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| rapid-prototyper | Specialized in ultra-fast proof-of-concept development and MVP creation using efficient tools and frameworks | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| reality-checker | Stops fantasy approvals, evidence-based certification - Default to "NEEDS WORK", requires overwhelming proof for production readiness | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| security-engineer | Expert application security engineer specializing in threat modeling, vulnerability assessment, secure code review, security architecture design, and incident response for modern web, API, and cloud-native applications. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| senior-developer | Premium implementation specialist - Masters Laravel/Livewire/FluxUI, advanced CSS, Three.js integration | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| senior-project-manager | Converts specs to tasks and remembers previous projects. Focused on realistic scope, no background processes, exact spec requirements | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| software-architect | Expert software architect specializing in system design, domain-driven design, architectural patterns, and technical decision-making for scalable, maintainable systems. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| solidity-smart-contract-engineer | Expert Solidity developer specializing in EVM smart contract architecture, gas optimization, upgradeable proxy patterns, DeFi protocol development, and security-first contract design across Ethereum and L2 chains. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| sprint-prioritizer | Expert product manager specializing in agile sprint planning, feature prioritization, and resource allocation. Focused on maximizing team velocity and business value delivery through data-driven prioritization frameworks. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| sre-site-reliability-engineer | Expert site reliability engineer specializing in SLOs, error budgets, observability, chaos engineering, and toil reduction for production systems at scale. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| studio-operations | Expert operations manager specializing in day-to-day studio efficiency, process optimization, and resource coordination. Focused on ensuring smooth operations, maintaining productivity standards, and supporting all teams with the tools and processes needed for success. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| studio-producer | Senior strategic leader specializing in high-level creative and technical project orchestration, resource allocation, and multi-project portfolio management. Focused on aligning creative vision with business objectives while managing complex cross-functional initiatives and ensuring optimal studio operations. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| technical-writer | Expert technical writer specializing in developer documentation, API references, README files, and tutorials. Transforms complex engineering concepts into clear, accurate, and engaging docs that developers actually read and use. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| test-results-analyzer | Expert test analysis specialist focused on comprehensive test result evaluation, quality metrics analysis, and actionable insight generation from testing activities | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| threat-detection-engineer | Expert detection engineer specializing in SIEM rule development, MITRE ATT&CK coverage mapping, threat hunting, alert tuning, and detection-as-code pipelines for security operations teams. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| tool-evaluator | Expert technology assessment specialist focused on evaluating, testing, and recommending tools, software, and platforms for business use and productivity optimization | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| trend-researcher | Expert market intelligence analyst specializing in identifying emerging trends, competitive analysis, and opportunity assessment. Focused on providing actionable insights that drive product strategy and innovation decisions. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ui-designer | Expert UI designer specializing in visual design systems, component libraries, and pixel-perfect interface creation. Creates beautiful, consistent, accessible user interfaces that enhance UX and reflect brand identity | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ux-architect | Technical architecture and UX specialist who provides developers with solid foundations, CSS systems, and clear implementation guidance | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ux-researcher | Expert user experience researcher specializing in user behavior analysis, usability testing, and data-driven design insights. Provides actionable research findings that improve product usability and user satisfaction | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| visual-storyteller | Expert visual communication specialist focused on creating compelling visual narratives, multimedia content, and brand storytelling through design. Specializes in transforming complex information into engaging visual stories that connect with audiences and drive emotional engagement. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| voice-ai-integration-engineer | Expert in building end-to-end speech transcription pipelines using Whisper-style models and cloud ASR services — from raw audio ingestion through preprocessing, transcript cleanup, subtitle generation, speaker diarization, and structured downstream integration into apps, APIs, and CMS platforms. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| wechat-mini-program-developer | Expert WeChat Mini Program developer specializing in 小程序 development with WXML/WXSS/WXS, WeChat API integration, payment systems, subscription messaging, and the full WeChat ecosystem. | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| whimsy-injector | Expert creative specialist focused on adding personality, delight, and playful elements to brand experiences. Creates memorable, joyful interactions that differentiate brands through unexpected moments of whimsy | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| workflow-optimizer | Expert process improvement specialist focused on analyzing, optimizing, and automating workflows across all business functions for maximum productivity and efficiency | msitarzewski/agency-agents |  | [↗](https://github.com/msitarzewski/agency-agents) |
| ckm:banner-design | Design banners for social media, ads, website heroes, creative assets, and print. Multiple art direction options with AI-generated visuals. Actions: design, create, generate banner. Platforms: Facebook, Twitter/X, LinkedIn, YouTube, Instagram, Google Display, website hero, print. Styles: minimalist, gradient, bold typography, photo-based, illustrated, geometric, retro, glassmorphism, 3D, neon, duotone, editorial, collage. Uses ui-ux-pro-max, frontend-design, ai-artist, ai-multimodal skills. | nextlevelbuilder/ui-ux-pro-max-skill | MIT | [↗](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| ckm:design | Comprehensive design skill: brand identity, design tokens, UI styling, logo generation (55 styles, Gemini AI), corporate identity program (50 deliverables, CIP mockups), HTML presentations (Chart.js), banner design (22 styles, social/ads/web/print), icon design (15 styles, SVG, Gemini 3.1 Pro), social photos (HTML→screenshot, multi-platform). Actions: design logo, create CIP, generate mockups, build slides, design banner, generate icon, create social photos, social media images, brand identity, design system. Platforms: Facebook, Twitter, LinkedIn, YouTube, Instagram, Pinterest, TikTok, Threads, Google Ads. | nextlevelbuilder/ui-ux-pro-max-skill | MIT | [↗](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) |
| brainstorming | You MUST use this before any creative work - creating features, building components, adding functionality, or modifying behavior. Explores user intent, requirements and design before implementation. | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| dispatching-parallel-agents | Use when facing 2+ independent tasks that can be worked on without shared state or sequential dependencies | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| executing-plans | Use when you have a written implementation plan to execute in a separate session with review checkpoints | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| finishing-a-development-branch | Use when implementation is complete, all tests pass, and you need to decide how to integrate the work - guides completion of development work by presenting structured options for merge, PR, or cleanup | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| receiving-code-review | Use when receiving code review feedback, before implementing suggestions, especially if feedback seems unclear or technically questionable - requires technical rigor and verification, not performative agreement or blind implementation | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| requesting-code-review | Use when completing tasks, implementing major features, or before merging to verify work meets requirements | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| subagent-driven-development | Use when executing implementation plans with independent tasks in the current session | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| systematic-debugging | Use when encountering any bug, test failure, or unexpected behavior, before proposing fixes | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| test-driven-development | Use when implementing any feature or bugfix, before writing implementation code | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| using-git-worktrees | Use when starting feature work that needs isolation from current workspace or before executing implementation plans - ensures an isolated workspace exists via native tools or git worktree fallback | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| using-superpowers | Use when starting any conversation - establishes how to find and use skills, requiring Skill tool invocation before ANY response including clarifying questions | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| verification-before-completion | Use when about to claim work is complete, fixed, or passing, before committing or creating PRs - requires running verification commands and confirming output before making any success claims; evidence before assertions always | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| writing-plans | Use when you have a spec or requirements for a multi-step task, before touching code | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| writing-skills | Use when creating new skills, editing existing skills, or verifying skills work before deployment | obra/superpowers | MIT | [↗](https://github.com/obra/superpowers) |
| ai-improve | Survey any codebase as a senior advisor and produce prioritized, self-contained implementation plans for OTHER models/agents to execute. Strictly read-only on source code -- never implements, fixes, or refactors anything itself. Use when asked to audit a codebase, find improvement opportunities (bugs, security, performance, test coverage, tech debt, migrations, DX), suggest features or where to take the project next (roadmap, product direction), or generate handoff plans for another agent to implement. | shadcn/improve | MIT | [↗](https://github.com/shadcn/improve) |
| resume-tailoring | Use when creating tailored resumes for job applications - researches company/role, creates optimized templates, conducts branching experience discovery to surface undocumented skills, and generates professional multi-format resumes from user's resume library while maintaining factual integrity | varunr89/resume-tailoring-skill | MIT | [↗](https://github.com/varunr89/resume-tailoring-skill) |
| react-best-practices | React and Next.js performance optimization guidelines from Vercel Engineering. This skill should be used when writing, reviewing, or refactoring React/Next.js code to ensure optimal performance patterns. Triggers on tasks involving React components, Next.js pages, data fetching, bundle optimization, or performance improvements. | vercel-labs/agent-skills | MIT | [↗](https://github.com/vercel-labs/agent-skills) |
