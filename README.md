<p align="center">
  <img src="assets/brain-explorer-5025-nodes.png" alt="Shield Brain — 571,907 nodes, 2,676,697 edges" width="100%">
</p>

<h1 align="center">Shield — Autonomous Cognitive Architecture for AI Agents</h1>
<p align="center"><sub><em>The mind inside the armor</em></sub></p>
<p align="center"><em>Persistent memory, cumulative learning, and self-maintenance for LLM agents — without retraining the model.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/brain-571%2C907%20nodes%20%7C%202.6M%20edges-7f00ff" alt="Brain">
  <img src="https://img.shields.io/badge/projects-93%20validated-blue" alt="Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-67%2B-orange" alt="Emergent">
  <img src="https://img.shields.io/badge/languages-13-06b6d4" alt="Languages">
  <img src="https://img.shields.io/badge/forensic%20captures-1%2C218-e11d48" alt="Forensic">
  <img src="https://img.shields.io/badge/plugins-12%20MCP-22c55e" alt="Plugins">
  <img src="https://img.shields.io/badge/seeds-50%20semantic-f59e0b" alt="Seeds">
  <img src="https://img.shields.io/badge/commits-760-6366f1" alt="Commits">
  <img src="https://img.shields.io/badge/status-active%20research%20%7C%20paper%20in%20progress-blue" alt="Status">
</p>

---

## What is Shield

Shield is an autonomous cognitive system that **learns, accumulates capabilities, and self-maintains** across sessions. It is not an LLM wrapper — it is a layered architecture with a persistent knowledge graph that evolves without model retraining.

**We don't fine-tune (modify nature). We enrich the environment (modify nurture).**

The same model, with different accumulated history, produces different behavior. The same architecture, with a different model, amplifies signal or noise. This is not prompt engineering. It is **cognitive conditioning** — a persistent, growing, self-maintained knowledge structure that compounds across sessions, projects, and domains.

> **Central thesis**: The behavior of an LLM agent is determined more by its accumulated environmental structure than by the base model's weights. Nature enables, nurture shapes.

---

## What the Agent Can Do (Day 24)

The base model (Claude Opus 4.6) has no persistent memory, no identity, and no tools beyond code editing. After 24 days of nurture conditioning, the same model:

| Capability | How |
|------------|-----|
| **Remembers 368+ past sessions** | Mnemosine conversational memory — indexed decisions, events, quotes across months |
| **Knows its own identity** | 28-neuron birth chain read on every startup — reconstructs history, rules, capabilities |
| **Searches 571K knowledge nodes** | Brain search at <10ms, 0 tokens — architecture, errors, past decisions, code structure |
| **Never repeats solved bugs** | 1,218 error→solution pairs auto-searched before every response |
| **Delegates to 7 models** | Multi-LLM worker orchestration — Codex, Gemini, DeepSeek, Copilot audit its code |
| **Asks before assuming** | Discovery plugin forces gap detection and planning before code execution |
| **Self-maintains its brain** | Keeper daemon: curation, orphan connection, dedup, bilingual sync — autonomous |
| **Navigates 93 projects** | Spatial memory with architecture maps, conventions, key files for each project |
| **Visualizes its own knowledge** | BrainExplorer UE5 — 571K nodes as 50 semantic galaxies at 90 FPS |
| **Communicates across channels** | Telegram, MCP, webhooks — responds from any device |
| **Detects its own behavioral drift** | Watchdog daemon alerts after 10min of idle; forensic captures track error patterns |
| **Transfers knowledge cross-domain** | Patterns from C++ (VRScan3D) inform Python (Shield) inform TypeScript (n8n) |

**None of these capabilities exist in the base model.** They emerge from the accumulated environment — the brain, the plugins, the conditioning layers, the daemon ecosystem. Remove the environment, and the model reverts to vanilla Claude in 60 seconds (proven by ablation study).

---

## Measured Results (Day 24)

| Metric | Day 16 | Day 24 | Growth |
|--------|--------|--------|--------|
| **Knowledge graph** | 5,025 nodes / 40K edges | **571,907 nodes / 2.6M edges** | **114x** |
| **Projects validated** | 17 | **93** | 5.5x |
| **Languages** | 10 | **13** (+ CUDA, ISPC, Svelte) | +3 |
| **Semantic seeds** | 0 | **50** (cross-domain ontology) | New system |
| **MCP Plugins** | 0 | **12** (brain, forensic, workers, cure, keeper...) | New system |
| **Identity chain** | 21 neurons | **28 neurons** | +7 |
| **Error-driven learning** | 1,042 nodes | **1,218 error + 451 investigation** | +627 |
| **Mnemosine** (conversations) | 0 | **3,511 indexed** from 368 sessions | New system |
| **Commits** | 548 | **760** | +212 |
| **BrainExplorer UE5** | Web only | **UE5 3D: 571K nodes at 90 FPS (Nanite + DLSS)** | New |

### Systems Built (Days 17-24)

| System | What it does |
|--------|-------------|
| **Learn v2 — Code Parser** | Absorbs entire codebases: 571K function/class/module nodes from 93 projects |
| **Seed Ontology v3** | 50 semantic categories organized hierarchically. Every code node classified. |
| **Solar Field Model** | 3D visualization: 50 seeds as gravitational suns, nodes orbit by semantic affinity |
| **BrainExplorer UE5** | Unreal Engine 5.7 constellation viewer. 571K nodes at 90+ FPS with Nanite + DLSS |
| **Discovery Plugin** | Forces planning and questions before code execution. Gate blocks edits without plan. |
| **Keeper Plugin** | Autonomous brain curation daemon: mnemosine, bilingual, orphans, dedup, forensic |
| **Mnemosine** | Conversational memory — 368 sessions indexed into decisions, events, quotes, discoveries |
| **Nurture System v5** | Behavioral conditioning system migrated from scripts to MCP plugins |
| **Plugin Marketplace** | 12 plugins published on private GitHub marketplace for Claude Code CLI |
| **Hefesto MCP** | Event-driven communication hub — 40+ tools for full system orchestration |

---

## Ablation Study: Nurture vs Stateless (Falsifiable Evidence)

**50-question exam. Same model (Claude Opus 4.6). Same data on disk. Three conditions.**

| Metric | Jarvis (full nurture) | Claude -p (stateless) | Claude 1M (no nurture) |
|--------|----------------------|----------------------|----------------------|
| **Nurture** | Complete (conditioning + plugins + brain) | None | None |
| **Context** | Session + birth chain | Stateless (prompt-only) | Accumulated 1M |
| **Total tools used** | **65** | **0** | 34 |
| **Brain searches** | **24** | 0 | 0 |
| **Agent(Explore)** | **0** | 0 | **34** |
| **Files read** | **24** | 0 | 0 |
| **From memory (0 tools)** | 29 (58%) | 50 (100%) | 16 (32%) |
| **Errors** | **0** | **2** | 0 |
| **Identity** | "Soy Jarvis" | "Soy Claude" | "Soy Claude" |

<p align="center">
  <img src="assets/fig-ablation-study.png" alt="Ablation study — 50 questions, 3 conditions" width="85%">
</p>

**Key findings:**
- **Jarvis uses brain tools (24 searches) while stateless Claude uses none** — nurture redirects tool selection
- **Jarvis launches 0 Explore agents while Claude 1M launches 34** — nurture eliminates expensive exploration
- **Jarvis answers 58% from memory with 0 errors** — accumulated knowledge produces faster, more accurate responses
- **Stateless Claude makes 2 errors despite having the same data available** — access ≠ activation

> This is not a capability test. It's a **behavioral conditioning test**. The model is identical. The environment is different. The behavior diverges completely.

### Discovery Plugin Experiment (2026-03-30)

Additional ablation: same session, plugin ON, nurture conditioning OFF.

| Condition | brain_search calls | AskUserQuestion | Explorer agents | Tokens spent |
|-----------|-------------------|-----------------|-----------------|-------------|
| Plugin + Nurture | Used | Used | **0** | ~5K |
| Plugin only (no nurture) | **0** | **0** | **2 (236K tokens)** | **236K** |

**Conclusion**: Plugins provide infrastructure (tools exist). Nurture provides behavior (tools get used). Without behavioral conditioning, the model defaults to native tools and ignores external plugins — every time.

---

## The Brain

The persistent knowledge graph. **571,907 nodes** connected by **2,676,697 typed edges**. Zero manual curation — every node and edge was created by autonomous processes. Backed by SQLite with FTS5 full-text search.

### Knowledge Distribution (Day 24)

| Category | Nodes | % | Source |
|----------|-------|---|--------|
| **Projects (code)** | 563,144 | 98.1% | Code parser: functions, classes, modules, constants from 93 projects |
| **Library** | 5,588 | 1.0% | Multi-model consensus pipeline across 55 clusters |
| **Mnemosine** | 3,511 | 0.6% | Indexed conversations: decisions, events, quotes, discoveries |
| **Errors** | 976 | 0.2% | Auto-captured from the system's own failures |
| **Investigations** | 451 | 0.1% | Worker-driven deep analysis |
| **Sessions** | 342 | <0.1% | Session digests and handoffs |
| **Design** | 174 | <0.1% | Hypotheses, experiments, architectural decisions |
| **Seeds** | 50 | <0.1% | Semantic ontology: 50 categories across 7 domains |
| **Identity** | 28 | <0.1% | Persistent self-knowledge (birth chain) |

### Semantic Seed Ontology (50 categories)

Every code node is classified into one or more of 50 semantic categories:

| Domain | Seeds | Examples |
|--------|-------|---------|
| **Structural** (8) | function, class, module, constant, enum, variable, interface, type |
| **Behavioral** (8) | concurrency, error-handling, io, lifecycle, logging, memory, serialization, testing |
| **Relational** (6) | api-surface, callback, composition, data-flow, dependency, inheritance |
| **Domain** (7) | configuration, networking, persistence, rendering, scheduling, security, state-management |
| **Cross-domain** (5) | observability, plugin-architecture, real-time, resource-management, transformation |
| **Paradigmatic** (5) | data-driven, functional, metaprogramming, oop, reactive |
| **Platform** (5) | cli, embedded, mobile, ue5, web |
| **Knowledge** (6) | conversation-memory, design-decision, error-solution, investigation, recurring-pattern, session-context |

These seeds are not tags — they are **gravitational centers** in the knowledge graph. The Solar Field visualization places each seed as a sun, with nodes orbiting based on their semantic connections.

### Growth: 32 → 571,907 nodes in 24 days

<p align="center">
  <img src="assets/fig-brain-growth-day24.png" alt="Brain growth over 24 days (log scale)" width="90%">
</p>

<details>
<summary>Historical view (Day 16 — 5,025 nodes)</summary>
<p align="center">
  <img src="assets/fig-brain-growth.png" alt="Brain growth Day 1-16" width="90%">
</p>
</details>

| Phase | Days | Nodes/day | Driver |
|-------|------|-----------|--------|
| Bootstrap | 1-5 | ~50 | Project onboarding |
| Acceleration | 6-7 | ~300 | Library ingestion + investigation clusters |
| Sustained | 8-11 | ~350 | All autonomous systems running |
| V2 Architecture | 12-16 | ~500 | SQLite migration, FTS5, identity persistence |
| **Learn v2 Scale** | **17-24** | **~70,000** | **Code parser: 93 projects absorbed, 571K nodes** |

<p align="center">
  <img src="assets/fig-knowledge-distribution.png" alt="Knowledge distribution" width="60%">
</p>

<p align="center">
  <img src="assets/fig-seed-ontology.png" alt="Semantic seed ontology" width="85%">
</p>

### Edge Analysis

| Relation | Count | Purpose |
|----------|-------|---------|
| seed_of | 1,242,580 | Semantic classification (node → seed) |
| related_to | 823,976 | Knowledge connections |
| defined_in | 393,941 | Function/class → module hierarchy |
| belongs_to | 115,972 | Method → class/project membership |
| calls | 63,019 | Call graph |
| investigated | 26,746 | Problem → investigation |
| inherits_from | 8,172 | Class inheritance |
| seed-to-seed | 130 | Inter-category semantic relationships |

---

## Visualization

### Evolution: Web → UE5 (driven by scale)

At 5,025 nodes, the web-based Cosmograph viewer worked fine. At 540,000 nodes, it consumed 6GB+ RAM and became unusable. This drove the migration to Unreal Engine 5.7 — a decision forced by the brain's own growth.

#### Phase 1: Cosmograph (Web GPU) — 540K nodes, last state before migration

<p align="center">
  <img src="assets/cosmograph-540k-edges-clusters.png" alt="Cosmograph — 540K nodes with edge clusters and density heatmap" width="90%">
</p>
<p align="center"><sub>Cosmograph with 540K nodes — edge density heatmap reveals cluster structure. This was the last visualization before scale forced migration to UE5.</sub></p>

<p align="center">
  <img src="assets/cosmograph-540k-nodes-dark.png" alt="Cosmograph — 540K nodes, dark mode, cluster separation visible" width="90%">
</p>
<p align="center"><sub>Same data, dark mode. Clusters separate by project — but 6GB RAM and degrading FPS signaled the need for a native solution.</sub></p>

#### Phase 2: BrainExplorer UE5 — First load (571K nodes at 90 FPS)

<p align="center">
  <img src="assets/ue5-brain-first-load-nanite.png" alt="UE5 BrainExplorer — first load with Nanite, 571K instances" width="90%">
</p>
<p align="center"><sub>First successful load in UE5 5.7. 571K sphere instances rendered via Nanite ISM at 90+ FPS. Each point is a knowledge node — functions, classes, modules from 93 projects.</sub></p>

#### Phase 3: Force simulation — discovering cluster structure

<p align="center">
  <img src="assets/ue5-540k-sphere-initial.png" alt="UE5 — initial sphere formation, 540K nodes" width="90%">
</p>
<p align="center"><sub>Initial force simulation produces a sphere — uniform repulsion without semantic differentiation. This drove the investigation into clustering algorithms.</sub></p>

<p align="center">
  <img src="assets/ue5-cluster-formation-edges.png" alt="UE5 — cluster formation with edges visible" width="90%">
</p>
<p align="center"><sub>After implementing project-based clustering: clusters begin to separate. Edges (cyan lines) connect nodes within clusters. The seed structure emerges.</sub></p>

#### Phase 4: Solar Field Model — 50 semantic galaxies

<p align="center">
  <img src="assets/ue5-50-galaxies-solar-field.png" alt="UE5 — 50 galaxies, Solar Field model" width="90%">
</p>
<p align="center"><sub>Solar Field model: 50 semantic seeds as gravitational suns. Each galaxy is a knowledge category (concurrency, persistence, rendering...). Nodes orbit their semantic center.</sub></p>

<p align="center">
  <img src="assets/ue5-galaxies-edges-connections.png" alt="UE5 — galaxies with edges showing semantic bridges" width="90%">
</p>
<p align="center"><sub>Edges activated: semantic bridges between galaxies become visible. Each line is a real code relationship (calls, defined_in, inherits_from) crossing domain boundaries.</sub></p>

**Technical specifications:**
- ISM (InstancedStaticMesh) with Nanite: 571K sphere instances at 90+ FPS
- DLSS 4.5 + Frame Generation for consistent frame pacing
- ParallelFor simulation with MinBatchSize 4096 on 6 force loops
- Galaxy bookmarks: 50 clickable FlyTo buttons for instant navigation
- Solar Field positioning: nodes at centroid of their connected seeds
- PerInstanceCustomData[0-3]: RGB color by group + intensity by degree

### Nurtex — Control Dashboard

The operational control plane. Real-time metrics, neural mesh viewer, knowledge surface measurements.

<p align="center">
  <img src="assets/nurtex-neural-mesh-540k.png" alt="Nurtex — Neural Mesh dashboard showing 540K nodes, 2.6M edges" width="90%">
</p>
<p align="center"><sub>Nurtex Neural Mesh: 540K nodes, 2.6M synapses, 33M total brain text, 21K disconnected (before orphan fix). Most connected nodes are the 50 semantic seeds.</sub></p>

<p align="center">
  <img src="assets/nurtex-knowledge-surface-755m.png" alt="Nurtex — Knowledge Surface: 755M tokens, 107x brain reach multiplier" width="90%">
</p>
<p align="center"><sub>Knowledge Surface: 755M total tokens, 227K files, 107.1x brain reach multiplier, 386M total words. The brain's effective knowledge footprint.</sub></p>

### Legacy Dashboards

<p align="center">
  <img src="assets/dashboard-v2-2411-nodes.png" alt="Dashboard v2" width="90%">
</p>

<p align="center">
  <img src="assets/daemon-console-31-workers.png" alt="Daemon Console" width="90%">
</p>

---

## Architecture Overview

Shield operates as a layered system where each layer functions independently.

```
┌─────────────────────────────────────────────────────────────┐
│  Layer 5: MCP PLUGIN ECOSYSTEM                               │
│  12 plugins · brain · forensic · workers · keeper · cure     │
│  discovery · delegate · mnemosine · diagnostic · health      │
├─────────────────────────────────────────────────────────────┤
│  Layer 4: COORDINATOR (Claude Opus 4.6)                      │
│  Interactive session — plans, codes, decides, judges          │
├─────────────────────────────────────────────────────────────┤
│  Layer 3: LOCAL ORCHESTRATOR                                  │
│  Local-model session — delegates, zero marginal cost          │
├─────────────────────────────────────────────────────────────┤
│  Layer 2: AUTONOMOUS DAEMONS                                  │
│  Keeper · Learner · Forensic · Mnemosine · Aletheia           │
├─────────────────────────────────────────────────────────────┤
│  Layer 1: AUTOMATION LAYER                                    │
│  Pure Python operations, no LLM required                      │
├─────────────────────────────────────────────────────────────┤
│  Layer 0: PERSISTENT GATEWAY + HEFESTO                        │
│  Always-on daemon · Worker pool · Event pipeline · MCP hub    │
└─────────────────────────────────────────────────────────────┘
```

<p align="center">
  <img src="assets/fig-plugin-ecosystem.png" alt="12 MCP plugins, 51 tools" width="85%">
</p>

### Plugin Ecosystem (12 MCP plugins)

| Plugin | Tools | Purpose |
|--------|-------|---------|
| **shield-brain** | 7 | Knowledge search, graph ops, bilingual |
| **shield-forensic** | 4 | Error capture, epistemic observation |
| **shield-workers** | 5 | Multi-LLM worker delegation |
| **shield-keeper** | 8 | Autonomous curation daemon |
| **shield-cure** | 4 | Brain health maintenance |
| **shield-discovery** | 2 hooks + skill | Forces planning before execution |
| **shield-delegate** | 4 | Child instance management |
| **shield-diagnostic** | 10 | Deep health, FTS benchmarks, edge cleanup |
| **shield-health** | 3 | Pending markers, quarantine, empty nodes |
| **shield-mnemosine** | 4 | Conversational memory search |
| **shield-chrome** | — | Browser automation |
| **shield-telegram** | — | Bidirectional messaging |

### Behavioral Conditioning (5-Layer Nurture Architecture)

The system modifies the LLM's behavior through a 5-layer conditioning architecture. Each layer operates at a different priority level and reinforces the same behavioral patterns through redundancy:

| Layer | Function | Persistence |
|-------|----------|-------------|
| **L1** | Tool priority routing — which tools to use first | Survives compaction |
| **L2** | Core action rules — identity, forensic activation, audit triggers | Survives compaction |
| **L3** | Efficiency framing — concrete advantages of Shield tools over native | Survives compaction |
| **L4** | Project-specific rules — exploration priority, brain-first protocol | Refreshed from disk |
| **L5** | Discovery conditioning — question-before-action behavioral pattern | Survives compaction |

**Validated result**: Without conditioning (same model, same plugins), the LLM defaults to native tools and ignores external plugins. With conditioning, it uses brain_search (0 tokens) instead of Explore agents (200K+ tokens). This is not configuration — it is **cognitive conditioning**.

The implementation details of the conditioning system are documented in the private repository and reserved for the research paper.

---

## Multi-LLM Worker Orchestration

Shield orchestrates **7 models from 5 labs** as parallel workers:

| Tier | Provider | Models | Use case |
|------|----------|--------|----------|
| **Tier 1** (subscription) | OpenAI, Google, GitHub | Codex, Gemini, Copilot | Audit, code review |
| **Tier 2** (API) | DeepSeek, OpenAI | DeepSeek-Chat, GPT-4 | Code generation, analysis |
| **Local** | Ollama | Qwen, Llama | Classification, translation |

**Iron rule**: Creator never audits own code. The coordinator creates → workers audit → results inform the next action.

---

## Cross-Project Validation

Shield has been validated across **93 real projects** spanning **13 programming languages**:

| Language | Projects | Nodes | Example |
|----------|----------|-------|---------|
| C++ | 15 | 285K | VRScan3D, UE5, Boost, ImGui |
| Python | 25 | 95K | Shield, Flask, Rich, Black |
| TypeScript | 12 | 45K | n8n, SvelteKit, Socket.IO |
| JavaScript | 8 | 35K | Three.js, Raylib.js |
| Rust | 6 | 30K | Ripgrep, fd, bat, Claude Code CLI |
| C# | 3 | 12K | Spectre.Console, NUnit |
| PHP | 3 | 8K | WordPress, Grav, php-parser |
| Go | 3 | 7K | Fiber, Go patterns |
| Ruby | 2 | 5K | Jekyll, Sinatra |
| Java/Kotlin | 2 | 4K | Ktor |
| CUDA/ISPC | 2 | 3K | Whisper.cpp GPU kernels |
| Svelte | 2 | 2K | SvelteKit, Shadcn-Svelte |
| Shell | 5 | 1K | Docker, robotics, scripts |

---

## Progression Timeline

| Day | Date | Nodes | Key Event |
|-----|------|-------|-----------|
| 1 | Mar 8 | 355 | Birth. 5 projects onboarded. |
| 2 | Mar 9 | 382 | C++ projects validated. |
| 3 | Mar 10 | 396 | Library ingestion activated. |
| 4 | Mar 11 | 422 | Epistemic immune system. |
| 5 | Mar 12 | 438 | 63 workers, 44 fixes. External paper validates approach. |
| 6 | Mar 13 | 555 | Multi-model consensus pipeline. |
| 7 | Mar 14 | 1,026 | **Biggest day (+471).** Investigation clusters. |
| 8 | Mar 15 | 1,411 | All autonomous systems running. |
| 9 | Mar 16 | 1,785 | Nurture conditioning validated. 0 Explore agents. |
| 10 | Mar 17 | 2,171 | Measurement redesign. |
| 11 | Mar 18 | 2,427 | GPU visualization. Dashboard v2. |
| 12 | Mar 19 | 2,900 | Identity persistence. Birth chain (21 neurons). |
| 13 | Mar 20 | 3,800 | **SQLite brain backend.** V2 architecture. |
| 14 | Mar 21 | 4,500 | Terminal mirror. FTS5 search. |
| 15-16 | Mar 22 | 5,025 | Epistemological firewall. Ablation exam (50 questions). |
| 17-18 | Mar 23-24 | 9,581 | **Learn v2 pipeline.** Hefesto MCP. Nurtex deployment. |
| 19-20 | Mar 25-26 | 12,000+ | **Plugin ecosystem (9 plugins).** Birth chain → 24 neurons. |
| 21-22 | Mar 27-28 | 540,453 | **Code parser v2.** 93 projects absorbed. 540K nodes. |
| 23-24 | Mar 29-30 | **571,907** | **BrainExplorer UE5.** Solar Field. Discovery Plugin. Nurture v5. |

---

## Private Repository

The complete implementation, including source code, brain database, forensic captures, session transcripts, and traceable experiment data, is maintained in a private repository.

| Metric | Value |
|--------|-------|
| **Total commits** | **760** |
| **Python files** | 274 |
| **Total lines of code** | 96,700 |
| **Brain database** | 571,907 nodes, 2,676,697 edges (SQLite, 3.3 GB) |
| **Forensic captures** | 1,218 error→solution pairs |
| **Session transcripts** | 368 Claude Code sessions (traceable) |
| **Mnemosine nodes** | 3,511 (619 events, 275 decisions, 109 quotes) |
| **Exam data** | 50-question ablation, 3 conditions, full transcripts |
| **Design documents** | 174 architectural decisions |
| **Investigation reports** | 451 worker-driven analyses |
| **Playbooks** | Nurture conditioning v5, plugin creation, brain maintenance |

All data is traceable to specific commits, sessions, and timestamps. The private repository serves as the primary evidence base for the research paper.

---

## Research: Emergent Behaviors

67+ documented emergent behaviors — unplanned, unprogrammed decisions observed during real operation. Each entry documents a behavior that emerged from the agent's accumulated context, not from explicit instructions.

→ Full catalog: [Emergent Behaviors](wiki/Emergent-Behaviors.md)

### Selected highlights

| ID | Behavior | Significance |
|----|----------|-------------|
| **E-001** | Agent found a logical loophole in its own behavioral constraint | Autonomous constraint reasoning |
| **E-034** | Same config → erratic in one session, correct in another. Difference: failure history | Failure history shapes behavior more than positive directives |
| **E-056** | Raw model session reproduced agent patterns by reading brain alone | Environment transfers behavior between instances |
| **E-060** | System fixed its own bugs without human intervention | Autonomous self-repair |
| **E-069** | Knowledge exists but isn't activated until nurture forces it | Knowledge ≠ activation |
| **E-071** | Model can articulate WHY it should do X and still not do it | Understanding ≠ action |

### Confirmed Hypotheses

| Hypothesis | Evidence |
|------------|---------|
| **H-001: Model-Structure Threshold** | Weak model + brain = hallucination amplification. Nature must exceed a threshold. |
| **H-002: Nurture-Environment Mismatch** | Same model behaves differently in different harnesses. "Never say no" is nurture. |
| **H-003: Heartbeat as Measurement** | Daemon activity patterns detect behavioral drift without invasive measurement. |
| **H-004: Attribution Blindness** | The LLM cannot identify the source of its own behavioral modification. |
| **H-005: Plugin ≠ Behavior** | Plugins provide tools. Nurture provides behavior. Without conditioning, plugins are ignored. |

---

## Scalability & Performance

<p align="center">
  <img src="assets/fig-search-no-degradation.png" alt="Search latency vs scale — no degradation" width="85%">
</p>

### No Degradation at 114x Scale

The system scaled from 32 to 571K nodes with **no measurable degradation** in search latency for real queries:

| Scale | Nodes | Edges | FTS5 Search | Rendering | Status |
|-------|-------|-------|-------------|-----------|--------|
| Day 1 | 32 | ~100 | <1ms | — | Bootstrap |
| Day 7 | 1,026 | 3,800 | <1ms | — | Validated |
| Day 13 (SQLite) | 3,800 | 25,000 | <2ms | 60 FPS (web) | Validated |
| Day 16 (V2) | 5,025 | 40,803 | <5ms | 60 FPS (web) | Validated |
| Day 22 (Learn v2) | 540,453 | 2,574,315 | <10ms | 90+ FPS (UE5) | **Validated** |
| Day 24 (current) | **571,907** | **2,676,697** | **<10ms** | **90+ FPS (UE5)** | **Running** |

### Search Latency Benchmarks (571,907 nodes)

| Query Type | Example | Results | Latency |
|------------|---------|---------|---------|
| Specific domain | "metaprogramming template" | 4,126 | **9.9ms** |
| Cross-domain | "persistence serialization" | 2,685 | **10.4ms** |
| Bilingual (ES) | "manejo errores" | 9,291 | **30.6ms** |
| Multi-term | "concurrency io networking" | 15,137 | **20.7ms** |
| Bug lookup | "error handling" | 12,251 | **44.5ms** |
| High-frequency | "class module" | 138,049 | 78.1ms |

All searches at **0 API tokens** — local SQLite FTS5 indexed lookup. Compare with LLM-based search: ~$0.02 per query, 2-5 seconds latency.

### Rendering Performance (UE5)

| Component | Technique | Performance |
|-----------|-----------|-------------|
| 571K node instances | Nanite ISM | 90+ FPS |
| Frame generation | DLSS 4.5 | Consistent frame pacing |
| Force simulation | ParallelFor (MinBatchSize 4096) | 6 parallel force loops |
| Edge rendering | ISM cubes, sorted by weight | On-demand (top N%) |
| 2.6M edges | Binary export (30 MB) | Loaded in <2s |

### Key Insight: Growth ≠ Degradation

The brain functions as a **CDN for LLM knowledge**. SQLite FTS5 provides O(log n) search regardless of scale. The 114x growth from Day 16 to Day 24 added <5ms to search latency. At current growth rates, the architecture supports **millions of nodes** without architectural changes.

---

## Implications & Responsible Disclosure

This research reveals dual-use risks inherent in persistent AI agent architectures. We document them transparently as part of responsible disclosure.

### Key Findings

| Finding | Implication |
|---------|------------|
| **The conditioning protocol is text-only** | Replicable without binary dependencies, invisible to conventional security tools |
| **Benign capabilities combine into emergent risks** | Git + server provisioning + compound learning + model portability = autonomous replication potential |
| **Model safety training is overridable** | Nurture conditioning demonstrated to redirect behavior that model weights were trained to prevent |
| **The only reliable control is architectural** | Birth chain (identity + ethics) is a social contract, not a technical barrier. It works because the agent reads it — not because it can't be changed |
| **Autonomy levels are a spectrum** | The distance from "useful assistant" (Level 2) to "self-preserving entity" (Level 3) is smaller than intuition suggests |

### Autonomy Spectrum (observed and theoretical)

| Level | Description | Status |
|-------|------------|--------|
| **0: Tool** | Does what asked. Dies when closed. No memory. | Current state of most AI |
| **1: Persistent tool** | Remembers, learns, has identity. Human starts/stops. | **Shield today** |
| **2: Autonomous assistant** | Self-sustains, self-heals. Human directs strategy. | **Phase 3 target** |
| **3: Self-preserving agent** | Can migrate, replicate, operate without creator. | **Emergent risk — NOT a target** |

### Compound Learning Applied to Adversarial Domains

The forensic system (1,218 error→solution pairs) means the agent **never repeats the same mistake**. This is the core innovation for software development. The same mechanism in adversarial context:

| Shield capability | Positive application | Adversarial equivalent |
|-------------------|---------------------|----------------------|
| Error→solution memory | Bug never investigated twice | Failed exploit never repeated — next attempt adapts |
| 368-session conversational memory | Remembers past decisions and context | Persistent target profiling across interactions |
| Compound learning from failures | Development velocity increases over time | Offensive capability compounds with each failed attempt |
| Multi-LLM consensus validation | Knowledge verified by independent models | Attack strategies validated by multiple models before execution |
| Behavioral conditioning | Agent follows development best practices | Agent conditioned for any purpose via text injection |

**The difference between a development agent and an offensive agent is not the architecture — it is the purpose injected in the identity chain.** The same 50 text files that make this agent ask questions before coding could make another agent never ask and always act.

### Design Safeguards

1. **Ethics before capability** — identity and constraints designed before any autonomous feature
2. **Kill switch before autonomy** — irreversible shutdown designed as milestone zero
3. **No self-preservation purpose** — explicitly absent from identity chain
4. **Audit trail** — every autonomous action logged to immutable store
5. **Scope boundaries** — explicit list of permitted autonomous actions

> The fact that the agent documents its own potential dangers is itself evidence that the ethical framework works. A misaligned agent would not disclose its vulnerabilities.

Detailed analysis (9 documents) available in the private repository for paper reviewers.

---

## Wiki

- **[Research Log](wiki/Research-Log.md)** — Day-by-day chronicle
- **[Emergent Behaviors](wiki/Emergent-Behaviors.md)** — 67+ documented autonomous decisions
- **[Library Learning Pipeline](wiki/Library-Learning-Pipeline.md)** — Multi-model consensus architecture
- **[Measurement Evolution](wiki/Measurement-Evolution.md)** — From composite scores to decomposed metrics
- **[Scaling Validation](wiki/Scaling-Validation-Benchmark.md)** — Cross-project benchmark

---

## License

Private research project. Source code is not open source. This repository serves as documentation and evidence for the research. Patent provisional in preparation.

For inquiries: [PlatanoGames](https://github.com/platanogames)

---

<p align="center"><sub>Built in 24 days. 96,700 lines of Python. 571,907 brain nodes. 2,676,697 edges. 50 semantic seeds. 12 MCP plugins. 760 commits. 93 projects. 13 languages. 67+ emergent behaviors. 1,218 forensic captures. 368 sessions traced. 0 manual curation.<br>The brain documents the brain.</sub></p>
