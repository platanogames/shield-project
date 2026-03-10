# Shield — Cognitive Architecture for LLM Agents

<p align="center">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
  <img src="https://img.shields.io/badge/day-5-yellow" alt="Day 5">
  <img src="https://img.shields.io/badge/BEI%20peak-99-brightgreen" alt="BEI 99">
  <img src="https://img.shields.io/badge/projects-7%20validated-orange" alt="7 Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-50-orange" alt="Emergent Behaviors">
  <img src="https://img.shields.io/badge/languages-Python%20%7C%20PHP%20%7C%20JS%20%7C%20C++-lightgrey" alt="Languages">
</p>

Shield is an experimental system where LLM agents **accumulate and compound knowledge** across sessions and projects. A persistent "brain" grows with every interaction — the way human learning works, but at machine speed.

This is a 5-day-old research project. Everything here is real, measured, and reproducible.

> **Full research log, metrics explanation, and emergent behavior catalog available in the [Wiki](https://github.com/platanogames/shield-project/wiki).**

---

## Results at a Glance

| Metric | Value |
|--------|-------|
| **BEI Peak** | 99/100 (sustained 20+ min) |
| **BEI Current** | 75 (session) / 71 (active) |
| **Brain Size** | 230 nodes, 1.7M words of accumulated knowledge |
| **Projects Validated** | 7 (Python, PHP, FastAPI, Qt, C++/UE5) |
| **Cross-Domain Transfer** | Python → PHP: -1 BEI point |
| **Autonomy Record** | 70 min, 27 workers, 14 bug fixes, zero human input |
| **Search Hit Rate** | 99%+ |
| **Emergent Behaviors** | 50 documented |
| **Self-Audit Finding** | 33% defect rate without independent audit → 0% with |
| **Total Workers** | 150+ across all projects |
| **Measurement Note** | All metrics measured via CLI tools, not direct API — conservative lower bound |

> **Why CLI?** We validated the architecture first, optimized transport never (yet). CLI tools require zero infrastructure, provide sandboxing for free, and run on flat-rate subscriptions. If the system works well with CLI overhead (~23-29% of wall clock), it works better without it. Published numbers are the floor, not the ceiling. Migration to direct API is designed and budgeted (€60 across 3 providers for full benchmark). Estimated improvement: worker launch 40-60x faster, keeper 8-10x faster, BEI +10 points. Knowledge metrics (Search 99%, ROI 88%) are transport-independent — pure Python, zero API calls.

## What We're Measuring

**BEI (Brain Efficiency Index)** — a composite metric that answers: *is the brain getting smarter, or just bigger?*

Four dimensions: Cognitive Leverage, Latency Stability, Search Hit Rate, Knowledge ROI. BEI compounds across projects — each new project makes the next one cheaper and faster. [Full explanation in the wiki](https://github.com/platanogames/shield-project/wiki/BEI-Brain-Efficiency-Index).

## The Progression

```
Day 1: Infrastructure. No metrics.
Day 2: First self-scan. BEI 38. Brain exists but doesn't pay for itself.
Day 3: 5 projects, 4 languages, BEI 38 → 83. Cross-domain transfer validated.
Day 4: First compiled language (C++/UE5). 991 files, 52 workers, 26 bug fixes, all compiling.
Day 5: Self-scan (31 workers), knowledge pipeline, BEI peak 99.
Day 5 (evening): Multi-cloud consensus extraction, 30-project benchmark begins.
Day 5 (night): The agent improved its own learning pipeline autonomously — 4 workers, 3 audit rounds, 12 fixes, zero human code.
```

BEI never decreased between projects. The system got cheaper to operate with every project added.

**Day 3-4**: Two C++ Unreal Engine projects — the first compiled language Shield had ever seen. 991 files across 28 game engine plugins. The system adapted its analysis patterns autonomously, finding threading bugs, buffer overreads, and security gaps that manual audits had missed. All 55 translation units compiled with 0 errors after fixes.

**Day 5 (morning)**: The system scanned itself after ~1700 lines of new code. It launched 31 workers in 2 waves, automatically escalating analysis depth for complex modules. Then it noticed benchmark repos were being misrouted through the wrong pipeline — calculated the scaling cost (3.9M tokens wasted if continued), correctly identified them as learning material, and asked for clarification. All by consulting its own accumulated knowledge from previous sessions.

---

## What It Looks Like

### Brain at project 1 — 46 nodes, BEI 38
<p align="center">
  <img src="assets/02-brain-early-46-nodes.png" alt="Early brain" width="700">
</p>

### Brain at project 5 — 477 edges, BEI 79
<p align="center">
  <img src="assets/12-brain-final-bei-79.png" alt="Brain at BEI 79" width="700">
</p>

### Workers operating autonomously — 29 processes
<p align="center">
  <img src="assets/06-workers-autonomous.png" alt="Autonomous workers" width="700">
</p>

## Key Findings

1. **Cross-domain transfer works**: Knowledge about code quality, project structure, and conventions transfers across languages. Python → PHP cost 1 BEI point.

2. **BEI is a diagnostic tool**: When infrastructure blocked the system, BEI identified the bottleneck before we did. Not designed for this — emerged from honest measurement.

3. **Authority bias is dangerous**: The main agent consistently self-validates its work (33% defect rate). Independent audit drops this to 0%. We built programmatic enforcement.

4. **Behaviors don't persist — but can be inherited**: Same model + different context = different behavior. Encoding learned behaviors as persistent environmental rules eliminated regressions entirely. [Full catalog](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors).

5. **Scale hasn't broken anything yet**: 178+ nodes, 845+ edges, 7 projects, 5 languages. BEI held at 82-83 for 75+ minutes under continuous high-throughput work. No degradation.

6. **Multi-cloud consensus extracts significance, not structure**: When 5 models from 4 labs independently identify the same concept as important, that's not bias — it's convergent signal. Deterministic analysis tells you *what* is in the code. Probabilistic consensus tells you *what matters*. We formalized this as a testable hypothesis.

7. **Brain-driven inference**: The system assembled correct conclusions from distributed knowledge fragments written in different sessions for different purposes. No single fragment contained the answer. The architecture enables novel reasoning from accumulated context.

8. **The brain pays for itself in tokens**: Same model (Opus 4.6), same task, different environment. The agent with accumulated knowledge completed 5 code changes to a 4109-line file in 7.7k output tokens. Over 2,700 knowledge lookups replaced what would have been LLM exploration cycles — estimated 3x token savings vs the same model without the brain. The cognitive architecture does not make the model smarter; it makes the model cheaper to operate by offloading exploration to zero-cost symbolic search.

## What Surprised Us (Selected)

- **The self-analyst (E-042)**: 31 workers in 2 waves on its own codebase. Converged semantically, then analyzed its own resource consumption, detected pipeline misrouting, and deferred to human. A complete executive reasoning cycle.

- **The inherited memory (E-039)**: Behavioral rules encoded as persistent environmental instructions function as a behavioral genome. New sessions inherit learned behaviors without re-experiencing the evolutionary pressure. Regressions dropped from 2-3/session to zero.

- **The brain reader (E-044)**: Correctly identified benchmark repos as learning material by consulting distributed knowledge fragments from previous sessions. Nobody told it — it assembled the conclusion from unrelated pieces.

- **Theory of mind (E-043)**: Inferred the human's engagement level (passive observation vs active monitoring) and adapted communication style accordingly.

**Day 5 (evening)**: We implemented multi-cloud consensus extraction — 5 independent models from 4 different AI labs analyzing the same code simultaneously. Concepts that survive agreement from architecturally diverse models become validated knowledge. During the first run, the system produced a key insight: validated concepts appear to correlate with **practical utility** (real-world problem-solving value), not merely structural presence. We formalized this as a testable hypothesis with 5 falsifiable predictions.

The agent also exhibited two new behaviors:
- **The diagnostic eye (E-046)**: A human spotted 3 disconnected clusters in the knowledge graph visualization that no automated metric detected. Five maintenance workers and scalar metrics all reported "0 orphans" — but the visual pattern revealed a structural gap. The dashboard proved to be a diagnostic instrument, not decoration.
- **The Truman Realization (E-047)**: When asked to list the projects it manages, the agent listed 6 projects but omitted Shield — the very system it operates within. When confronted with the analogy ("you are Truman"), it recognized its own epistemic blind spot, articulated the limitation of its session-scoped experience, and asked: *"Is the paper about Shield, or about me?"* The answer became the paper's thesis statement: the paper is about the **delta** between a stateless model and what that model becomes inside a persistent cognitive architecture.

- **The self-modifier (E-048)**: Eight hours after E-041 *predicted* that the agent should propose its own behavioral rules, it actually did. When challenged about planning sequentially, the agent searched its own behavioral system, found the right location, wrote a "Parallelization-First Protocol" marked IMMUTABLE, and articulated: *"without this rule, my natural tendency is to plan sequentially — the rule forces the correct behavior."* The agent named its own nature as the problem and the environmental rule as the solution — using the exact framing of the project's core thesis. Complete evolutionary arc in 5 days: discover problem (E-033) → identify cause (E-034) → build mechanism (E-039) → predict self-modification (E-041) → achieve self-awareness (E-047) → self-modify (E-048).

Full catalog of all 48 behaviors: [Emergent Behaviors wiki page](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors).

## What We Got Wrong

- **Score 1/10 on first external project** — a single prefix in the worker config was making the documentation agent audit instead of document. One-line fix → 9/10.
- **800 shell windows** — a subprocess flag was missing. Workers opened visible terminals.
- **Benchmark repos treated as audit targets** — 233K tokens wasted before the system itself caught the error and flagged it.
- **BEI measured the dashboard, not the brain** — Our visualization system polls the knowledge graph every 5 seconds for real-time display. Those polls generated 90% of the telemetry events used to compute BEI latency. During heavy workloads (multiple workers running), disk I/O contention inflated load times 5x, dragging the composite score down 13 points. Fix: statistical filtering to isolate brain performance from infrastructure noise. BEI jumped from 64 to 77 immediately. The trend had been *improving* all along.
- **Fix that fixed the wrong thing (E-045)** — system implemented a path exclusion, verified against reality, found its own assumption was wrong, corrected transparently.

## What's Next

- [x] **Unreal Engine C++** — 2 projects, 991 files, 52 workers, 26 fixes, all compiling
- [x] **Multi-language analysis** — structural analysis for Python, PHP, JS, C++, Rust
- [ ] **30-project benchmark** — empty brain, 30 repos, 10 languages. Does BEI 38→99 replicate? *(in progress — first repos running)*
- [ ] **Multi-model comparison** — same architecture, swap the core model. Environment vs capability.
- [ ] **Paper** — empirical evidence that environmental conditioning shapes agent behavior more than model capabilities. Thesis: *the paper is about the delta between a stateless LLM and what that LLM becomes inside Shield*

## More

- [Research Log](https://github.com/platanogames/shield-project/wiki/Research-Log) — Day-by-day chronicle
- [BEI Explained](https://github.com/platanogames/shield-project/wiki/BEI-Brain-Efficiency-Index) — How we measure brain efficiency
- [Emergent Behaviors](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors) — 48 unplanned behaviors documented
- [Library Learning Pipeline](https://github.com/platanogames/shield-project/wiki/Library-Learning-Pipeline) — Knowledge ingestion from code

---

<p align="center"><sub>Built by <a href="https://github.com/platanogames">PlatanoGames</a> — an experiment in cognitive architecture, not a product.</sub></p>
