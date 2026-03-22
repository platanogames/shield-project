# Library Learning Pipeline

Shield learns from two distinct sources. The first is experience: working on
real projects, making mistakes, and encoding the outcomes into the brain. The
second is study: systematically reading curated libraries and documentation and
converting them into structured knowledge nodes before any project requires that
knowledge.

The Library Learning Pipeline implements the second pathway. It is Shield's
equivalent of deliberate study — the way a surgeon reads anatomy before
operating. Both knowledge types coexist in the same brain, but with different
epistemological weights: experience always outranks theory.

![Library clusters](../assets/fig-library-clusters.png)

*28 library clusters processed as of 2026-03-22, spanning 10 programming languages.
Each bar represents the number of brain nodes produced per cluster after multi-model
consensus filtering. 3,458 library nodes total. UE5 (115K files) is the largest
target currently being absorbed.*

---

## What the Pipeline Does

The pipeline takes a folder of source code or documentation and produces a
collection of **brain nodes** — structured markdown files with YAML frontmatter
that live in `brain/library/` and are indexed alongside project knowledge.

Each brain node represents one validated concept: an API pattern, an
architectural decision, a behavioral characteristic of the library. The node
contains a summary, tags, relations to other concepts, and full provenance
metadata showing which models agreed on it and at what confidence level.

The process is sequential:

1. **Reconnaissance** — pure Python scan; classifies files, measures sizes,
   detects languages. Zero LLM calls. This phase never hallucinates.

2. **Multi-model consensus extraction** — source files are split into chunks
   and each chunk is dispatched simultaneously to all available models. A
   concept survives only if at least two independent models independently
   propose it.

3. **Quality gate** — validated concepts pass through seven sequential filters
   (summary length, noise patterns, near-duplicate detection, cap enforcement,
   type validation, tag pruning). Concepts that fail are either discarded or
   written to a review queue for future recovery.

4. **Node writing** — surviving concepts are written as brain nodes with full
   graph edges, hub index node, and provenance metadata.

5. **Optional enrichment** — an enrichment pass deepens summaries and
   resolves cross-cluster links.

---

## 7-Model Consensus: Why It Prevents Hallucination

The core mechanism that separates this pipeline from single-model extraction is
**cross-model consensus across models from four independent training lineages**.

![Consensus](../assets/learner-7-model-consensus.png)

*The 7-model consensus pool. Each concept must be independently proposed by at
least 2 models to survive. Four independent training lineages ensure
uncorrelated biases that cancel each other.*

### The Condorcet Argument

The theoretical foundation is Condorcet's Jury Theorem (1785): if each
independent judge has a probability greater than 50% of being correct, the
probability that the majority is correct approaches 100% as independent judges
are added.

Applied to LLMs: three different models at approximately 75% individual accuracy
yield:

| Judges | Mechanism | Estimated Confidence |
|--------|-----------|---------------------|
| 1 model alone | no check | ~75% |
| 2/3 consensus | majority | ~84% |
| 3/3 consensus | unanimous | ~92% |

**The critical constraint is independence.** Three instances of the same model
share training data, RLHF procedure, and architectural biases — they are not
independent judges. Three models from different organizations with different
training corpora and different reinforcement procedures are genuinely
independent. Their errors are uncorrelated, so consensus cancels them out.

### The Model Pool

The 7 models span four independent training lineages from different organizations
(4 organizations). The pool includes both cloud models
(accessed via CLI subscriptions at zero marginal cost) and local models (running
on-device for zero-cost consensus diversity). Each model brings different
training data, reinforcement procedures, and failure modes — ensuring genuine
independence in the voting process.

### How Concepts Are Validated

After all models respond for a given source chunk, the consensus algorithm runs
in three steps:

**Step 1 — Cross-model deduplication.** Two concepts from different models are
treated as the same concept if their titles have sufficient token-set overlap
(Jaccard ≥ 0.35), sequence similarity (ratio ≥ 0.65), or if tag overlap ≥ 70%
with similar summaries. The tag-overlap path catches semantic duplicates that
evade title matching — for example, "Onion Middleware Flow" and "Async Middleware
Composition" refer to the same Koa concept under different names.

**Step 2 — Vote counting.** Each deduplicated concept accumulates one vote per
model that proposed it. Concepts reaching the threshold (default: 2 votes) are
classified as *validated*. Those with a single vote are classified as
*candidates* and routed to the review queue rather than discarded.

**Step 3 — Concept merging.** When multiple models propose the same concept, the
merged result takes the richest title, the longest summary, frequency-ranked
tags (capped at 8), and an averaged confidence score weighted by model count.

### Provenance Weights

Every brain node carries a `provenance_weight` in its YAML frontmatter. This
weight is consumed by Shield's Epistemic Immune System when propagating trust
across the brain graph:

| Consensus Level | Provenance Weight | Trust Tier |
|----------------|-------------------|------------|
| 5/5 with cloud models | 0.95 | `library_verified` |
| 3/5+ with cloud models | 0.85 | `brain_verified` |
| 2/5 mixed cloud+local | 0.70 | `brain_keeper_audited` |
| 2/5 local only | 0.50 | `multi_llm_consensus` |
| 1/N single source | 0.40 | `worker_output` |

A node produced by unanimous cloud consensus carries 0.95 trust and can
propagate confidence to related nodes. A single-source node is accepted but
flagged for revalidation.

---

## Quality Progression

The pipeline was developed iteratively. Each version introduced a measurable
change to quality, tracked by auditor score on a 10-point scale.

| Version | Date | Key Change | Auditor Score |
|---------|------|-----------|---------------|
| v0.1 | 2026-03-10 | Single local model, no consensus | 6.5/10 |
| v0.2 | 2026-03-10 | 5-model consensus (3 cloud + 2 local) | 8.0/10 |
| v0.3 | 2026-03-10 | Semantic dedup + tag cap + defensive hardening | 8.5/10 (predicted) |
| v0.4 | 2026-03-13 | 7th model added; all 26 clusters rerun | active |

### v0.1 — Single Model Baseline (6.5/10)

The first run (`gamedev-patterns`, 9 files) used a single local model with no
consensus filter. The model accepted everything it produced. Results: thin
summaries of 1–2 sentences, excessive near-duplication across nodes, and noise
nodes representing boilerplate rather than meaningful concepts.

### v0.1 → v0.2 — The Consensus Jump (+1.5 points)

The second run (`10-koa`, 111 files) introduced 5-model consensus. The effect
was immediate and dramatic: 556 raw concepts were filtered down to 141 validated
(25.4% pass rate), then deduplicated to 53 brain nodes.

The 73% rejection rate is not waste — it is the signal. Concepts that only
one model proposed are either model-specific noise or ambiguous concepts that
different models named differently. Consensus forces agreement on what matters.
Summaries in v0.2 averaged 4–6 sentences with clear WHAT/WHY/HOW structure.

### v0.3 — Autonomous Self-Improvement

After Run 1, Shield identified three documented defects in the pipeline. Jarvis
autonomously analyzed the defects, implemented fixes, launched audit
workers across 3 audit rounds, and verified 11/11 inline tests — zero human
intervention.

The self-improvement cycle the pipeline now runs on:

```
Run → Measure Quality → Document Defects → Jarvis Reads Defects →
Jarvis Fixes Pipeline → Worker Audit → Next Run Scores Higher
```

This is meta-learning: the pipeline that ingests external knowledge is itself
subject to the same improvement cycle Shield applies to external projects.

### v0.4 — 7th Model Integration

A 5th cloud model was added, bringing the total to 7. With this addition, the
consensus pool spans 4 genuinely independent training lineages. All 26 clusters
were rerun under v0.4 to benefit from the expanded pool.

---

## Library Clusters — Complete Inventory

The following 26 clusters have been fully processed as of 2026-03-18. Source
file counts and node counts are from the final run per cluster.

| # | Cluster | Language | Source Files | Workers | Validated Concepts | Brain Nodes | Duration |
|---|---------|----------|--------------|---------|--------------------|-------------|---------|
| — | gamedev-patterns | C++ / Python | 9 | 4 | 19 | 30 | 11 min |
| 02 | typer | Python | 738 | 126 | 615 | 80 | 407 min |
| 03 | rich | Python | 553 | 292 | 671 | 64 | 826 min |
| 04 | black | Python | 452 | 111 | 384 | 82 | 290 min |
| 05 | flask | Python | 236 | 81 | 385 | 48 | 219 min |
| 06 | express | JavaScript | 213 | 48 | 218 | 47 | 141 min |
| 07 | zod | TypeScript | 56 | 8 | 21 | 37 | 31 min |
| 08 | hono | TypeScript | 484 | 155 | 667 | 62 | 452 min |
| 09 | svelte | JavaScript | 174 | 41 | 179 | 54 | 127 min |
| 10 | koa | JavaScript | 111 | 29 | 135 | 37 | 78 min |
| 11 | slim | PHP | 145 | 39 | 182 | 48 | 100 min |
| 12 | php-parser | PHP | 664 | 82 | 280 | 84 | 220 min |
| 13 | grav | PHP | 902 | 241 | 915 | 38 | 721 min |
| 14 | raylib | C | 1,364 | 332 | 1,220 | 107 | 979 min |
| 15 | imgui | C++ | 268 | 110 | 406 | 39 | 343 min |
| 16 | entt | C++ | 313 | 127 | 505 | 68 | 428 min |
| 17 | nlohmann-json | C++ | 1,178 | 240 | 892 | 105 | 661 min |
| 18 | spdlog | C++ | 177 | 61 | 242 | 39 | 176 min |
| 19 | ripgrep | Rust | 220 | 85 | 252 | 50 | 206 min |
| 20 | bat | Rust | 890 | 157 | 407 | 51 | 386 min |
| 21 | fd | Rust | 55 | 20 | 58 | 31 | 46 min |
| 22 | cobra | Go | 66 | 32 | 95 | 43 | 73 min |
| 23 | fiber | Go | 385 | 179 | 442 | 27 | 379 min |
| 24 | fzf | Go | 145 | 58 | 97 | 40 | 123 min |
| 25 | gson | Java | 306 | 141 | 333 | 61 | 372 min |

**Totals: 10,523 source files — 3,068 workers — ~10,166 validated concepts —
1,286 brain nodes across 9 languages.**

Languages covered: Python, JavaScript, TypeScript, PHP, C, C++, Rust, Go, Java, Kotlin.

Two new clusters added in V2:
- **26-ktor** (Kotlin) — web framework, first Kotlin cluster
- **ue-5.5** (C++) — Unreal Engine 5, 115K files, largest target attempted

The contrast between raw validated concepts and final brain nodes illustrates
the effect of the quality gate and cap enforcement. On average, approximately
8 validated concepts are consolidated or filtered into 1 brain node. The brain
contains the most distinctive and useful knowledge from each cluster, not the
most voluminous.

---

## Three-Layer Retrieval Architecture (No RAG)

The pipeline deliberately avoids vector embeddings. Retrieval is deterministic:
the same query always returns the same result.

```
Layer 1: Brain nodes  (~KB per cluster)
  Lightweight markdown: title, tags, summary, relations
  Lookup: inverted index — O(1), 0 tokens, < 1ms
          ↓
Layer 2: Markers  (~KB total)
  File:line_start-line_end pointers into source files
  Example: "koa/lib/application.js:47-89"
  Lookup: direct — O(1), 0 tokens
          ↓
Layer 3: Source material  (raw files, potentially GB)
  Only the exact lines indicated by markers are read
  Never loaded in full
  Read: seek + readline — 1–5ms
```

Query cost across all three layers: **0 tokens**. The brain finds the concept;
the marker finds the exact source location; the file read extracts 50–200 lines
of relevant code. Total latency for any query against millions of lines of source
material: under 5 milliseconds.

Compared to RAG-based retrieval: no chunking artifacts, no embedding drift, no
cosine similarity approximation, no vector store infrastructure. The tradeoff is
that this architecture requires upfront processing cost (the pipeline runs
described above). The benefit is that every retrieval is auditable — you can
read the exact source lines the marker points to and verify the brain node
describes them accurately.

---

## Revalidation: Recovery from Degraded Runs

When cloud models are temporarily unavailable during a run (quota exhaustion,
network failure), affected source chunks degrade to local-only consensus. The
resulting nodes have lower provenance weights and may have missed richer
semantic understanding from cloud models.

The revalidation tool selectively re-processes only degraded chunks:

1. Scan all nodes in a cluster and identify those with `provenance_weight < 0.75`
2. Reconstruct the original source chunks from node metadata
3. Discover which cloud models are available now
4. Re-extract only the degraded chunks using cloud models
5. Compare cloud output against existing nodes and apply one of three outcomes:

| Outcome | Condition | Effect |
|---------|-----------|--------|
| UPGRADED | Cloud confirms the concept | Raises consensus score, adds cloud provenance |
| DISPUTED | Cloud does not find the concept | Marks node `consensus: disputed`, lowers confidence to 0.2 |
| DISCOVERED | Cloud finds new concept not in original run | Creates new node |

For a run where 20 of 126 chunks lost cloud coverage, revalidation processes
only those 20 chunks — approximately 84% cost reduction versus a full rerun.

---

## Review Queue: Knowledge Recovery

Concepts that pass consensus but exceed the per-cluster node cap are not
discarded. They are written to `brain/library/.learner-review-queue.jsonl` with
a `discard_score` that enables priority-ordered re-evaluation.

The cap exists for a reason: uncapped clusters degrade inverted index performance
and reduce search precision because high-frequency generic terms saturate the
index. The cap forces consolidation — if 200 concepts pass consensus but only 50
survive, the 50 must be the most distinctive ones.

But distinctive is not the same as useless. The review queue provides a recovery
path: Jarvis can review cap-overflow candidates without re-running extraction.
Cheap workers generate the candidates; Jarvis reviews borderline cases. This
preserves knowledge that would otherwise be permanently lost, at near-zero
additional cost.

---

## Namespace Isolation

Library nodes are physically and logically isolated from project nodes:

```
brain/projects/shield/      → origin: project/shield
brain/library/10-koa/       → origin: library/10-koa
```

Brain search activates in two phases:

1. **Phase 1** — Search only `origin: project/*` (the current active project).
   If the results are sufficient, stop here. Experience outranks theory.

2. **Phase 2** — If Phase 1 is insufficient, expand to `origin: library/*`
   with domain tag filtering. A Rust project activates only Rust and C++
   clusters. A PHP project activates only PHP clusters. Cross-domain
   contamination is prevented by design.

This means that knowing the Koa framework (cluster 10) never pollutes a search
about a C++ game engine project. The brain knows what it knows and applies it
only where relevant.

---

## Library Nodes in the Brain Health System

Library nodes participate in Shield's broader brain maintenance systems with
rules adapted to their nature:

**Keeper (pruning):** Project nodes are pruned by inactivity — if a node is not
activated in N sessions, it is considered stale and a candidate for removal.
Library nodes are never pruned by inactivity. Their value is potential, not
historical usage. A node about `nlohmann::json` serialization may sit unused
for months until a C++ project requires it; at that point it becomes
immediately useful.

**Brain Graph:** Library nodes are full participants in the brain graph.
Cross-namespace edges (project to library) are created when the keeper identifies
semantic connections during audits. For example, a Shield project node about
a UI module might link to an imgui library node about the immediate-mode
rendering context.

**Epistemic Immune System:** Each node's `provenance_weight` participates in
trust propagation across the graph. A cloud-consensus node at 0.85 can anchor
trust for adjacent related nodes. A single-source node at 0.40 is quarantined
from trust propagation until revalidated.

---

## Design Decisions

**Why not RAG/embeddings?**
Embeddings produce probabilistic retrieval. The result of querying a vector store
is an approximation ranked by cosine similarity — the same query on the same
store can return different top-k results depending on floating-point conditions.
Brain search is deterministic and auditable. The tradeoff accepted is that
knowledge must be structured upfront; the benefit is that retrieval is reliable
and incurs zero runtime cost.

**Why not same-model multi-agent?**
Running three instances of the same model and taking the majority vote is
superficially similar to consensus but fundamentally different. Three instances
share training data, RLHF tuning, and architectural biases. Their errors are
correlated, so a majority vote does not improve accuracy — it only amplifies
the dominant bias. Models from different organizations have
genuinely independent biases. This is the Condorcet requirement: independence
is not optional.

**Why cap nodes per cluster?**
A 500-file library does not require 500 brain nodes. It requires the most
distinctive 50–100 concepts. A high cap produces index bloat and reduces
search precision because generic terms appear in too many nodes. The cap is
a quality mechanism, not a storage constraint.

**Why add a 5th cloud model?**
The selected model costs approximately 10x less than alternatives at comparable quality for
code understanding tasks. Adding it to the cloud pool increases the training
diversity of the consensus pool (a fourth independent lineage) while reducing
average per-run cost. In cross-model evaluation experiments, it showed
higher directive compliance (8.4/10) than the Claude API baseline (5.6/10),
making it a reliable consensus participant.
