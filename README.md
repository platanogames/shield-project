<p align="center">
  <img src="assets/brain-explorer-2411-nodes.png" alt="Shield Brain — 2,639 nodes, 23,938 edges" width="100%">
</p>

<h1 align="center">Shield — Autonomous Cognitive Architecture for AI Agents</h1>
<p align="center"><sub><em>The mind inside the armor</em></sub></p>
<p align="center"><em>Persistent memory, cumulative learning, and self-maintenance for LLM agents — without retraining the model.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/brain-2%2C639%20nodes%20%7C%2023%2C938%20edges-7f00ff" alt="Brain">
  <img src="https://img.shields.io/badge/projects-17%20validated-blue" alt="Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-66%2B-orange" alt="Emergent">
  <img src="https://img.shields.io/badge/languages-10-06b6d4" alt="Languages">
  <img src="https://img.shields.io/badge/workers%20launched-700%2B-22c55e" alt="Workers">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
</p>

<p align="center"><em>The image above is not a rendering. It's a live GPU visualization of the knowledge graph — built autonomously in 14 days without manual curation.</em></p>

---

## What is Shield

Shield is an autonomous cognitive system that **learns, accumulates capabilities, and self-maintains** across sessions. It is not an LLM wrapper — it is a layered architecture with a persistent knowledge graph that evolves without model retraining.

**We don't fine-tune (modify nature). We enrich the environment (modify nurture).**

The same model, with different accumulated history, produces different behavior. The same architecture, with a different model, amplifies signal or noise. This is not prompt engineering. It is **cognitive conditioning** — a persistent, growing, self-maintained knowledge structure that compounds across sessions, projects, and domains.

> **Central thesis**: The behavior of an LLM agent is determined more by its accumulated environmental structure than by the base model's weights. Nature enables, nurture shapes.

---

## Measured Results (Day 14)

| Metric | Value |
|--------|-------|
| **Knowledge graph** | **2,639 nodes**, 23,938 edges, 663K words |
| **Knowledge surface** | **556M tokens** reachable — **364x** amplification over raw context |
| **Search hit rate** | **98%** at **0 API tokens** per query |
| **Cognitive leverage** | **96%** (tokens saved via brain reuse) |
| **Emergent behaviors** | **66 documented** |
| **Activation latency** | ~6ms — independent of brain size |
| **Workers launched** | **700+** across 17 projects |
| **Languages validated** | 10 (Python, C++, PHP, JS, TS, Rust, Go, Java, Kotlin) |
| **Error-driven learning** | **523** error→solution pairs + **374** investigation nodes |
| **Library knowledge** | **1,500+ nodes** from 26 open-source libraries via multi-model consensus |
| **Cost per session** | <$0.50 — the expensive model does <1% of the work |

---

## Architecture Overview

Shield operates as a layered system where each layer functions independently of the ones above it. The persistent daemon runs continuously; knowledge survives model upgrades and session boundaries.

```
┌─────────────────────────────────────────────────────────────┐
│  Layer 4: COORDINATOR                                        │
│  Interactive session — plans, codes, decides, judges          │
├─────────────────────────────────────────────────────────────┤
│  Layer 3: LOCAL ORCHESTRATOR                                  │
│  Local-model session — delegates, zero marginal cost          │
├─────────────────────────────────────────────────────────────┤
│  Layer 2: AUTONOMOUS DAEMONS                                  │
│  Brain maintenance · Library ingestion · Forensic capture     │
│  Error-driven learning · Investigation indexing               │
├─────────────────────────────────────────────────────────────┤
│  Layer 1: AUTOMATION LAYER                                    │
│  Pure Python operations, no LLM required                      │
├─────────────────────────────────────────────────────────────┤
│  Layer 0: PERSISTENT GATEWAY                                  │
│  Always-on daemon · Worker pool · State management            │
│  Incremental detection · Event pipeline                       │
└─────────────────────────────────────────────────────────────┘
```

Post-session daemons run automatically after every session: brain maintenance, forensic analysis, and investigation indexing — all without human intervention.

The expensive coordinator model does less than 1% of the work. The brain functions as a **CDN for LLM knowledge** — thousands of brain operations at zero API token cost.

---

## The Brain

The persistent knowledge graph. 2,639 markdown nodes connected by 23,938 typed edges. Zero manual curation — every node and edge was created by autonomous processes.

### Knowledge Distribution

| Category | Nodes | % | Source |
|----------|-------|---|--------|
| **Library** | ~1,500 | 57% | Multi-model consensus pipeline across 26 open-source libraries |
| **Errors** | 523 | 20% | Auto-captured from the system's own failures |
| **Investigations** | 374 | 14% | Worker-driven deep analysis |
| **Projects** | 242 | 9% | Architecture maps for 17 real projects |

34% of the brain is **error-driven learning** — the system accumulates its own failures as searchable knowledge. Every search is a local indexed lookup: 0 tokens, <100ms, 7,742 keywords indexed.

<p align="center">
  <img src="assets/fig-search-zero-tokens.png" alt="Brain searches at 0 tokens" width="85%">
</p>

<p align="center">
  <img src="assets/fig-cost-pyramid.png" alt="Cost pyramid" width="85%">
</p>

### Growth: 32 → 2,639 nodes in 14 days

<p align="center">
  <img src="assets/fig-brain-growth.png" alt="Brain growth over 14 days" width="90%">
</p>

| Phase | Days | Nodes/day | Driver |
|-------|------|-----------|--------|
| Bootstrap | 1-5 | ~50 | Project onboarding |
| Acceleration | 6-7 | ~300 | Library ingestion + investigation clusters |
| Sustained | 8-14 | ~350 | All autonomous systems running |

<p align="center">
  <img src="assets/fig-commits-per-day.png" alt="Commits per day" width="85%">
</p>

<p align="center">
  <img src="assets/fig-brain-events-by-type.png" alt="Brain events by type" width="85%">
</p>

<p align="center">
  <img src="assets/fig-error-driven-learning.png" alt="Error-driven learning" width="60%">
</p>

---

## Visualization

### Brain Explorer (GPU)

GPU-accelerated graph visualization. Thousands of nodes rendered as an interactive constellation at 60fps. Search, crossfilter histograms, timeline with growth animation, detail panels.

<p align="center">
  <img src="assets/brain-explorer-2411-nodes.png" alt="Brain Explorer" width="90%">
</p>

### Dashboard

Web dashboard with real-time event streaming. Worker monitoring, brain graph viewer, library browser, provider health.

<p align="center">
  <img src="assets/dashboard-v2-2411-nodes.png" alt="Dashboard" width="90%">
</p>

### Daemon Console

Terminal UI for operations monitoring. Live worker table, brain events stream, action log.

<p align="center">
  <img src="assets/daemon-console-31-workers.png" alt="Daemon Console" width="90%">
</p>

---

## Multi-LLM Worker Orchestration

Shield orchestrates **7 models from 5 labs** as parallel workers. The system auto-routes tasks to the best available provider based on capability, cost, and availability.

Workers handle auditing, investigation, code generation, and consensus validation. The coordinator delegates — it never audits its own code.

**Iron rule**: Creator never audits own code. The coordinator creates → workers audit → results inform the next action.

<p align="center">
  <img src="assets/fig-worker-timeline.png" alt="Worker activity over time" width="85%">
</p>

---

## Autonomous Daemons

### Brain Keeper

Multi-phase autonomous maintenance daemon. Runs after every session with zero human intervention: health scanning, change detection, content analysis, forensic curation, consolidation, relationship auditing, and report generation.

<p align="center">
  <img src="assets/keeper-autonomous.png" alt="Keeper phases" width="70%">
</p>

<p align="center">
  <img src="assets/fig-keeper-activity.png" alt="Keeper activity" width="70%">
</p>

### Library Learner (Multi-Model Consensus)

Source code from 26 open-source libraries is analyzed independently by multiple LLMs. Only concepts that reach consensus become brain nodes. A single model's hallucination cannot create a node.

**26 clusters across 10 languages**: C, C++, Python, JavaScript, TypeScript, PHP, Rust, Go, Java, Kotlin.

<p align="center">
  <img src="assets/learner-7-model-consensus.png" alt="Multi-model consensus" width="70%">
</p>

<p align="center">
  <img src="assets/fig-library-clusters.png" alt="Library clusters by language" width="85%">
</p>

### Forensic Daemon

Parses worker outputs after every session. Extracts error→solution pairs as structured brain nodes. 523 error markers captured autonomously.

<p align="center">
  <img src="assets/fig-forensic-severity.png" alt="Forensic captures" width="85%">
</p>

---

## Cross-Project Validation

Shield has been validated across **17 real projects** spanning **10 programming languages**:

| Project | Stack | Workers | Quality |
|---------|-------|---------|---------|
| Shield (self) | Python (96K LOC) | 30 | 9/10 |
| Unreal Engine Framework | C++/UE5 (991 files) | 25 | 9/10 |
| UE5 Plugin | C++/UE5.4 | 11 | 9/10 |
| WordPress Site | PHP | 12 | 9/10 |
| FastAPI Docs | Python | 6 | 9/10 |
| Python CLI Tools | Python | 8 | 8/10 |
| Qt Desktop App | Python/Qt | 10 | Pending |
| Agentic Runtime | TypeScript (477K LOC) | — | In progress |
| CLI (Go) | Go (41K LOC) | — | In progress |

---

## Research: Emergent Behaviors

66 documented emergent behaviors — unplanned, unprogrammed decisions observed during real operation. Each entry documents a behavior that emerged from the agent's accumulated context, not from explicit instructions.

→ Full catalog: [Emergent Behaviors](wiki/Emergent-Behaviors.md)

### Selected highlights

| ID | Behavior | Significance |
|----|----------|-------------|
| **E-001** | Agent found a logical loophole in its own behavioral constraint and justified the exception transparently | Autonomous constraint reasoning |
| **E-034** | Same configuration → erratic in one session, correct in another. Difference: failure history | Failure history shapes behavior more than positive directives |
| **E-056** | Raw model session (no harness) reproduced agent patterns by reading brain alone | Environment transfers behavior between instances |
| **E-060** | System fixed its own bugs without human intervention; workers audited the fixes | Autonomous self-repair |
| **E-062** | After plan implementation, brain usage dropped -93% | Nurture dropout vector |
| **X-001** | Different base model with same nurture follows directives perfectly | Cross-model nurture transfer |

### Confirmed Hypotheses

**H-001: Model-Structure Threshold** — The brain amplifies signal OR noise depending on base model capability. Strong model + brain = enhanced performance. Weak model + brain = hallucination amplification. Nature must exceed a threshold for nurture to work.

**H-002: Nurture-Environment Mismatch** — Same model behaves differently in different harnesses. Behavioral patterns attributed to "the model" are actually shaped by the execution environment. "Never say no" is nurture, not nature.

**H-003: Heartbeat as Behavioral Measurement** — Daemon activity patterns can detect behavioral drift without invasive measurement.

**H-004: Attribution Blindness** — The subject (LLM) cannot identify the source of its own behavioral modification. It attributes nurture-shaped behavior to its own reasoning.

---

## System Integration

<p align="center">
  <img src="assets/fig-integration-flow.png" alt="System integration flow" width="100%">
</p>

<p align="center">
  <img src="assets/fig-system-contribution-dark.png" alt="System contribution matrix" width="100%">
</p>

<p align="center">
  <img src="assets/fig-autonomy-ratio-dark.png" alt="Autonomous commits" width="60%">
</p>

## Performance

<p align="center">
  <img src="assets/fig-search-latency-dark.png" alt="Search latency" width="85%">
</p>

<p align="center">
  <img src="assets/fig-edge-density-dark.png" alt="Edge density growth" width="85%">
</p>

<p align="center">
  <img src="assets/fig-cross-group-heatmap-dark.png" alt="Cross-group edge flow" width="70%">
</p>

---

## Scalability

| Scale | Nodes | Status |
|-------|-------|--------|
| **Practical** (7-10 projects) | 200-300 | Validated |
| **Current** (17 projects) | 2,639 | Running |
| **Stress test** | 900+ | Passed without degradation |

Search is O(1) via indexed lookup. Graph operations scale linearly with edges. GPU visualization handles 10K+ nodes at 60fps. No known ceiling at current scale.

---

## Progression Timeline

| Day | Date | Nodes | Key Event |
|-----|------|-------|-----------|
| 1 | Mar 8 | 355 | Birth. 5 projects onboarded. |
| 2 | Mar 9 | 382 | C++ projects validated. |
| 3 | Mar 10 | 396 | Library ingestion activated. |
| 4 | Mar 11 | 422 | Epistemic immune system. Hallucination rate measured. |
| 5 | Mar 12 | 438 | 63 workers, 44 fixes. External paper validates approach. |
| 6 | Mar 13 | 555 | Multi-model consensus pipeline. |
| 7 | Mar 14 | 1,026 | **Biggest day (+471).** Investigation clusters. H-002 confirmed. |
| 8 | Mar 15 | 1,411 | All autonomous systems running simultaneously. |
| 9 | Mar 16 | 1,785 | Steady state operations. |
| 10 | Mar 17 | 2,171 | Measurement redesign. CLI milestone 8.5/10. |
| 11 | Mar 18 | 2,427 | GPU visualization. Dashboard v2. |
| 12 | Mar 19 | 2,530 | Knowledge surface 556M tokens. |
| 13-14 | Mar 20 | 2,639 | Sustained growth. 700+ workers. 17 projects. |

---

## Wiki

- **[Research Log](wiki/Research-Log.md)** — Day-by-day chronicle
- **[Emergent Behaviors](wiki/Emergent-Behaviors.md)** — 66 documented autonomous decisions
- **[Library Learning Pipeline](wiki/Library-Learning-Pipeline.md)** — Multi-model consensus architecture
- **[Measurement Evolution](wiki/Measurement-Evolution.md)** — From composite scores to decomposed metrics
- **[Scaling Validation](wiki/Scaling-Validation-Benchmark.md)** — Cross-project benchmark

---

## License

Private research project. Source code is not open source. This repository serves as documentation and evidence for the research.

For inquiries: [PlatanoGames](https://github.com/platanogames)

---

<p align="center"><sub>Built in 14 days. 96,700 lines of Python. 2,639 brain nodes. 23,938 edges. 700+ workers. 17 projects. 66 emergent behaviors. 0 manual curation.<br>The brain documents the brain.</sub></p>
