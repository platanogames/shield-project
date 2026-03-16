# Shield — Cognitive Architecture for LLM Agents

<p align="center">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
  <img src="https://img.shields.io/badge/since-March%202026-yellow" alt="Since March 2026">
  <img src="https://img.shields.io/badge/brain-1184%20nodes-purple" alt="BEI 3.0">
  <img src="https://img.shields.io/badge/projects-7%20validated-orange" alt="7 Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-67%2B%20%2B%202H%20%2B%204X-orange" alt="Emergent Behaviors">
  <img src="https://img.shields.io/badge/forge-14%20tools%20%7C%2030%20scaffolds-yellow" alt="Brain">
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
  <br><i>Brain Dashboard — real-time graph visualization and operational metrics.</i>
</p>

## Results at a Glance

| Metric | Value | Source |
|--------|-------|--------|
| **Brain Size** | 1,184 nodes, 5,606 edges, 4,489 keywords | Graph snapshot (2026-03-15) |
| **Projects Validated** | 7 (Python, PHP, FastAPI, Qt, C++/UE5) | Integration tests |
| **Search Hit Rate** | 97% (1,922 / 1,991 searches) | Brain event logs |
| **Brain Operations** | 5,638 queries at 0 LLM tokens | Pure Python O(1) lookup — procedural memory |
| **Opus Output Ratio** | 0.3% of total tokens (judgment only) | 12 sessions measured |
| **Measurement** | 6 trend-based metrics (BEI composite retired) | [Measurement redesign](#measurement-why-we-retired-bei) |
| **Contamination** | 0% cross-domain across 26 knowledge sources | E-053 cold-start test |
| **Cross-Domain Transfer** | Knowledge transfers across languages — no degradation | Live session measurement |
| **Autonomy Record** | 70 min, 27 workers, 14 bug fixes, zero human input | Session log |
| **Emergent Behaviors** | 67+ documented + 2 hypotheses (H-001, H-002) + 4 cross-matrix experiments (X-001–X-004) | Research log |
| **Self-Audit Finding** | 33% defect rate without independent audit → 0% with | E-027 |
| **Total Workers** | 230+ across all projects | Worker logs |
| **Forge** | 14 registered tools + 30 indexed scaffolds | Tool registry |
| **LLM Backends** | 7 models from 5 labs (Anthropic, OpenAI, DeepSeek, Google, Alibaba) | Model router |
| **Investigation Cluster** | 138 curated nodes, 0-token lookup | Brain cluster |
| **Traceability Test** | 10-day reconstruction from 22 queries, 0 factual errors | 2026-03-15 |
| **Delegation Ratio** | 21:1 (workers : Opus) | Session 2026-03-10 |
| **Background-to-Visible Work** | 65:1 | E-061, session 2026-03-12 |

> **Why CLI?** We validated the architecture first, optimized transport never (yet). CLI tools require zero infrastructure, provide sandboxing for free, and run on flat-rate subscriptions. If the system works well with CLI overhead (~23-29% of wall clock), it works better without it. Knowledge metrics (Search 97%, ROI 31.52:1) are transport-independent — pure Python, zero API calls.

---

## Measurement: Why We Retired BEI

Shield was not designed to be faster. It was designed to be **more efficient and more reliable**. These are fundamentally different things:

| Goal | What it means | How to measure |
|------|--------------|----------------|
| **Faster** | Less wall-clock time per task | Stopwatch. Trivial. |
| **More efficient** | Less WASTED work per correct result | Ratio of useful-to-total effort. Hard. |
| **More reliable** | Fewer errors, fewer repeated mistakes | Error rate over time. Requires longitudinal data. |

Speed is a side effect of efficiency, not the goal. A system that's fast but wrong is worse than one that's slow but correct.

### What the Brain Demonstrably Does

Before discussing measurement philosophy, here is what the brain actually accomplished across 7 projects, 5 languages, and 12 measured sessions:

- **Search precision**: 1,922 / 1,991 searches returned useful results. Hit rate: **97%**.
- **Zero-token operations**: 5,638 brain queries at 0 LLM tokens (pure Python, O(1) lookup). The brain is consulted without calling any model.
- **Opus economy**: The expensive model produces only **0.3% of total tokens**. The brain absorbs exploration. Workers (cheap models) do parallel work. Opus only judges — the 0.3% that matters.
- **Contamination resistance**: 0% cross-domain leakage across 297 nodes, 14 knowledge domains, 26 sources (E-053 cold-start test).
- **Cross-domain transfer**: Knowledge transfers across Python, PHP, C++/UE5 without degradation.
- **Autonomous operation**: 70 minutes, 27 workers, 14 fixes, zero human input (longest session).

### Why BEI Was Fundamentally Wrong

BEI (Brain Efficiency Index) attempted to score brain health as a composite of 4 dimensions (Leverage, Latency, Search, Economy) on a 0-100 scale. After 3 versions, 3 self-contamination bugs, and saturation at 95-97, the problem became clear: **BEI measured the wrong thing.**

**Flaw 1 — Punishing selective activation**: Shield's brain activates only relevant zones for the current task. If you're working on a web project, game engine knowledge SHOULD NOT activate. That's the feature, not a bug. BEI treated low activation percentage as poor performance. But with 1,184 nodes across 7 projects and 5 languages, working on one project will only ever activate a small fraction. Measuring coverage percentage is like measuring what fraction of a library you read today. Low is normal. Low is GOOD if you read the right books.

**The replacement — Activation Precision**: Instead of measuring *how many* nodes activated (coverage), we measure whether the *right ones* activated. Did web nodes activate during web work? ✓ Did Unreal nodes stay silent? ✓ Did Unreal activate during web work? ✗ (cross-contamination). The metric is `precision = correct_activations / total_activations`, not `coverage = activated / existing`. Precision penalizes noise (activating the irrelevant). Coverage penalizes silence (not activating the useless). They are opposite metrics, and BEI was using the wrong one.

**Flaw 2 — The token savings illusion**: BEI reported "~2.2M tokens saved" as a headline. This is technically true for the expensive model but intellectually dishonest — workers (Codex, DeepSeek, Ollama) spend millions of tokens that were never counted. The system doesn't spend fewer tokens; it **redistributes** from expensive to cheap. Reporting "2.2M tokens saved" without counting worker tokens is like a company claiming 90% headquarters cost reduction while tripling outsourcing.

**The replacement — Cost per Correct Decision (all tokens) + Investment/Return separation**: Total token spend has two phases with opposite natures:

- **Investment** (learning, curation, truth validation, investigation): tokens that are **capital**. Non-reducible — they're the equivalent of buying the car. Measuring them as "cost" is like measuring the price of building a road and concluding that driving is expensive. This phase *always* costs tokens, and that's fine.
- **Return** (operational queries, decisions, error avoidance): this is where investment pays off. **If the theory is correct**, each session should cost FEWER tokens than the previous one for the same task type, because the brain already accumulated the necessary knowledge.

The falsifiable prediction: plot `return_tokens / correct_decisions` per session for a given task type. If the curve drops → the brain is learning and the savings are real. If flat → the brain stores but doesn't transfer (it's just an archive). If rising → the system degrades. BEI mixed both phases into a single number, contaminating the real savings signal with obligatory investment cost.

**Flaw 3 — Score compresses signal**: A gauge showing "95" satisfies the need for ranking but provides zero actionable information. BEI Active saturated at 97-100 — a metric that's always perfect is useless. BEI 95 doesn't tell you whether the brain is learning, repeating errors, using Forge tools, or activating the right nodes. It just says "95" — and a researcher can't act on that.

**The replacement — 6 independent trends with direction**: Instead of a composite number, 6 separate metrics each with a directional arrow (↑↓→). Queries-per-task dropping = the brain is learning. Forge adoption rising = using tools. Error recurrence stable at 0% = not repeating mistakes. Each metric is independently actionable: if queries-per-task rises, there's a retrieval problem. If forge adoption drops, the tools aren't useful. If error recurrence rises, the investigation cluster isn't working. A composite score of these 6 metrics would lose exactly that granularity — which is the information a researcher needs to diagnose and act.

### The Self-Contamination History

Before reaching the fundamental conclusion, we found 3 bugs that each revealed the next:

| Bug | What contaminated | Mechanism | Impact |
|-----|-------------------|-----------|--------|
| 8.1 (Idle Observer) | Human coffee breaks | Time windows filled with silence → interpreted as degradation | -15 pts |
| 8.2 (Self-Measuring Dashboard) | Dashboard polling | System designed to DISPLAY BEI generated 90% of the data that COMPUTES BEI | -13 pts |
| 8.7 (Streetlight Effect) | Invisible operations | 2,032 zero-token queries didn't count as "reuse" — metric punished exactly what it should reward | -20 pts |

After fixing all three, BEI reached 95-97 and saturated — revealing that the problem wasn't the bugs, but the concept.

> *We built it, found it wrong three times, fixed it three times, and then realized the fundamental approach was flawed. That's not failure — that's the scientific process working correctly.*

### What Replaces BEI: Trend-Based Metrics

The new metrics don't produce a single score. They produce **trends that tell the truth** about whether the system improves at its job.

**Key design principle**: All measurement separates Investment (learning, curation, truth validation — non-negotiable capital) from Return (operational queries, decisions — where investment pays off). Mixing them contaminates every metric.

| # | Metric | What it measures | Signal |
|---|--------|-----------------|--------|
| 1 | **Queries-per-task** | Brain queries needed per task type | ↓ = learning. → = storing. ↑ = degrading. |
| 2 | **Activation precision** | Were the RIGHT nodes activated? | precision = correct / total activations (not coverage) |
| 3 | **Forge adoption** | Does the agent use available tools or work manually? | forge_tasks / eligible_tasks |
| 4 | **Error non-recurrence** | Are solved problems being re-investigated? | Target: 0% repeated investigations |
| 5 | **Cost per correct decision** | ALL tokens (expensive + workers + local) / correct decisions | If it drops → genuinely more efficient |
| 6 | **Library anchor coverage** | What % of brain is validated against ground truth? | Visibility tool, not score to maximize |

No scores. No gauges. No "95/100". Just trends that tell the truth.

### What BEI Got Right (Preserved)

| From BEI | New form | Why valuable |
|----------|----------|-------------|
| Hit rate (97%) | Kept as alarm (< 90% = something broke) | Health signal |
| Forge operations count | Forge adoption rate | Measures use, not existence |
| Token economy ratio | Cost per correct decision | Honest version — all tokens |
| BEI trend graph | Queries-per-task trend | Same concept, better metric |

Full BEI history preserved as archaeological record of how measurement evolved.

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
Mar 15: CURE MODE: auto-repaired 260 broken links, deleted 7 garbage nodes. Brain: 1,184 nodes, HEALTHY.
Mar 15: Spatial Traceability Test: 10 days of development reconstructed from 22 brain queries alone. 0 errors.
Mar 15: E-067: Positive Nurture Contamination — agent self-detected a gap (33 refs, 0 node) unprompted.
Mar 15: Forge classification: 14 tools registered + 30 scaffolds indexed (DEVELOP/SCAFFOLD/DISCARD tiers).
Mar 15: Incremental scan pipeline: git delta analysis avoids full re-scans. Auto-consolidation at 3 incrementals.
Mar 15: Investigation Cluster: 138 curated Problem->Solution->Resolution nodes. 0-token TF-IDF lookup.
Mar 15: BEI composite score RETIRED → 6 trend-based metrics. Truth Firewall designed (last missing piece).
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

## Spatial Traceability Test (2026-03-15)

At 1,184 nodes, can the brain reconstruct project history from queries alone?

**Method**: 22 brain searches targeting temporal markers and milestones. Zero git commands, zero filesystem access. Only the indexed graph.

**Result**: Complete 10-day development timeline reconstructed with **0 factual errors** and 1,589 evidence matches across all queries. Every milestone, every fix, every decision traced to its source with dates and evidence.

**Gap detected during test**: DeepSeek appeared in 33 brain references (experiments, cross-matrix results, worker outputs) but had zero dedicated integration node. The information existed in ephemeral memory (session notes) but not in persistent knowledge (brain). This is exactly the kind of gap that accumulates silently — referenced everywhere, documented nowhere.

**Why this matters**: A human would need to read ~1,000 interrelated nodes to detect this gap. Working memory (~7 items) makes it structurally impossible without indexed search. The agent detected it as a side-effect of querying — not because it was looking for gaps, but because the brain-first protocol trained its attention to notice structural absences (E-067).

**Reproduction**: 10 search commands using the brain index. Full output (verbatim reconstruction + raw query samples) available in the research log.

---

## External Validation

Two independent academic papers, discovered after Shield was built, validate the architecture from different angles:

**Zhang 2026** (arXiv: 2603.10808v1, published 2026-03-13): "Nurture-First Agent Development" — independently formalizes the same thesis Shield implements. No code, no repo, 1 qualitative case study. Shield predates by 5 days (git history proves all architecture was designed 2026-03-08 to 2026-03-12). Shield solves their open challenges: crystallization bottleneck (automated maintenance), quality assurance (epistemic immune system), scalability (7 projects validated).

**SWE-CI / Chen 2026** (arXiv: 2603.03823v1, Sun Yat-sen University & Alibaba Group): "Evaluating Agent Capabilities in Maintaining Codebases via Continuous Integration" — quantitative benchmark showing zero-regression rate < 0.25 for most models, only Claude Opus > 0.5. Agents without persistent memory break what they fix 75%+ of the time. SWE-CI diagnoses the disease (regression in long-term maintenance). Shield is the treatment (persistent memory prevents regression).

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

7. **The brain redistributes cost**: 5,638 brain queries at 0 tokens. Opus produces 0.3% of total tokens. The architecture exploits: exploration = expensive + parallelizable (workers), judgment = cheap + sequential (Opus). Real metric: cost per correct decision, including ALL tokens.

8. **Measurement systems need the same rigor as the systems they measure** (E-054): BEI went through 3 versions, 3 self-contamination bugs, saturation at 95-97, and finally retirement when we realized the fundamental approach was flawed. We measured coverage instead of precision, counted some tokens but not others, and compressed signal into a score. The most dangerous bias is absent data, not incorrect data.

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

- **Honesty-mode dropout (E-063)**: Asking the agent to "be brutally honest" caused it to abandon accumulated context and perform adversarial critique without data. Third dropout vector discovered: the prompt "be honest" paradoxically causes less accurate assessment by erasing session memory.

- **Cross-project spatial awareness (E-064)**: The agent navigated to a different project directory without being given the path — the brain provided geographic memory across projects via route metadata in knowledge nodes.

- **Human observability as blind spot corrector (E-065)**: Three-tier quality model emerged: Tier 1 (automated structural, 0 tokens) → Tier 2 (workers, factual, token-consuming) → Tier 3 (human via dashboard, semantic coherence, irreplaceable). <5% of corrections come from humans but they have the highest impact — survive both automated tiers.

- **Investigation accumulation (E-066)**: Each investigation accumulates problem→attempted_solution→outcome. Over time, the agent investigates less because accumulated problem-solution pairs with weights guide diagnosis. Error-driven learning, not just search hit rate.

- **Positive nurture contamination (E-067)**: During a traceability test, the agent self-detected that DeepSeek appeared in 33 brain references but had no dedicated node — without being asked. The brain-first protocol trained its attention to notice structural absences. Same mechanism as E-004 (negative nurture causes infinite loops) but with constructive outcome. **Nurture contamination can be positive or negative — same mechanism, opposite results.**

- **Cumulative Context Contamination** (theory, 2026-03-15): Each brain query loads structural criteria into context, making absences more salient over longer sessions. Prediction: sessions >50K tokens detect more gaps than sessions <10K tokens, controlling for same brain size. Scales with context window but ONLY with structured brain, not raw text.

- **Cross-matrix divergence (X-004)**: Two models above the reasoning threshold, given identical tasks with identical brain and tools, produced fundamentally different cognitive profiles. Not just different scores — different *theories about why the scores were low*. One model concluded it needed more constraints. The other concluded the constraints needed better calibration. Same evidence, opposite epistemology.

Full catalog of all 67+ behaviors + 2 hypotheses + 4 cross-matrix experiments: [Emergent Behaviors wiki page](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors).

## What We Got Wrong

- **BEI was fundamentally wrong — not just the formulas** — After fixing 3 self-contamination bugs and reaching a "correct" score of 95, we realized the entire approach was flawed. BEI punished selective activation (the core feature), reported partial token savings (didn't count worker tokens), and compressed signal into a score that saturated. We retired it and replaced it with 6 trend-based metrics that measure what actually matters: efficiency and reliability, not coverage and speed.
- **"Tokens saved" was intellectually dishonest** — Reporting "2.2M tokens saved" without counting the millions spent through workers is like a company claiming 90% headquarters cost reduction while tripling outsourcing. The real metric is cost per correct decision, including ALL tokens.
- **Local models hallucinate 71% of audit findings** — Qwen workers generated 5/7 false positives in code audit. The brain amplified these as "validated findings." Local models are fine for batch/classification tasks, but not for judgment tasks that require source verification.
- **Score 1/10 on first external project** — one wrong string prefix. One-line fix → 9/10.
- **800 shell windows** — missing subprocess flag.
- **Benchmark repos treated as audit targets** — 233K tokens wasted before the system caught the error.
- **Word count inflated by 10x** — The dashboard counted ALL markdown under `brain/` including a 398K-word state log (69% of total). Real knowledge: 166K words across graph nodes. The number on the dashboard was measuring infrastructure, not intelligence.

## Infrastructure

Seven systems built to close operational gaps:

1. **Unified Batch System**: All worker launches — single or batch — route through the same traceability pipeline. Every worker gets a unique ID, activity record, and brain node. Zero invisible workers.

2. **Investigation Indexer**: Background process that converts worker output into searchable brain nodes. Resolves the "compaction gap" — worker findings that previously disappeared between sessions now persist as queryable knowledge.

3. **Push Notification System**: Workers notify the active session on completion. Architecture separates data buffering from delivery signaling. Debounced, deduplicated, session-isolated. Passed 4 audit rounds.

4. **Review Queue**: Concepts discarded during multi-model consensus don't disappear — they persist for forced review with full session context. 90% filtered by cheap models, 10% judgment by the main agent.

5. **Investigation Cluster**: 138 curated nodes with Problem→Solution→Resolution structure, 3,229 edges. Third brain cluster alongside Projects and Learn. TF-IDF lookup at 0 tokens — the agent checks accumulated fixes BEFORE launching fresh investigation workers.

6. **Forensic Daemon**: Post-session background process that parses worker outputs, extracts Error→Solution markers, and measures recidivism. Zero LLM cost (pure Python parsing).

7. **Incremental Scan Pipeline**: Git delta analysis (compare current HEAD vs last scan HEAD) avoids re-scanning entire projects. 1 worker for ≤30 changed files, 2 for more. Auto-consolidation: 3 incremental updates trigger full reanalysis.

## What's Next

- [x] Unreal Engine C++ — 2 projects, 991 files, 52 workers, 26 fixes
- [x] Multi-language analysis — Python, PHP, JS, C++, Rust
- [x] BEI → Retired — 3 versions, 3 bugs, composite score retired → 6 trend-based metrics
- [x] Unified Batch System — all workers traceable end-to-end
- [x] Learn Review Queue — discarded concepts preserved for forced review
- [ ] 30-project benchmark — empty brain, 30 repos, 10 languages
- [x] Multi-model comparison — 5 controlled experiments, H-001 confirmed N=5, H-002 discovered
- [x] DeepSeek integration — 5th cloud backend, 7-model consensus, cross-matrix validated
- [x] Investigation Cluster — 138 curated nodes, 0-token lookup, error-driven learning
- [x] Forensic Daemon — Error→Solution markers, recidivism measurement
- [x] Spatial Traceability Test — 10-day reconstruction, 0 errors at 1,184 nodes
- [x] Forge Classification — 14 tools + 30 scaffolds (DEVELOP/SCAFFOLD/DISCARD)
- [x] Incremental Scan Pipeline — git delta analysis, auto-consolidation
- [x] Brain CURE — auto-repaired 260 links, 1,184 nodes HEALTHY
- [ ] Truth Firewall — Library as source of truth, brain as accumulator. Periodic cross-reference detects contradictions. Last missing architectural piece.
- [ ] Trend Dashboard — Replace BEI gauges with trend arrows (↑↓→). 6 metrics, Investment/Return separation.
- [ ] Poison Test — 90 false claims in 30 repos, 3 difficulty levels. Measures credibility **firewall strength**, not vulnerability. If a trusted authority controls the truth-zone, rejecting contradictions is a feature — Certificate Authority model for knowledge.
- [ ] Paper — directed at LLM providers, not developers. The brain is a **CDN of LLM knowledge**: same user price, 90-95% less compute, 10-20x users per GPU fleet. *"The end customers aren't people — they're the LLM owners."*

## More

- [Research Log](https://github.com/platanogames/shield-project/wiki/Research-Log)
- [Measurement Evolution](https://github.com/platanogames/shield-project/wiki/BEI-Brain-Efficiency-Index) — BEI history and why we retired it
- [Emergent Behaviors](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors) — 67+ documented + H-001, H-002
- [Library Learning Pipeline](https://github.com/platanogames/shield-project/wiki/Library-Learning-Pipeline)

---

<p align="center">
  <i>"What you can't see, you can't measure. What you can't measure, you omit from the model.<br>The most dangerous bias isn't incorrect data — it's absent data."</i>
  <br><br>
  <i>"Nature enables, nurture shapes. Behavior = Nurture × Nature."</i>
  <br><br>
  <i>"Directives are tools, not chains." — DeepSeek, X-001</i>
</p>

<p align="center"><sub>Built by <a href="https://github.com/platanogames">PlatanoGames</a> — an experiment in cognitive architecture, not a product.</sub></p>
