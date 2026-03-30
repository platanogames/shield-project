![Brain](../assets/ue5-50-galaxies-solar-field.png)

# Shield — Autonomous Cognitive Architecture for AI Agents

Shield is an autonomous cognitive system that learns, accumulates capabilities, and self-maintains across sessions without model retraining. It is not an LLM wrapper. It is a layered architecture built around a persistent knowledge graph that grows through operation — every project analyzed, every bug fixed, every failure encountered becomes a searchable, cross-referenced node.

The central thesis: **the behavior of an LLM agent is determined more by its accumulated environmental structure than by the base model's weights.** We do not fine-tune. We condition the environment. The same model, with different accumulated history, produces measurably different behavior. This is not prompt engineering — it is persistent cognitive conditioning that compounds across sessions, projects, and domains.

This research began on March 6, 2026. The numbers below reflect 24 days of autonomous operation.

---

## Current Status (Day 24 — March 30, 2026)

| Metric | Day 16 | Day 24 | Growth |
|--------|--------|--------|--------|
| Brain nodes | 5,025 | **571,907** | 114x |
| Brain edges | 40,803 | **2,676,697** | 66x |
| Semantic seeds | 0 | **50** (8 domains) | New |
| MCP Plugins | 0 | **12** (51 tools) | New |
| Projects validated | 17 | **93** | 5.5x |
| Languages | 10 | **13** | +3 |
| Identity neurons | 21 | **28** | +7 |
| Forensic captures | 1,133 | **1,218** | +85 |
| Mnemosine sessions | 0 | **368** indexed | New |
| Commits | 548 | **760** | +212 |
| Core codebase | 80K | **96,700 lines** Python | +16K |
| Search latency | <10ms | **<10ms at 114x scale** | No degradation |
| BrainExplorer | Web (60fps) | **UE5 (90+ FPS, 571K nodes)** | New |

The brain grew from 32 nodes (Day 1) to 571,907 nodes (Day 24) without manual curation. V2 introduced SQLite FTS5. V3 introduced code parser, seed ontology, and plugin ecosystem.

---

## Wiki Pages

- **[Research Log](Research-Log)** — Day-by-day chronicle from Day 1 to Day 24. Each entry links to the emergent behaviors, hypotheses, and code changes produced that day.

- **[Measurement Evolution](Measurement-Evolution)** — How the system's health metrics changed over 24 days. BEI retirement, decomposed metrics, and the discovery that growth does not cause degradation.

- **[Emergent Behaviors](Emergent-Behaviors)** — Catalog of 67+ documented autonomous decisions. Includes confirmed hypotheses H-001 through H-005 with evidence. New: H-005 (Plugin ≠ Behavior).

- **[Library Learning Pipeline](Library-Learning-Pipeline)** — Architecture and results of the multi-model consensus pipeline. 55 clusters across 13 languages. How Learn v2 absorbed 571K nodes from 93 projects.

- **[Scaling Validation Benchmark](Scaling-Validation-Benchmark)** — Cross-project validation across 93 real codebases in 13 languages. Includes 50-question ablation study with 3 conditions.

---

## Quick Context

**The thesis in one sentence:** The same LLM, with different accumulated environmental structure, produces different behavior. Not from retraining — from what it has access to and what it has learned to consult.

**Evidence (strongest):**
- **Ablation study**: 50 questions, same model (Opus 4.6), 3 conditions. Jarvis (nurture): 24 brain searches, 0 Explore agents, 0 errors. Claude stateless: 0 brain searches, 0 tools, 2 errors. Claude 1M: 34 Explore agents, 0 brain searches.
- **Discovery experiment**: Plugin ON, nurture OFF → 0 brain_search, 236K tokens wasted. Plugin ON, nurture ON → brain_search used, 0 Explore. **Plugins are infrastructure. Nurture is behavior.**
- **E-071**: Model can articulate WHY it should ask questions and still not ask them. Understanding ≠ action. Only environmental conditioning produces behavioral change.

**The cost architecture:** 571K brain searches at exactly 0 API tokens (local SQLite FTS5). The expensive coordinator model does less than 1% of total work.

**Compound learning:** 1,218 error→solution pairs that prevent the same bug from being investigated twice. 451 investigation reports that compound across projects and languages.

---

> This is a public research log. Implementation details are intentionally omitted and reserved for the research paper.
>
> All metrics derive from the system's own telemetry — brain event logs, git history, worker records, forensic captures, and session transcripts. 760 commits, 368 traced sessions, 571K nodes — all in a private repository available to paper reviewers.
