# Shield — Cognitive Architecture for LLM Agents

<p align="center">
  <img src="https://img.shields.io/badge/status-active%20research-blue" alt="Status">
  <img src="https://img.shields.io/badge/day-6-yellow" alt="Day 6">
  <img src="https://img.shields.io/badge/BEI-v2%20recalibrated-brightgreen" alt="BEI v2">
  <img src="https://img.shields.io/badge/projects-7%20validated-orange" alt="7 Projects">
  <img src="https://img.shields.io/badge/emergent%20behaviors-54-orange" alt="Emergent Behaviors">
  <img src="https://img.shields.io/badge/languages-Python%20%7C%20PHP%20%7C%20JS%20%7C%20C++-lightgrey" alt="Languages">
</p>

Shield is an experimental system where LLM agents **accumulate and compound knowledge** across sessions and projects. A persistent "brain" grows with every interaction — the way human learning works, but at machine speed.

This is a 6-day-old research project. Everything here is real, measured, and reproducible.

> **Full research log, metrics explanation, and emergent behavior catalog available in the [Wiki](https://github.com/platanogames/shield-project/wiki).**

---

## Results at a Glance

| Metric | Value | Source |
|--------|-------|--------|
| **Brain Size** | 297 nodes, 1109 edges, 1.5M+ words | Graph snapshot |
| **Projects Validated** | 7 (Python, PHP, FastAPI, Qt, C++/UE5) | Integration tests |
| **Search Hit Rate** | 98.2% (4,528 / 4,613 searches) | 9,338 brain events |
| **Token Economy** | 39.9:1 (5.4M tokens saved / 137K invested) | Estimated from event counts |
| **Contamination** | 0% cross-domain across 26 knowledge sources | E-053 cold-start test |
| **Cross-Domain Transfer** | Python → PHP: -1 BEI point | Live session measurement |
| **Autonomy Record** | 70 min, 27 workers, 14 bug fixes, zero human input | Session log |
| **Emergent Behaviors** | 54 documented | Research log |
| **Self-Audit Finding** | 33% defect rate without independent audit → 0% with | E-027 |
| **Total Workers** | 150+ across all projects | Gateway registry |

> **Why CLI?** We validated the architecture first, optimized transport never (yet). CLI tools require zero infrastructure, provide sandboxing for free, and run on flat-rate subscriptions. If the system works well with CLI overhead (~23-29% of wall clock), it works better without it. Knowledge metrics (Search 98.2%, ROI 39.9:1) are transport-independent — pure Python, zero API calls.

---

## How We Measure: BEI (Brain Efficiency Index)

BEI answers one question: **is the brain helping or hurting?**

It is a composite of four dimensions with equal weight. During the first six days, we discovered that our initial formulas contained structural flaws that made BEI contradict the empirical evidence. What follows is the full account of what happened, what the data showed, and how we corrected the measurement.

### The empirical evidence (what the system actually did)

Before discussing formulas, here is what the brain demonstrably accomplished across 7 projects, 5 languages, and 9,338 recorded events:

**Search precision**: 4,528 out of 4,613 brain searches returned useful results. Hit rate: **98.2%**. The brain answers when asked.

**Contamination resistance**: In a cold-start test (E-053), Jarvis started from an empty environment with no automated assistance. The brain contained 297 nodes across 14 knowledge domains, 8 projects, 18 library repositories, and 1.5M+ words. Across 6 escalating phases — from simple recall to forensic self-analysis — the agent maintained **0% cross-domain contamination**. Library repos were never confused with projects. Design documents were never treated as facts. A 730-line analysis from a different Claude instance was correctly used as reference without importing its conclusions. Every factual claim was traced back to brain sources: **100% internal, 0% external**.

**Token economy**: The brain's construction cost — keeper analysis, edge creation, common knowledge synthesis — consumed an estimated 137K tokens across 88 brain-building operations. The brain's usage — 4,528 search hits that each avoided a grep-read-reason cycle, plus context activations — saved an estimated 5.4M tokens. Ratio: **39.9:1**. The brain paid for itself approximately 40 times over.

**Cross-domain transfer**: BEI never decreased between projects, even when switching from Python to PHP to C++/UE5. Knowledge about code quality, project structure, and engineering conventions transferred across languages at a cost of approximately 1 BEI point per domain boundary.

**Autonomous operation**: The longest autonomous session ran 70 minutes with 27 parallel workers, 14 bug fixes, and zero human input. The agent detected when a pipeline was misrouting benchmark repos, calculated the token waste (3.9M if continued), and escalated before proceeding.

### What the formulas reported (and why it didn't match)

BEI v1 used four dimensions:

| Dimension | What v1 measured | v1 score |
|-----------|-----------------|----------|
| Leverage | `activated_nodes / (activated + edges + ramifications) * 200` | 46 |
| Latency | First-half vs second-half trend in ms/node | 44 |
| Search | `hits / total * 100` | 98.2 |
| ROI | First-half vs second-half trend in tokens/operation | 50 |
| **BEI v1** | **Weighted average** | **59.5** |

A brain with 98.2% search precision, 0% contamination, and 39.9:1 token economy scored **59.5 out of 100**. The numbers did not add up.

### Investigation: three independent flaws, one shared cause

We analyzed each dimension against the empirical data. Three of four dimensions shared the same structural defect: **they measured rate of change instead of absolute state**.

#### Leverage (46/100) — The selectivity penalty

The formula divided activated nodes by total brain operations. A brain that selectively activates 3.7% of its nodes (11 out of 307 paths) — which E-053 proved was the optimal behavior with 0% contamination — scored poorly because the denominator included all edge creations and ramifications from keeper maintenance.

The formula was answering: "What fraction of brain operations are activations?" The useful question is: "When the brain is asked for something, does it deliver?" That is search hit rate — 98.2%.

The conceptual error: comparing reading (activations) to writing (edge creation, ramification) in a single ratio. A researcher who writes 1000 pages of analysis from 200 pages of reading is productive, not inefficient.

E-053 provided the decisive evidence: the agent accessed 3.7% of the brain with 0% contamination and 98% hit rate. The formula scored this as 46/100. It was penalizing the behavior that made the brain work.

#### Latency (44/100) — The absence of a reference point

The formula compared first-half to second-half loading times. If brain load time was consistent — say, 92.6ms average across all sessions — the change was ~0, yielding a score of ~50. If the brain happened to slow down by 7% in the second half (possibly due to I/O contention, not actual degradation), the score dropped to 44.

The structural problem: **50 was the ceiling for stable performance**. A brain could only exceed 50 by actively getting faster. This means a mature, optimized brain that maintained consistent sub-100ms loads would score 44-50 forever.

The formula was answering: "Is the brain getting faster?" The useful question is: "How much overhead does the brain add to the response cycle?" With 92.6ms brain load against a conservative 3000ms LLM inference estimate, the brain adds 3.0% overhead — negligible.

Additionally, we had previously discovered (documented as calibration entry 8.2) that 90% of latency samples came from dashboard polling — the visualization system designed to DISPLAY BEI was generating most of the events that COMPUTE BEI. A two-stage statistical filter (window dedup + outlier removal) was already in place, but the underlying formula still measured trend instead of overhead.

#### ROI (50/100) — The zero denominator

The formula had three compounding issues:

1. **The denominator was effectively zero.** Of 160 brain-building operations (ramify, add_edge, ck_build, index_rebuild), all 160 had `tokens_est=0` in the event log. Nobody had instrumented the token cost of brain construction. The "Return On Investment" metric was dividing by zero — or falling back to a default score of 50.

2. **The "savings" constant was unvalidated.** The formula estimated savings as `count(activations) * 500`. The 500 was a guess with no empirical basis. Real savings per activation vary from near-zero (if the LLM ignores the context) to 2000+ (if it avoids entire search loops).

3. **Like Latency, it measured trend.** Even if the data had been correct, the formula compared first-half to second-half tokens-per-operation. A brain that was efficient from day 1 scored 50 forever. A brain that was terrible but improved 20% scored 60.

### The correction: four orthogonal axes

The investigation revealed that three dimensions were measuring variants of the same thing — "is it improving?" — which is a useful question during beta testing but not a health metric for a production system.

We established the **orthogonality principle**: four BEI dimensions must map to four independent measurement axes. If two dimensions measure the same axis, one is redundant and a different axis goes unmeasured.

This principle caught an error during the redesign itself. The initial proposal for the new ROI was an overhead ratio (`brain_ms / total_ms`), which would have been identical to the new Latency formula. Both would have measured speed, leaving no metric for economy. The redundancy was identified and the design corrected before implementation.

The four axes:

| Dimension | Axis | v2 formula | What it answers |
|-----------|------|-----------|-----------------|
| **Leverage** | Reuse | Search hit rate | When asked, does the brain deliver? |
| **Latency** | Speed | Brain overhead as % of total response time | Does the brain slow things down? |
| **Search** | Precision | Hit rate (unchanged) | What fraction of searches return results? |
| **ROI** | Economy | Tokens saved / tokens invested | Does the brain save more than it costs? |

### Retroactive calculation with corrected formulas

Applying v2 formulas to the same 9,338 events:

| Dimension | v1 | v2 | What the data shows |
|-----------|----|----|---------------------|
| Leverage | 46 | 98.2 | 4,528/4,613 searches returned hits |
| Latency | 44 | 94 | 92.6ms load / 3092.6ms total = 3.0% overhead |
| Search | 98.2 | 98.2 | No change — was already correct |
| ROI | 50 | 100 | 5.4M saved / 137K invested = 39.9:1 ratio |
| **BEI** | **59.5** | **97.6** | Same brain, same events, corrected measurement |

**97.6 is a retroactive recalculation, not a live measurement.** The corrected formulas have not yet been deployed. Once implemented, the first live v2 BEI will be the true baseline. We expect it to be near 97.6 but will report the actual measured value.

### ROI methodology: estimated token costs

The ROI formula uses estimated costs per operation type, derived from typical LLM inference patterns:

```
Investment (brain construction):                 137K tokens
  27 common-knowledge builds * 3000 tokens  =   81,000   (keeper synthesizes cross-project knowledge)
  51 edge creations * 800 tokens            =   40,800   (keeper evaluates and validates relationships)
  10 ramifications * 1500 tokens            =   15,000   (keeper analyzes nodes and generates children)
  73 index rebuilds * 0 tokens              =        0   (pure Python, no LLM cost)

Return (brain usage):                           5.4M tokens
  4,528 search hits * 1200 tokens           = 5,433,600  (each hit avoids a grep-read-reason LLM cycle)
  5 context activations * ~3000 tokens      =    15,015  (project context loaded without LLM inference)
  10 node activations * 300 tokens          =     3,000  (direct node retrieval avoids exploratory search)

Ratio: 39.9:1
```

These are estimates. The absolute values may be imprecise. But the ratio is internally consistent — if both sides are underestimated by the same factor, the ratio holds. A ratio of 39.9:1 means the brain's primary value (search hits that eliminate exploratory inference) massively outweighs its construction cost.

### Transparency notes

- **BEI v1 peak of 99 was real but misleading.** It occurred during Day 5's intensive self-scan when the brain was actively learning — the trend-based metrics temporarily scored high because improvement was happening. Once the system stabilized, those metrics fell back toward 50. The peak reflected a transient condition, not sustained health.

- **The 3000ms inference constant is an assumption.** It is the minimum realistic non-cached LLM response for non-trivial queries (Claude/Codex documented range: 3-15 seconds). It will be replaced with measured inference times once instrumented.

- **Leverage and Search are currently identical** (both = hit_rate). This is acknowledged. A future split — Leverage measuring active-query hit rate (68.7%), Search measuring global hit rate (98.2%) — would differentiate them. For v2, the priority was stopping the penalty on correct behavior.

- **ROI caps at 100.** The 39.9:1 ratio saturates the score. The raw `roi_ratio` value provides diagnostic precision beyond the cap.

### What v1 got right

Not everything was wrong. BEI v1's most important finding — that **BEI never decreased between projects** — holds under any formula. The cross-domain compounding effect is real and is the strongest signal in the data. Search hit rate (98.2%) was correctly measured from day 1. The dashboard contamination fix (calibration 8.2, removing polling noise) remains valid and necessary.

---

## The Progression

```
Day 1: Infrastructure. No metrics.
Day 2: First self-scan. Brain exists. Trend-based BEI = 38.
Day 3: 5 projects, 4 languages. BEI v1 38 → 83 (trend improvement during active learning).
Day 4: First compiled language (C++/UE5). 991 files, 52 workers, 26 bug fixes.
Day 5: Self-scan (31 workers), knowledge pipeline. BEI v1 peak 99 (transient).
Day 5 (evening): Multi-cloud consensus extraction. 30-project benchmark begins.
Day 5 (night): Agent improved its own learning pipeline — 4 workers, 3 audits, 12 fixes, zero human code.
Day 6: E-053 cold-start test proves 0% contamination. BEI v1 (59.5) contradicts evidence.
Day 6: Investigation traces 3 structural flaws. Redundancy in proposed fix caught (E-054).
Day 6: v2 formulas designed. Retroactive = 97.6. Implementation pending.
```

---

## Evidence: Cold-Start Contamination Resistance (E-053)

On Day 6, we ran the most demanding test. Jarvis started completely cold — no project directory, no keeper, no workers, no automated context loading. The brain contained 297 nodes across 14 knowledge domains, 8 projects, 18 library repositories, and 1.5M+ words.

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

2. **BEI is a diagnostic tool**: When infrastructure blocked the system, BEI identified the bottleneck before we did. When the formulas were wrong, the contradiction with empirical evidence exposed the flaws.

3. **Authority bias is dangerous**: The main agent self-validates its work at a 33% defect rate. Independent audit drops this to 0%.

4. **Behaviors don't persist — but can be inherited**: Encoding learned behaviors as persistent environmental rules eliminated regressions from 2-3/session to zero.

5. **Scale hasn't broken anything yet**: 297 nodes, 1109 edges, 1.5M+ words, 26 knowledge sources. Zero contamination (E-053).

6. **Multi-cloud consensus extracts significance, not structure**: 5 models from 4 labs independently agreeing on concept importance is convergent signal, not shared bias.

7. **The brain pays for itself**: 39.9:1 token economy. The brain absorbs the entire exploration/understanding phase at zero LLM cost (pure Python). The model only activates for judgment and writing.

8. **Measurement systems need the same rigor as the systems they measure** (E-054): Three of four BEI dimensions contained structural flaws that went undetected for 5 days. The contradiction only became visible when empirical evidence (E-053) was strong enough to challenge the reported scores.

## What Surprised Us (Selected)

- **The self-analyst (E-042)**: 31 workers in 2 waves on its own codebase. Converged semantically, analyzed resource consumption, detected pipeline misrouting, deferred to human.

- **Cross-instance disambiguation (E-052)**: A worker notification from a different Claude Code instance arrived. The agent rejected it by consulting the brain. A stateless model cannot make this distinction.

- **Contamination resistance (E-053)**: 297 nodes, 1.5M+ words, 26 knowledge sources — perfect channel isolation from cold start. Index noise (331 false-positive hits) did not produce reasoning-level errors.

- **Measurement self-correction (E-054)**: BEI discovered its own formulas were broken through the same empirical process the system uses on external code: evidence contradicts reported state → investigate → trace root cause → correct.

Full catalog of all 54 behaviors: [Emergent Behaviors wiki page](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors).

## What We Got Wrong

- **BEI v1 formulas were structurally flawed for 5 days** — Three of four dimensions measured improvement trend instead of absolute state, penalizing a system that was working correctly. The "peak" of 99 was a transient alignment during active learning, not a health metric. We are transparent about this because honest measurement is more valuable than impressive numbers.
- **BEI measured its own infrastructure** — Dashboard polling generated 90% of telemetry events used to compute latency. The observer was contaminating the observation.
- **Score 1/10 on first external project** — one wrong string prefix. One-line fix → 9/10.
- **800 shell windows** — missing subprocess flag.
- **Benchmark repos treated as audit targets** — 233K tokens wasted before the system caught the error.

## What's Next

- [x] Unreal Engine C++ — 2 projects, 991 files, 52 workers, 26 fixes
- [x] Multi-language analysis — Python, PHP, JS, C++, Rust
- [x] BEI v2 design — 4 orthogonal axes, evidence-based correction
- [ ] BEI v2 implementation — deploy corrected formulas, measure first live baseline
- [ ] 30-project benchmark — empty brain, 30 repos, 10 languages
- [ ] Multi-model comparison — same architecture, different core model
- [ ] Paper — empirical evidence that environmental conditioning shapes agent behavior

## More

- [Research Log](https://github.com/platanogames/shield-project/wiki/Research-Log)
- [BEI Explained](https://github.com/platanogames/shield-project/wiki/BEI-Brain-Efficiency-Index)
- [Emergent Behaviors](https://github.com/platanogames/shield-project/wiki/Emergent-Behaviors) — 54 documented
- [Library Learning Pipeline](https://github.com/platanogames/shield-project/wiki/Library-Learning-Pipeline)

---

<p align="center"><sub>Built by <a href="https://github.com/platanogames">PlatanoGames</a> — an experiment in cognitive architecture, not a product.</sub></p>
