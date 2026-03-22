![Brain](../assets/brain-explorer-5025-nodes.png)

# Shield — Autonomous Software Analysis System

Shield is an autonomous cognitive system that learns, accumulates capabilities, and self-maintains across sessions without model retraining. It is not an LLM wrapper. It is a layered architecture built around a persistent knowledge graph that grows through operation — every project analyzed, every bug fixed, every failure encountered becomes a searchable, cross-referenced node.

The central thesis: **the behavior of an LLM agent is determined more by its accumulated environmental structure than by the base model's weights.** We do not fine-tune. We condition the environment. The same model, with different accumulated history, produces measurably different behavior. This is not prompt engineering — it is persistent cognitive conditioning that compounds across sessions, projects, and domains.

This research began on March 6, 2026. The numbers below reflect 16 days of autonomous operation.

---

## Current Status (Day 16 — March 22, 2026)

| Metric | Value |
|--------|-------|
| Brain nodes | **5,025** (40,803 edges, 1.05M words) |
| Search engine | **SQLite + FTS5** — <10ms, 0 API tokens per query |
| Cognitive leverage | **96%** (tokens saved via brain reuse) |
| Emergent behaviors documented | **67+** |
| Workers launched | **800+** across 17 projects |
| Languages validated | **10** (Python, C++, C, PHP, JS, TS, Rust, Go, Java, Kotlin) |
| Library clusters | **28** via multi-model consensus |
| Forensic captures | **1,133** error→solution pairs |
| Commits | **548** in 16 days |
| Core codebase | **80,712 lines** Python |
| Cost per session | **<$0.50** (expensive model does <1% of work) |

The brain grew from 32 nodes (Day 1) to 5,025 nodes (Day 16) without manual curation. Every node was created by autonomous daemons. V2 migrated the brain backend from JSON to SQLite with FTS5 full-text search.

---

## Wiki Pages

- **[Research Log](Research-Log)** — Day-by-day chronicle of sessions, experiments, and key decisions. Each entry links to the emergent behaviors, hypotheses, and code changes produced that day.

- **[Measurement Evolution](Measurement-Evolution)** — How the system's health metrics changed over 16 days. Covers BEI (Brain Efficiency Index) retirement after 8 calibration rounds, the observer effect that contaminated it, and the decomposed replacement metrics.

- **[Emergent Behaviors](Emergent-Behaviors)** — Catalog of 67+ documented autonomous decisions: unplanned, unprogrammed behaviors observed during real operation. Includes confirmed hypotheses H-001 through H-005 with evidence.

- **[Library Learning Pipeline](Library-Learning-Pipeline)** — Architecture and results of the multi-model consensus pipeline. 28 library clusters across 10 languages. How hallucination is structurally prevented: a single model's output cannot create a brain node.

- **[Scaling Validation Benchmark](Scaling-Validation-Benchmark)** — Cross-project validation across 17 real codebases in 10 languages. Audit scores, worker counts, bugs fixed, and behavior observations per project.

---

## Quick Context

**The thesis in one sentence:** The same LLM, with different accumulated environmental structure, produces different behavior. Not from retraining — from what it has access to and what it has learned to consult.

**Evidence:**
- **E-034**: Same configuration → erratic behavior in one session set, correct behavior in another. The difference was accumulated failure documentation. Failure history shapes behavior more than positive directives.
- **E-056**: A raw LLM session with no harness reproduced the orchestrator's behavioral patterns simply by reading the brain. The environment transfers behavior across instances.
- **H-001** (N=5): Capable model + brain = enhanced performance. Weak model + brain = hallucination amplification. The brain amplifies whatever the model provides — signal or noise.
- **H-002** (confirmed empirically): Same directives cause opposite pathologies in different environments. Same model behaves differently depending on the execution harness. Behavioral compliance is environmental, not intrinsic.

**The cost architecture:** Thousands of brain searches at exactly 0 API tokens (local indexed search). The expensive coordinator model does less than 1% of total work.

**Why 21% of the brain is error-driven:** The system captures its own failures as searchable, cross-referenced knowledge nodes (1,042 error+investigation nodes, plus 1,133 forensic captures). Each node contains: problem, solution, file, line, severity, and confidence. The system learns from what it gets wrong, not just what it gets right.

---

> This is a public research log. Implementation details are intentionally omitted.
>
> Design documents, commit history, and the emergent behavior log provide full traceability from initial hypothesis (Day 1) through empirical confirmation (Days 4-13). All metrics derive from the system's own telemetry — brain event logs, git history, worker records, and forensic captures.
