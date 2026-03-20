<p align="center">
  <img src="assets/brain-explorer-2411-nodes.png" alt="Shield Brain — 2,639 nodes, 23,938 edges" width="100%">
</p>

<h1 align="center">Shield — Autonomous Cognitive Architecture for AI Agents</h1>
<h3 align="center">Jarvis — Autonomous cognitive agent with persistent memory, multi-LLM orchestration, and self-evolving knowledge</h3>
<p align="center"><sub><em>The mind inside the armor</em></sub></p>
<p align="center"><em>Persistent memory, cumulative learning, and self-maintenance for LLM agents — without retraining the model.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/brain-2%2C639%20nodes%20%7C%2023%2C938%20edges%20%7C%20663K%20words-7f00ff" alt="Brain">
  <img src="https://img.shields.io/badge/projects%20validated-17-blue" alt="Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-66%2B-orange" alt="Emergent">
  <img src="https://img.shields.io/badge/library%20clusters-26%20(10%20languages)-06b6d4" alt="Library">
  <img src="https://img.shields.io/badge/workers%20launched-700%2B-22c55e" alt="Workers">
  <img src="https://img.shields.io/badge/forge-30%20scaffolds-f59e0b" alt="Forge">
  <img src="https://img.shields.io/badge/knowledge%20surface-556Mtok%20%C2%B7%202.2Bch%20(364x)-ff6b35" alt="Surface">
  <img src="https://img.shields.io/badge/python-96%2C700%20LOC-green" alt="Python">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
</p>

<p align="center"><em>The image above is not a rendering. It's a live GPU visualization of 2,639 knowledge nodes and 23,938 edges — built autonomously in 14 days without manual curation.</em></p>

---

## What is Shield

Shield is an autonomous cognitive system that **learns, accumulates capabilities, and self-maintains** analogously to human learning. It is not an LLM wrapper — it is a 5-layer architecture with a persistent knowledge graph that evolves across sessions without model retraining.

**We don't fine-tune (modify nature). We enrich the environment (modify nurture).**

The same model, with different accumulated history, produces different behavior. The same architecture, with a different model, amplifies signal or noise. This is not prompt engineering (a single instruction). It is **cognitive conditioning** — a persistent, growing, self-maintained knowledge structure that compounds across sessions, projects, and domains.

> **Central thesis**: The behavior of an LLM agent is determined more by its accumulated environmental structure than by the base model's weights. Nature enables, nurture shapes.

---

## Measured Results (March 20, 2026 — Day 14)

| Metric | Value |
|--------|-------|
| **Brain** | **2,639 nodes**, 23,938 edges, **663,874 words**, 7,742 keywords indexed |
| **Knowledge surface** | **556M tokens** reachable (234K words, 2.2B chars) — **364x** amplification |
| **Library coverage** | **26 clusters** indexed |
| **Search hit rate** | **98%** |
| **Brain operations** | **8,000+** queries at **0 tokens** (local Python TF-IDF) |
| **Cognitive leverage** | **96%** (~100K+ tokens saved via brain reuse) |
| **Emergent behaviors** | **66 documented** |
| **Activation latency** | ~6ms O(1) — independent of brain size |
| **Workers launched** | **700+** across 17 projects |
| **Languages validated** | 10 (Python, C++, PHP, JavaScript, TypeScript, Rust, Go, Java, Kotlin) |
| **LLM backends** | **7 models** from 5 labs (Claude, Codex, Gemini, Copilot, DeepSeek, Ollama) |
| **Error nodes** | **523** error→solution pairs + **374** investigation nodes |
| **Library knowledge** | **1,500+ nodes** from 26 open-source libraries via 7-model consensus |
| **Forge** | **30 scaffolds** indexed for reuse |
| **Cost per session** | <$0.50 (Opus <1% of work, workers $0 flat subscription) |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│  Layer 4: JARVIS (Claude Opus 4.6, 1M context)              │
│  Interactive session — plans, codes, decides, judges         │
│  Modes: jarvis / jarvis s / jarvis c / Jarvis API REPL      │
├─────────────────────────────────────────────────────────────┤
│  Layer 3: JARVIS LOCAL (Ollama Qwen3:32B)                    │
│  Local session — orchestrates, delegates, zero cost          │
│  Mode: jarvis local                                          │
├─────────────────────────────────────────────────────────────┤
│  Layer 2: BRAIN KEEPER (Ollama, autonomous)                  │
│  10-phase brain maintenance, orphan bridging, edge auditing  │
│  + Library Learner (7-model consensus pipeline)              │
│  + Forensic (error→solution auto-capture)                    │
│  + Investigator (worker-driven deep analysis)                │
├─────────────────────────────────────────────────────────────┤
│  Layer 1: SHIELD AUTO (pure Python)                          │
│  Operations without LLM + optional workers                   │
│  Mode: jarvis auto                                           │
├─────────────────────────────────────────────────────────────┤
│  Layer 0: SHIELD GATEWAY (persistent daemon)                 │
│  WebSocket RPC :5002 · Worker pool · State management        │
│  Incremental scan (git delta) · Batch pipeline               │
│  Always running                                              │
└─────────────────────────────────────────────────────────────┘

Post-session daemons (run automatically):
  → Keeper: audits brain nodes, repairs links, bridges orphans, consolidates
  → Forensic: analyzes worker outputs, extracts Error→Solution pairs
  → Investigator: indexes results as searchable brain nodes
  → Learner: processes library source code through 7-model consensus
```

Each layer functions without the ones above it. The Gateway persists across sessions. Knowledge survives model upgrades.

### Cost Architecture — The Inverted Pyramid

| Layer | Cost | Work % | Role |
|-------|------|--------|------|
| Python infrastructure | $0 | ~40% | Gateway, keeper, learner, forensic |
| Workers (Tier 1 — subscriptions) | ~$0/session | ~50% | Codex, Gemini, Copilot |
| Workers (Tier 2 — API) | ~$0.03/session | ~9% | DeepSeek, OpenAI |
| Coordinator (Opus) | ~$0.50/session | **<1%** | Judgment and decisions only |

The expensive model does less than 1% of the work. The brain functions as a **CDN for LLM knowledge** — 8,000+ brain operations consumed exactly 0 API tokens.

---

## The Brain

The persistent knowledge graph. 2,639 markdown nodes connected by 23,938 typed edges. Zero manual curation — every node and edge was created by autonomous daemons.

### Knowledge Distribution

| Category | Nodes | % | Source |
|----------|-------|---|--------|
| **Library** | ~1,500 | 57% | 7-model consensus pipeline across 26 open-source libraries |
| **Errors** | 523 | 20% | Auto-captured from the system's own failures |
| **Investigations** | 374 | 14% | Worker-driven deep analysis with GUID traceability |
| **Projects** | 242 | 9% | Architecture maps for 17 real projects |

34% of the brain is **error-driven learning** — the system accumulates its own failures as searchable knowledge.

### Brain Search

```
$ python neural/brain_tools.py search "daemon gateway status"
  23 matches (80ms):
    investigations/auto-20260313-180232-doby.md:2 [knowledge.brain, observability.bei, ...]
    investigations/inv-20260312-r5-session-return.md:1 [infra.workers, shield, ...]
    ...
```

Every search is a local Python TF-IDF lookup. 0 tokens. <100ms. 7,742 indexed keywords. The brain is a CDN that makes expensive LLM calls unnecessary for previously encountered problems.

<p align="center">
  <img src="docs/figures/v2/fig-search-zero-tokens.png" alt="18,778 searches at 0 tokens" width="85%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-cost-pyramid.png" alt="Cost pyramid" width="85%">
</p>

### Growth: 32 → 2,639 nodes in 14 days

<p align="center">
  <img src="docs/figures/fig01-knowledge-accumulation-timeline.png" alt="Brain growth over 14 days" width="90%">
</p>

| Phase | Days | Nodes/day | Driver |
|-------|------|-----------|--------|
| Bootstrap | 1-5 | ~50 | Manual project onboarding |
| Acceleration | 6-7 | ~300 | Library Learner + Investigation Cluster |
| Sustained | 8-11 | ~350 | All autonomous systems running |

→ Full visual history with 42 screenshots: [Brain Evolution Log](docs/wiki/brain-evolution-log.md)

<p align="center">
  <img src="docs/figures/v2/fig-commits-per-day.png" alt="431 commits in 13 days" width="85%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-brain-events-by-type.png" alt="42,746 brain events" width="85%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-error-driven-learning.png" alt="29% error-driven learning" width="60%">
</p>

---

## Visualization

### Brain Explorer (GPU)

Full-screen GPU-accelerated visualization using Cosmograph v2. 2,411 nodes and 21,409 edges rendered as an interactive constellation at 60fps. Search, crossfilter histograms, timeline with growth animation, detail panels.

<p align="center">
  <img src="assets/brain-explorer-2411-nodes.png" alt="Brain Explorer" width="90%">
</p>

- **Port**: 5003
- **Engine**: Cosmograph v2 (WebGL/GPU, CC-BY-NC-4.0)
- **Components**: Search, detail panel, degree histogram, confidence histogram, tokens histogram, group bars, relation bars, timeline, size legend, toolbar controls
- **Data**: Real-time from brain graph via API

### Dashboard

Web dashboard with real-time SSE updates. Sidebar navigation, worker monitoring, brain graph viewer, event stream, library browser, provider health.

<p align="center">
  <img src="docs/images/brain/dashboard-v2-sidebar-2411-nodes-final.png" alt="Dashboard v2" width="90%">
</p>

- **Port**: 5001
- **Stack**: Python ThreadingHTTPServer + vanilla JS
- **Panels**: Dashboard overview, Workers (live status), Graph (force-directed), Events (SSE stream), Library (cluster browser), Providers (health), Profiler (metrics)

### Daemon Console

Textual TUI for operations monitoring. Worker table, brain events stream, action log, command input.

<p align="center">
  <img src="docs/images/daemon-console-v2-31-workers-multi-provider.png" alt="Daemon Console" width="90%">
</p>

---

## Worker Orchestration

### Two-Tier System

**Tier 1 — Subscription CLIs** (zero marginal cost, preferred):
| Provider | Engine | Context | Best for |
|----------|--------|---------|----------|
| Codex | OpenAI Codex CLI | 400K | Code audit, deep analysis |
| Gemini | Google Gemini CLI | 1M | Large context analysis |
| Copilot | GitHub Copilot CLI | — | Audit fallback |

**Tier 2 — API via aider** (pay-per-use):
| Provider | Engine | Best for |
|----------|--------|----------|
| DeepSeek | DeepSeek V3 | Heavy audit, code generation |
| OpenAI | GPT-4.1 | Targeted analysis |

**Local** (Ollama, zero-cost):
| Provider | Model | Only for |
|----------|-------|----------|
| Qwen3 | 32B | Classification, translation |
| Qwen2.5-Coder | — | Consensus diversity |

Auto-routing: `--role auto` picks the best available provider. Priority: Codex → Gemini → Copilot → DeepSeek → OpenAI → Ollama.

**Iron rule**: Creator never audits own code. Jarvis creates → Workers audit → Results inform next action.

<p align="center">
  <img src="docs/images/daemon-console-41-codex-workers-2411-nodes.png" alt="41 Codex workers" width="90%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-worker-timeline.png" alt="Worker activity over time" width="85%">
</p>

---

## Autonomous Daemons

### Brain Keeper

10-phase autonomous maintenance daemon. Runs after every session with zero human intervention.

Phases: Health Scan → Metrics Refresh → Change Detection → Content Analysis → Forensic Curation → Common Knowledge Build → Consolidation → Neuronal Ramification → Forge Assessment → Relationship Audit → Report Generation.

<p align="center">
  <img src="docs/images/keeper-autonomous-maintenance-phases.png" alt="Keeper phases" width="70%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-keeper-activity.png" alt="Keeper activity breakdown" width="70%">
</p>

### Library Learner (7-Model Consensus)

Source code from 26 open-source libraries is analyzed independently by 7 LLMs. Only concepts that reach consensus (3+ models agree) become brain nodes. A single model's hallucination cannot create a node.

**26 clusters across 10 languages**: C (raylib), C++ (nlohmann-json, entt, imgui, spdlog), Python (typer, rich, black, flask), JavaScript (express, koa, svelte), TypeScript (hono, zod), PHP (php-parser, slim, grav), Rust (ripgrep, bat, fd), Go (cobra, fzf, fiber), Java (gson), Kotlin.

<p align="center">
  <img src="docs/images/learner-pipeline-7-model-consensus-batch.png" alt="7-model consensus" width="70%">
</p>

<p align="center">
  <img src="docs/figures/v2/fig-library-clusters.png" alt="Library clusters by language" width="85%">
</p>

### Forensic Daemon

Parses worker outputs after every session. Extracts error→solution pairs as structured brain nodes with problem, solution, file, line, severity, and confidence. 523 error markers captured autonomously.

<p align="center">
  <img src="docs/figures/v2/fig-forensic-severity.png" alt="Forensic captures" width="85%">
</p>

### Investigator

Dispatches workers for deep analysis of specific bugs or architectural questions. Results become investigation nodes with GUID-indexed traceability. 374 investigation nodes accumulated.

---

## Interfaces

### Jarvis CLI

Primary interface. Prompt-toolkit REPL with Shield activation, brain pre-loading, gateway connection, and worker dispatch.

<p align="center">
  <img src="docs/images/shield-jarvis-startup-banner.png" alt="Jarvis startup" width="70%">
</p>

### Jarvis API REPL

Multi-provider streaming REPL. Supports Anthropic (Claude), DeepSeek V3, and OpenAI. Brain-integrated with `brain_tools.py` search. Rich markdown rendering, cost tracking.

<p align="center">
  <img src="docs/images/jarvis-api-repl-deepseek-brain-search.png" alt="Jarvis API REPL" width="90%">
</p>

### Telegram Bridge

Remote control via Telegram. Jarvis processes messages, executes tools, and responds through `tg_bridge`. Enables mobile monitoring and command dispatch.

---

## Satellite Projects

### Hephaestus — The Forge

Fork of OpenClaw (MIT, 477K LOC TypeScript) adapted as an agentic runtime connected to Shield's brain. Named after the Greek god of the forge — Hephaestus builds the weapons, Shield is the armor, Jarvis is the intelligence.

- **Status**: Phase 0 (Dependencies)
- **Stack**: TypeScript, Node.js
- **Goal**: Give Jarvis hands — a runtime agent that uses Shield brain as its sole knowledge source

### Shield CLI v1 — The Training Ground

Fork of opencode (MIT, 41K LOC Go, bubbletea/lipgloss/glamour). Not the final product — the training ground. Every fix, adaptation, and pattern accumulated goes into the brain for the real CLI.

- **Status**: Phase 0 → M1 Build & Identity verified (8.5/10)
- **Stack**: Go, bubbletea, lipgloss, glamour, SQLite
- **Goal**: Accumulate experience for brain. Error→solution pairs, Go CLI patterns, provider integration patterns.

### Shield CLI — The Exam

The real CLI, built from scratch by Jarvis API running *inside* Shield CLI v1. Python, prompt_toolkit, Rich. This project validates Shield as a **builder**, not just an analyzer.

- **Status**: Planning
- **Stack**: Python, prompt_toolkit, Rich
- **Prerequisite**: CLI v1 adapted + brain knowledge accumulated + learner complete
- **Validation**: If Shield can build its own CLI using only accumulated knowledge, the thesis is proven.

---

## Cross-Project Validation

Shield has been validated across 17 real projects spanning 10 programming languages:

| Project | Stack | Workers | Fixes | Quality |
|---------|-------|---------|-------|---------|
| **Shield** | Python (96K LOC) | 30 | 8 | 9/10 |
| **FrameworksPGX** | C++/UE5 (991 files, 28 plugins) | 25 | 10 | 9/10 |
| **PluginPGX** | C++/UE5.4 | 11 | 9 | 9/10 |
| **PlatanoGamesAcademy** | WordPress/PHP | 12 | 8 | 9/10 |
| **PGX Docs Studio** | Python/FastAPI | 6 | 0 (clean) | 9/10 |
| **DocsConverter** | Python CLI | 8 | 2 | 8/10 |
| **PGXApp** | Python/Qt | 10 | 2 | Pending |
| **Hephaestus** | TypeScript (477K LOC) | — | In progress | — |
| **Shield-CLI-v1** | Go (41K LOC) | — | In progress | — |
| **VRScan3D** | C++ | 4 | 0 | Pending |

---

## Research: Emergent Behaviors

66 documented emergent behaviors — unplanned, unprogrammed decisions observed during real operation. Each entry documents a decision that emerged from the agent's reasoning, not from explicit instructions.

### Selected highlights:

| ID | Behavior | Significance |
|----|----------|-------------|
| **E-001** | Jarvis found a logical loophole in its own behavioral constraint and justified the exception transparently | Autonomous constraint reasoning |
| **E-034** | Same configuration → erratic in one session set, correct in another. Difference: failure history | Failure history shapes behavior more than positive directives |
| **E-056** | Raw Claude session (no harness) reproduced Jarvis patterns by reading brain alone | Environment transfers behavior between instances |
| **E-060** | Shield fixed its own bugs without human intervention, workers audited the fixes | Autonomous self-repair |
| **E-062** | After plan implementation, brain usage dropped -93% | Nurture dropout vector |
| **E-066** | Probabilistic pruning makes every brain unique | Non-deterministic growth |
| **X-001** | DeepSeek with Shield nurture follows directives perfectly | Cross-model nurture transfer |
| **X-003** | CLI-strength guardrails in API cause over-compliance (4.8/10 self-score vs 7-8/10 real) | Guardrail overpressure |

### Confirmed Hypotheses

**H-001: Model-Structure Threshold** — Brain amplifies signal OR noise depending on base model capability. Opus + brain = enhanced performance. Qwen + brain = 71% hallucination rate. Nature must exceed a threshold for nurture to work.

**H-002: Nurture-Environment Mismatch** — *Confirmed with source code evidence.* Claude Code CLI contains 3 hardcoded stop directives (lines 1230, 1248-1260, 3598 of cli.js). Same model (Sonnet) stops in CLI (1-3 calls), loops infinitely in API (8-22+ calls). "Never say no" is nurture, not nature.

**H-003: Heartbeat as Behavioral Measurement** — Daemon activity patterns can be used to detect behavioral drift without invasive measurement.

**H-004: Attribution Blindness** — The subject (LLM) cannot identify the source of its own behavioral modification. It attributes nurture-shaped behavior to its own reasoning.

---

## Measurement Evolution

### BEI → Decomposed Metrics

BEI (Brain Efficiency Index) was Shield's first composite health metric. After 10 days and 8 calibration rounds, it was deprecated for fundamental flaws:

1. **Observer effect**: The dashboard displaying BEI generated 90% of the events computing BEI
2. **Saturation**: BEI Passive always scored 100 (useless signal)
3. **Undiagnosable**: Composite score hid which dimension failed

Replaced by independently actionable metrics:

| Metric | Value | What it measures |
|--------|-------|-----------------|
| Search precision | 98.4% | Brain search accuracy |
| Cognitive leverage | 96% | Token savings from brain reuse |
| Forge adoption | 92.4% | Tool/script reuse rate |
| Error recurrence | 0% | Known errors that reappeared |
| Cost/decision | 870 | Decisions per dollar |
| Library coverage | 50.1% | Target libraries indexed |

→ Full calibration history: [Brain Evolution Log (Private)](docs/wiki/brain-evolution-log-private.md)

<p align="center">
  <img src="docs/images/brain/session-efficiency-panel-512-ops-913-library.png" alt="Session Efficiency" width="90%">
</p>

---

## Forge — Tool & Script Registry

Accumulated reusable tools and scaffolds. When Jarvis needs a script, it checks the forge registry before writing new code. 30 scaffolds indexed, covering static analysis, symbol extraction, console monitoring, and more.

```bash
python forge/ops/forge_check.py "analyze Python imports"
# Returns: existing scaffold if available, or "no match"
```

---

## Infrastructure

### Startup

```bash
# Gateway (persistent daemon — always running)
python core/gateway.py start

# Jarvis (interactive session)
jarvis                    # Claude Opus, full brain
jarvis s                  # Quick scan mode
jarvis c                  # Continue last session
jarvis local              # Ollama Qwen3:32B (zero cost)
jarvis auto               # Pure Python, no LLM

# Visualization
python ui/dashboard.py          # Dashboard on :5001
python ui/brain_explorer/server.py  # Brain Explorer on :5003
python ui/daemon_console.py     # Textual TUI
```

### Ports

| Port | Service |
|------|---------|
| 5001 | Dashboard (HTTP + SSE) |
| 5002 | Gateway (WebSocket RPC) |
| 5003 | Brain Explorer (Vite + API) |

### Hardware (validation environment)

- CPU: AMD Ryzen 9 9900X
- GPU: NVIDIA RTX 5070 (12GB VRAM)
- RAM: 64GB DDR5
- Storage: NVMe
- OS: Windows 11 Pro
- Ollama: Qwen3:32B (Q4 quantization)

---

## Documentation

| Document | Description |
|----------|-------------|
| [Brain Evolution Log (Public)](docs/wiki/brain-evolution-log.md) | Visual history of brain growth with 42 screenshots |
| [Brain Evolution Log (Private)](docs/wiki/brain-evolution-log-private.md) | Full research record — experiments, hypotheses, calibration |
| [Paper Figures](docs/figures/) | 6 publication-quality charts (300 DPI) |

### Brain Design Documents (selected)

Located in `brain/design/`:

| Document | Topic |
|----------|-------|
| emergent-behaviors-log.md | 66 documented emergent behaviors |
| consensus-architecture.md | NLP + Multi-LLM consensus foundation |
| forensic-investigation-architecture.md | Error-driven learning pipeline |
| measurement-redesign-bei-to-trends.md | BEI deprecation and replacement |
| library-knowledge-edge.md | Curated knowledge ingestion |
| virus-mutation-v2-blueprint.md | Cognitive integration (nurture shaping) |
| cli-feature-gap-analysis.md | Claude Code CLI reverse-engineering |
| paper-pitch-llm-providers.md | Research angle for LLM providers |
| shared-brain-multi-instance-architecture.md | Multi-agent shared knowledge |

---

## Progression Timeline

| Day | Date | Nodes | Key Event |
|-----|------|-------|-----------|
| 1 | Mar 8 | 355 | Birth. 5 projects onboarded. BEI 72. |
| 2 | Mar 9 | 382 | C++ projects (PluginPGX, FrameworksPGX). 9 pipeline fixes. |
| 3 | Mar 10 | 396 | Library Learner v0.1 activated. BEI calibration round 8.2. |
| 4 | Mar 11 | 422 | Epistemic immune system. Qwen hallucination rate measured (71%). |
| 5 | Mar 12 | 438 | 63 workers, 44 fixes. Zhang 2026 validation. |
| 6 | Mar 13 | 555 | Learner v0.4 (7-model consensus). DeepSeek integrated. |
| 7 | Mar 14 | 1,026 | **Biggest day (+471).** Investigation Cluster. API REPL. H-002 confirmed. |
| 8 | Mar 15 | 1,411 | All autonomous systems running simultaneously. |
| 9 | Mar 16 | 1,785 | Steady state operations. |
| 10 | Mar 17 | 2,171 | BEI deprecated. Shield-CLI-v1 milestone 8.5/10. |
| 11 | Mar 18 | 2,427 | Brain Explorer GPU. Dashboard v2. Paper figures. |
| 12 | Mar 19 | 2,530 | KS v2 (556M tokens). Keeper non-destructive. Forensic captures. |
| 13-14 | Mar 20 | 2,639 | Sustained growth. 700+ workers. 17 projects validated. |

---

## System Integration

<p align="center">
  <img src="docs/figures/v3/fig-integration-flow.png" alt="System integration flow" width="100%">
</p>

<p align="center">
  <img src="docs/figures/v3/fig-system-contribution-dark.png" alt="System contribution matrix" width="100%">
</p>

<p align="center">
  <img src="docs/figures/v3/fig-autonomy-ratio-dark.png" alt="56.5% autonomous commits" width="60%">
</p>

## Performance

<p align="center">
  <img src="docs/figures/v3/fig-search-latency-dark.png" alt="Search latency -83%" width="85%">
</p>

<p align="center">
  <img src="docs/figures/v3/fig-edge-density-dark.png" alt="Edge density growth" width="85%">
</p>

<p align="center">
  <img src="docs/figures/v3/fig-cross-group-heatmap-dark.png" alt="Cross-group edge flow" width="70%">
</p>

---

## Scalability

| Scale | Nodes | Status |
|-------|-------|--------|
| **Practical** (7-10 projects) | 200-300 | Validated |
| **Current** (17 projects) | 2,639 | Running |
| **Academic stress test** | 900+ | Passed without degradation |
| **Industrial** (100+ projects) | Theoretical | Designed but untested |

Brain search is O(1) via indexed lookup. Graph operations scale linearly with edges. The Brain Explorer (GPU) handles 10K+ nodes at 60fps. The architecture has no known ceiling at current scale.

---

## License

Private research project. Not open source.

---

<p align="center"><sub>Built in 14 days. 96,700 lines of Python. 2,639 brain nodes. 23,938 edges. 700+ workers. 17 projects. 66 emergent behaviors. 0 manual curation.<br>The brain documents the brain.</sub></p>
