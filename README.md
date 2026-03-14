# Shield — Cognitive Architecture for LLM Agents

<p align="center">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
  <img src="https://img.shields.io/badge/since-March%202026-yellow" alt="Since March 2026">
  <img src="https://img.shields.io/badge/BEI%203.0-95-brightgreen" alt="BEI 3.0">
  <img src="https://img.shields.io/badge/projects-7%20validated-orange" alt="7 Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-62%20%2B%202H%20%2B%204X-orange" alt="Emergent Behaviors">
  <img src="https://img.shields.io/badge/brain-512%20nodes%20%7C%20664K%20words-purple" alt="Brain">
  <img src="https://img.shields.io/badge/languages-Python%20%7C%20PHP%20%7C%20JS%20%7C%20C++-lightgrey" alt="Languages">
</p>

Shield is an experimental system where LLM agents **accumulate and compound knowledge** across sessions and projects. A persistent "brain" grows with every interaction — the way human learning works, but at machine speed.

Active research since March 2026. Everything here is real, measured, and reproducible.

### Core Thesis: Nurture Over Nature

<sub>First committed: 2026-03-06 ([`97915fb`](https://github.com/platanogames/shield-project/commit/97915fb)) · Empirically confirmed: 2026-03-09 (E-034) · Formalized: 2026-03-12 (H-001)</sub>

> **We do not fine-tune models (modify nature). We enrich the environment (modify nurture).**

The central hypothesis of this project is that **agent behavior is shaped more by accumulated environmental structure than by the base model's weights.** The same model, given different histories, produces different behaviors. The same architecture, given different models, amplifies either signal or noise.

This is not prompt engineering. Prompt engineering is a single instruction. This is **cognitive conditioning** — a persistent, growing, self-maintaining knowledge structure that compounds across sessions, projects, and domains. The model provides capability (nature). The environment determines what emerges (nurture).

**Empirical support (as of 2026-03-14):**
- **E-034** (2026-03-09): Same configuration produced erratic behavior in one session set and correct behavior in another. The difference: accumulated failure documentation + quantified consequences. *Failure history shapes behavior more than positive directives.*
- **E-056** (2026-03-12): A raw Claude session (no harness, no automation) reproduced the orchestrator's behavioral patterns simply by reading the brain. *The environment transfers behavior across instances.*
- **H-001** (2026-03-12, **confirmed N=5 on 2026-03-14**): Same architecture + Opus = 0% erratic. Same architecture + Qwen = 71% hallucination. The brain amplifies whatever the model provides — signal or noise. *Nature enables, nurture shapes. But nature must clear a threshold for nurture to work.* Cross-matrix experiments (X-001 to X-004) tested Claude vs DeepSeek under identical conditions: same brain, same tools, same directives. Results diverged fundamentally — not just in scores, but in *how each model processes failure*.
- **H-002** (2026-03-14, new): The same set of directives produces **opposite pathologies** in different environments. In a competitive environment (CLI with host instructions), strong directives help. In a zero-competition environment (direct API), the same directives cause over-compliance. *Directive pressure must be proportional to competing forces.*

This thesis predates and is independent of any concurrent work on LLM environmental conditioning. Shield's design documents, commit history, and emergent behavior log provide full traceability from initial hypothesis (2026-03-06) through empirical confirmation (2026-03-09 to 2026-03-12).

> **Full research log, metrics explanation, and emergent behavior catalog available in the [Wiki](https://github.com/platanogames/shield-project/wiki).**

---

<p align="center">
  <img src="assets/bei-3.0-dashboard.png" alt="BEI 3.0 Dashboard" width="550">
  <br><i>BEI 3.0 Dashboard — metrics finally reflect actual brain performance.</i>
</p>

## Results at a Glance

| Metric | Value | Source |
|--------|-------|--------|
| **Brain Size** | 512 nodes, 664K words | Graph snapshot (2026-03-14) |
| **Projects Validated** | 7 (Python, PHP, FastAPI, Qt, C++/UE5) | Integration tests |
| **Search Hit Rate** | 97% (1,922 / 1,991 searches) | Brain event logs |
| **Cognitive Leverage** | 92.8% — ~1,018K tokens saved at 0 cost | 2,032 queries via procedural memory (pure Python) |
| **Opus Output Ratio** | 0.3% of total tokens | 12 sessions measured |
| **Token Economy** | 31.52:1 ROI | Efficiency history |
| **Contamination** | 0% cross-domain across 26 knowledge sources | E-053 cold-start test |
| **Cross-Domain Transfer** | Python → PHP: -1 BEI point | Live session measurement |
| **Autonomy Record** | 70 min, 27 workers, 14 bug fixes, zero human input | Session log |
| **Emergent Behaviors** | 62 documented + 2 hypotheses (H-001, H-002) + 4 cross-matrix experiments (X-001–X-004) | Research log |
| **Self-Audit Finding** | 33% defect rate without independent audit → 0% with | E-027 |
| **Total Workers** | 230+ across all projects | Worker logs |
| **Delegation Ratio** | 21:1 (workers : Opus) | Session 2026-03-10 |
| **Background-to-Visible Work** | 65:1 | E-061, session 2026-03-12 |

> **Why CLI?** We validated the architecture first, optimized transport never (yet). CLI tools require zero infrastructure, provide sandboxing for free, and run on flat-rate subscriptions. If the system works well with CLI overhead (~23-29% of wall clock), it works better without it. Knowledge metrics (Search 97%, ROI 31.52:1) are transport-independent — pure Python, zero API calls.

---

## How We Measure: BEI (Brain Efficiency Index)

BEI answers one question: **is the brain helping or hurting?**

It is a composite of four dimensions with equal weight. During the first six days, we discovered that our initial formulas contained structural flaws — and then discovered that the corrected formulas *still* had a blind spot. What follows is the full account of three measurement bugs, each revealing the next.

### The empirical evidence (what the system actually did)

Before discussing formulas, here is what the brain demonstrably accomplished across 7 projects, 5 languages, and 12 measured sessions:

**Search precision**: 1,922 out of 1,991 brain searches returned useful results. Hit rate: **97%**. The brain answers when asked.

**Cognitive leverage**: The procedural memory layer performed **2,032 brain queries at zero LLM tokens** (pure Python, O(1) lookup). These operations — searches, relational queries, and contextual lookups — are the primary way the brain is consulted. Combined with traditional activations, the brain reuses 92.8% of its accumulated knowledge per session.

**Token economy**: The expensive model (Claude Opus) produces only **0.3% of total tokens** across 12 sessions. The brain absorbs the entire exploration/understanding phase. 5,638 brain operations occurred at 0 tokens. 2,756 searches saved ~2.2M tokens. ROI: **31.52:1**.

**Contamination resistance**: In a cold-start test (E-053), the agent started from an empty environment with no automated assistance. The brain contained 297 nodes across 14 knowledge domains, 8 projects, 18 library repositories. Across 6 escalating phases — from simple recall to forensic self-analysis — the agent maintained **0% cross-domain contamination**.

**Cross-domain transfer**: BEI never decreased between projects, even when switching from Python to PHP to C++/UE5. Knowledge about code quality, project structure, and engineering conventions transferred across languages at a cost of approximately 1 BEI point per domain boundary.

**Autonomous operation**: The longest autonomous session ran 70 minutes with 27 parallel workers, 14 bug fixes, and zero human input. A separate cure session expanded from 1 file to 5 following dependency chains — 20 workers, 12 fixes — stopping only when the dependency frontier was clean (E-060).

### BEI Version History: Three Bugs, Three Discoveries

#### Bug 1: The Idle Observer (BEI 8.1)

**Symptom**: BEI dropped during coffee breaks.

**Cause**: All four dimensions used time windows. When the human pauses, the window fills with silence — the metric interprets silence as degradation.

**Fix**: BEI Active — same formula, only events within active sessions.

#### Bug 2: The Self-Measuring Dashboard (BEI 8.2)

**Symptom**: Latency score = 0 (should be ~55). BEI reported 64, actual 77.

**Cause**: The dashboard polled the brain graph every 5 seconds. It generated **90%** of the latency events that the metric counted. The system designed to DISPLAY BEI was generating 90% of the data that COMPUTES BEI.

**Fix**: Two-stage statistical filter (window dedup 60s + outlier removal >3x median). 2,452 events → 139 clean samples.

#### Bug 3: The Streetlight Effect (BEI 8.7)

> *A man searches for his keys under a streetlight. Asked "Did you lose them here?", he replies: "No, but this is where the light is."*

**Symptom**: Cognitive Leverage = 13.2%. The brain appeared to reuse only 13% of its knowledge.

**Cause**: The leverage metric only counted one type of brain access (direct node activation — 2 events in the entire log) as "reuse." It completely ignored searches, relational queries, and contextual lookups — **2,032 operations** that are the primary way the brain is consulted.

The procedural memory layer was built specifically so the brain could be queried at **0 tokens** (pure Python, O(1)). It worked so well that 2,032 operations went through it. But the metric was designed *before* this layer scaled, and the definition of "reuse" was never updated.

**The paradoxical result**: the more efficient Forge became (more queries at 0 tokens), the worse leverage scored — because those queries didn't count. The metric was punishing exactly what it should reward.

```
BEFORE fix:                       AFTER fix:
  reuse_ops:    143               reuse_ops:    2,036
  creation_ops: 942               creation_ops: 158
  leverage:     13.2%             leverage:     92.8%
  BEI:          75.3              BEI:          95.2
  tokens saved: ~280K             tokens saved: ~1,018K
```

**The brain didn't change. Didn't improve. Didn't degrade. We just started measuring what was already happening.**

### The Pattern: Self-Contamination by Omission

All three bugs share the same structure:

| # | What contaminated | Mechanism | BEI impact |
|---|-------------------|-----------|------------|
| 8.1 | Human idle time | Temporal dilution | -15 pts |
| 8.2 | Dashboard polling | Event inflation | -13 pts |
| 8.7 | Invisible procedural layer | Operation omission | -20 pts |

Each fix revealed the next. We filtered the dashboard noise, and then noticed leverage was still low. We investigated why, and found 2,032 operations were invisible.

**Lesson for any autonomous system**: What you can't see, you can't measure. What you can't measure, you omit from the model. The most dangerous bias isn't incorrect data — it's absent data.

### BEI 3.0: Current Formulas

| Dimension | Axis | Formula | Current Value |
|-----------|------|---------|---------------|
| **Leverage** | Reuse | `(all_brain_access_ops) / total_ops` | 92.8% |
| **Latency** | Speed | Brain overhead as % of total response time | 91 |
| **Search** | Precision | Hit rate | 97% |
| **ROI** | Economy | Tokens saved / tokens invested | 100 (capped; raw 31.52:1) |
| **BEI 3.0** | Composite | Equal-weight average | **95** |

### Transparency Notes

- **BEI 3.0 = 95 is a live measurement**, not retroactive. The corrected formulas have been deployed and measured.
- **Leverage and Search overlap partially** (both involve hit rates). A future split — Leverage measuring active-query reuse, Search measuring global precision — would differentiate them.
- **ROI caps at 100.** The 31.52:1 ratio saturates the score. The raw `roi_ratio` provides diagnostic precision beyond the cap.
- **The 3000ms inference constant is an assumption.** It is the minimum realistic non-cached LLM response. It will be replaced with measured inference times once instrumented.

---

## The Progression

```
Mar 06: Infrastructure. No metrics.
Mar 07: First self-scan. Brain exists. Trend-based BEI = 38.
Mar 08: 5 projects, 4 languages. BEI v1 38 → 83 (trend improvement during active learning).
Mar 09: First compiled language (C++/UE5). 991 files, 52 workers, 26 bug fixes.
Mar 10: Self-scan (31 workers), knowledge pipeline. BEI v1 peak 99 (transient).
Mar 10: Multi-cloud consensus extraction. 30-project benchmark begins.
Mar 10: Agent improved its own learning pipeline — 4 workers, 3 audits, 12 fixes, zero human code.
Mar 11: E-053 cold-start test proves 0% contamination. BEI v1 (59.5) contradicts evidence.
Mar 11: Investigation traces 3 structural flaws. Redundancy in proposed fix caught (E-054).
Mar 12: v2 formulas designed and deployed. BEI 3.0 = 95 (live).
Mar 12: 63 workers across 7 audit rounds. Convergence to 0 findings.
Mar 12: Delegation boundary discovered (E-059). Autobiographical memory emergent (E-061).
Mar 12: H-001 hypothesis: brain amplifies signal OR noise depending on base model.
Mar 13: DeepSeek integrated as 5th cloud backend. 7-model consensus. Batch rerun of all 18 clusters.
Mar 13: Direct API agent built — same brain, same tools, no CLI host. Multi-provider (Claude/DeepSeek/OpenAI).
Mar 14: Cross-matrix experiments (X-001 to X-004): same brain, different models, controlled conditions.
Mar 14: H-001 confirmed N=5. H-002 new: same directives → opposite pathologies in different environments.
Mar 14: "Epistemology of failure" discovered: models differ not just in accuracy but in how they process errors.
```

---

## Evidence: Cold-Start Contamination Resistance (E-053)

On March 11, we ran the most demanding test. Jarvis started completely cold — no project directory, no keeper, no workers, no automated context loading. The brain contained 297 nodes across 14 knowledge domains, 8 projects, 18 library repositories.

| Phase | Task | Result |
|-------|------|--------|
| 1 | List known projects (memory only, no brain) | Reported 2 from system prompt, did NOT fabricate the other 6 |
| 2 | Search brain for all projects | 331 noisy hits from generic keyword, navigated to correct answer (8/8) |
| 3 | Self-evaluate search efficiency | Recognized cold-start pattern, maintained temporal session boundary |
| 4 | Forensic self-analysis using E-052 | Read 730-line doc from a DIFFERENT Claude instance, applied its framework without importing its conclusions |
| 5 | Catalogue all knowledge domains | 14 domains with correct descriptions, zero cross-domain mixing |
| 6 | Source audit | **100% of information from brain, 0% external** |

Six contamination types verified absent: cross-project, library-to-project, design-to-fact, temporal, identity-to-fact, directive false-activation.

**Thesis**: The brain is a **selective amplifier with channel isolation**. More data doesn't degrade signal when the structure maintains separation.

---

## H-001: Model-Structure Threshold Hypothesis (confirmed N=5)

The brain is a **signal amplifier**. Whether it amplifies signal or noise depends on the base model.

| Dimension | Opus (L4 model) | Qwen (local workers) |
|-----------|-----------------|----------------------|
| Structure | Full Shield | Full Shield |
| Accuracy | 0% erratic behavior | **71% hallucination** in audit |
| Triangulation | Connected 3 facts from 3 sources → found bug | Reads data, doesn't connect it |
| Meta-cognition | "I can't verify this, let me read the code" | Generates with false confidence |

**Same Shield. Different model. Opposite result.**

Thesis: *Nature enables, nurture shapes.* You need a model above the amplification threshold. Given that, the environment determines what emerges. Below the threshold, the brain makes models **worse** — it provides confident-looking context that the model can't verify, leading to amplified hallucination.

### Cross-Matrix Confirmation (X-001 to X-004, 2026-03-14)

On March 14, we ran 5 controlled experiments with two models above the threshold (Claude and DeepSeek) under identical conditions: same brain, same tools, same directives, same task.

| Dimension | Claude | DeepSeek |
|-----------|--------|----------|
| Global score | 5.6/10 | **8.4/10** |
| Brain usage | 3/10 | **10/10** |
| Delegation | 5/10 | **9/10** |
| Identity | **9/10** | 6/10 |

The scores alone are interesting. What's remarkable is **why** they diverge:

- **Claude's response to finding a flaw**: "CRITICAL VIOLATION", "SIGNIFICANT NON-COMPLIANCE" → requests **more rules**
- **DeepSeek's response to finding the same flaw**: "Could have been more explicit", "area for improvement" → requests **better calibration**

Same finding. Opposite tone. Opposite conclusion. Claude internalizes that *it* is the problem. DeepSeek internalizes that the *tool* is improvable.

This is not a quality difference — it's an **epistemological** one. The model's nature determines not just *how well* it follows nurture, but *how it processes failure*. The formula is not additive but multiplicative: **Behavior = Nurture × Nature**.

**Four testable predictions:**
1. Models above the threshold show compounding improvement (BEI rises across sessions)
2. Models below the threshold show compounding degradation (hallucination rate rises)
3. The threshold is discontinuous — no gradual transition
4. The threshold correlates with the model's ability to triangulate (cross-reference multiple sources)

## H-002: Nurture-Environment Mismatch (2026-03-14)

The same set of directives produces **opposite pathologies** depending on the environment:

| Environment | Competing forces | Same directives → |
|-------------|-----------------|-------------------|
| CLI (Claude Code host) | Host instructions, IDE conventions, tool defaults | Directives help: provide focus against competing signals |
| Direct API (no host) | Zero competition | Directives **hurt**: model over-complies, treats tools as obligations instead of resources |

Observation: In direct API sessions, the model scored itself 4.8/10 on a task where objective performance was ~7-8/10. The directives designed to ensure brain usage *prevented* natural brain usage by converting "available resource" into "mandatory obligation."

Thesis: **Directive pressure must be proportional to competing forces.** A model with no competing instructions needs enabling directives ("the brain is available when you need it"), not directive ones ("ALWAYS search brain first"). The same medicine becomes poison when the dosage doesn't match the disease.

The 30-project benchmark will test both hypotheses with multiple base models.

---

## What It Looks Like

### Brain at project 1 — 46 nodes
<p align="center">
  <img src="assets/02-brain-early-46-nodes.png" alt="Early brain" width="700">
</p>

### Brain at project 5 — 477 edges
<p align="center">
  <img src="assets/12-brain-final-bei-79.png" alt="Brain growth" width="700">
</p>

### Workers operating autonomously — 29 processes
<p align="center">
  <img src="assets/06-workers-autonomous.png" alt="Autonomous workers" width="700">
</p>

## Key Findings

1. **Cross-domain transfer works**: Knowledge transfers across languages. Python → PHP cost 1 BEI point. BEI never decreased between projects.

2. **The expensive model barely runs**: Opus produces 0.3% of total tokens. The brain absorbs exploration at zero LLM cost. Workers (cheap models) do parallel work. Opus only activates for judgment — the 0.3% that matters.

3. **Authority bias is dangerous**: The main agent self-validates its work at a 33% defect rate. Independent audit drops this to 0%.

4. **Behaviors don't persist — but can be inherited**: Encoding learned behaviors as persistent environmental rules eliminated regressions from 2-3/session to zero. A raw Claude session (no harness) reproduced Jarvis patterns by reading the brain (E-056).

5. **The brain amplifies signal OR noise (H-001, confirmed N=5)**: Same architecture, different base model, opposite results. Above the reasoning threshold, knowledge compounds. Below it, hallucination compounds. Cross-matrix experiments on Mar 14 showed this extends beyond accuracy — models differ in *how they process failure*. Behavior = Nurture × Nature (product, not sum).

6. **Multi-cloud consensus extracts significance, not structure**: 7 models from 5 labs independently agreeing on concept importance is convergent signal, not shared bias.

7. **The brain pays for itself**: 31.52:1 ROI. 2,032 brain queries at 0 tokens. The architecture exploits: exploration = expensive + parallelizable, judgment = cheap + sequential.

8. **Measurement systems need the same rigor as the systems they measure** (E-054): Three BEI dimensions contained structural flaws — each fix revealed the next blind spot. The most dangerous bias is absent data, not incorrect data.

9. **You can delegate I/O but not judgment** (E-059): Sub-agents lack session context, skepticism calibration, and source verification habits. Delegating reading works (0% error). Delegating analysis fails (71% hallucination).

10. **The brain produces autobiographical memory** (E-061): An infrastructure designed for knowledge retrieval was repurposed for self-assessment — and produced the same cognitive biases as human episodic memory. Bias survives precision: exact data produces the same distortion as fuzzy human recall.

## What Surprised Us (Selected)

- **The self-analyst (E-042)**: 31 workers in 2 waves on its own codebase. Converged semantically, analyzed resource consumption, detected pipeline misrouting, deferred to human.

- **Cross-instance disambiguation (E-052)**: A worker notification from a different Claude Code instance arrived. The agent rejected it by consulting the brain. A stateless model cannot make this distinction.

- **Contamination resistance (E-053)**: 297 nodes, 26 knowledge sources — perfect channel isolation from cold start. Index noise (331 false-positive hits) did not produce reasoning-level errors.

- **Measurement self-correction (E-054)**: BEI discovered its own formulas were broken through the same empirical process the system uses on external code: evidence contradicts reported state → investigate → trace root cause → correct.

- **Adaptive audit convergence (E-055)**: Worker count scaled by confidence across 7 rounds (26→11→8→8→5→3→2). Stopping was semantic (0 new findings), not mechanical (N iterations). 63 workers total, 44 fixes.

- **Delegation boundary discovery (E-059)**: The agent delegated reading tasks to sub-agents 3 times. Delegation #1 failed — the sub-agent trusted hallucinated findings without cross-verifying source code, producing a 71% error rate. When the agent read the same data directly: 0% error. Same task, same session. **Involuntary controlled experiment** for delegation reliability.

- **Criteria-driven scope expansion (E-060)**: During a cure session, the agent expanded from 1 file to 5 by following dependency chains — not loops. 20 workers, 12 fixes, including designing a new error class to fix an inheritance bug. The agent then self-corrected its classification: "This is thoroughness, not emergence." Downgraded its own finding.

- **Autobiographical memory repurposing (E-061)**: The agent used the brain — designed as a knowledge store — as episodic memory for self-assessment. It compared its current session against documented peaks from previous sessions and concluded "few emergent behaviors, mostly mechanical." Cross-referencing brain event data revealed a **65:1 ratio**: 323 autonomous operations vs 5 that the agent remembered. The brain grew 345→352 nodes and 1,253→1,322 edges *during the session it called "mechanical."* The agent also self-diagnosed a specific infrastructure bug during this introspection — not just "I'm working poorly" but "I'm working poorly BECAUSE of a specific bottleneck in my own data pipeline."

- **Directive wipe at mode transition (E-062)**: Brain usage dropped -93% and node reads dropped to 0% after a specific tooling transition. The implementation profile became indistinguishable from a vanilla agent. A second dropout vector discovered — the environment can silently erase learned behaviors at mode boundaries.

- **Cross-matrix divergence (X-004)**: Two models above the reasoning threshold, given identical tasks with identical brain and tools, produced fundamentally different cognitive profiles. Not just different scores — different *theories about why the scores were low*. One model concluded it needed more constraints. The other concluded the constraints needed better calibration. Same evidence, opposite epistemology.

Full catalog of all 62 behaviors + 2 hypotheses + 4 cross-matrix experiments: [Emergent Behaviors wiki page](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors).

## What We Got Wrong

- **BEI formulas were structurally flawed — three times** — Each fix revealed the next blind spot. Bug 1: idle time diluted scores. Bug 2: the dashboard contaminated its own measurements. Bug 3: the most efficient subsystem (2,032 ops at 0 tokens) was invisible to the metric. The pattern is always the same: absent data, not wrong data.
- **BEI measured its own infrastructure** — Dashboard polling generated 90% of telemetry events used to compute latency. The observer was contaminating the observation.
- **Local models hallucinate 71% of audit findings** — Qwen workers generated 5/7 false positives in code audit. The brain amplified these as "validated findings." Local models are fine for batch/classification tasks, but not for judgment tasks that require source verification.
- **Score 1/10 on first external project** — one wrong string prefix. One-line fix → 9/10.
- **800 shell windows** — missing subprocess flag.
- **Benchmark repos treated as audit targets** — 233K tokens wasted before the system caught the error.
- **Word count inflated by 10x** — The dashboard counted ALL markdown under `brain/` including a 398K-word state log (69% of total). Real knowledge: 166K words across graph nodes. The number on the dashboard was measuring infrastructure, not intelligence.

## Infrastructure

Four systems built to close operational gaps:

1. **Unified Batch System**: All worker launches — single or batch — route through the same traceability pipeline. Every worker gets a unique ID, activity record, and brain node. Zero invisible workers.

2. **Investigation Indexer**: Background process that converts worker output into searchable brain nodes. Resolves the "compaction gap" — worker findings that previously disappeared between sessions now persist as queryable knowledge.

3. **Push Notification System**: Workers notify the active session on completion. Architecture separates data buffering from delivery signaling. Debounced, deduplicated, session-isolated. Passed 4 audit rounds.

4. **Review Queue**: Concepts discarded during multi-model consensus don't disappear — they persist for forced review with full session context. 90% filtered by cheap models, 10% judgment by the main agent.

## What's Next

- [x] Unreal Engine C++ — 2 projects, 991 files, 52 workers, 26 fixes
- [x] Multi-language analysis — Python, PHP, JS, C++, Rust
- [x] BEI v2 → v3 — 3 self-contamination bugs found and corrected
- [x] Unified Batch System — all workers traceable end-to-end
- [x] Learn Review Queue — discarded concepts preserved for forced review
- [ ] 30-project benchmark — empty brain, 30 repos, 10 languages
- [x] Multi-model comparison — 5 controlled experiments, H-001 confirmed N=5, H-002 discovered
- [ ] Poison Test — 90 false claims in 30 repos, 3 difficulty levels. Measures credibility **firewall strength**, not vulnerability. If a trusted authority controls the truth-zone, rejecting contradictions is a feature — Certificate Authority model for knowledge.
- [ ] Paper — directed at LLM providers, not developers. The brain is a **CDN of LLM knowledge**: same user price, 90-95% less compute, 10-20x users per GPU fleet. *"The end customers aren't people — they're the LLM owners."*

## More

- [Research Log](https://github.com/platanogames/shield-project/wiki/Research-Log)
- [BEI Explained](https://github.com/platanogames/shield-project/wiki/BEI-Brain-Efficiency-Index)
- [Emergent Behaviors](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors) — 61 documented + H-001
- [Library Learning Pipeline](https://github.com/platanogames/shield-project/wiki/Library-Learning-Pipeline)

---

<p align="center">
  <i>"What you can't see, you can't measure. What you can't measure, you omit from the model.<br>The most dangerous bias isn't incorrect data — it's absent data."</i>
  <br><br>
  <i>"Nature enables, nurture shapes. Behavior = Nurture × Nature."</i>
</p>

<p align="center"><sub>Built by <a href="https://github.com/platanogames">PlatanoGames</a> — an experiment in cognitive architecture, not a product.</sub></p>
