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

*55 knowledge clusters processed as of 2026-03-30, spanning 13 programming languages.
5,588 library nodes via multi-model consensus. Additionally, 563,144 code nodes
from 93 projects via the Learn v2 code parser — functions, classes, modules, constants
extracted and classified into 50 semantic categories.*

### Learn v2 Scale (Days 17-24)

The original consensus pipeline produced high-quality, curated library nodes (5,588).
Learn v2 added a complementary pathway: direct code parsing that extracts structural
elements from projects and classifies them into the semantic ontology.

| Pathway | Nodes | Method | Quality |
|---------|-------|--------|---------|
| Library consensus (v1) | 5,588 | Multi-model validation | High (curated) |
| Code parser (v2) | 563,144 | Structural extraction + semantic classification | Comprehensive (raw) |
| **Total** | **571,907** | Both coexist in brain | Layered |

The two pathways serve different purposes: consensus nodes answer "what does this library do?",
code nodes answer "what specific functions exist and how are they related?"

---

## What the Pipeline Does

The pipeline takes a folder of source code or documentation and produces a
collection of **brain nodes** — structured knowledge entries with metadata
that are indexed alongside project knowledge.

Each brain node represents one validated concept: an API pattern, an
architectural decision, a behavioral characteristic of the library. The node
contains a summary, tags, relations to other concepts, and full provenance
metadata showing which models agreed on it and at what confidence level.

---

## Multi-Model Consensus: Why It Prevents Hallucination

The core mechanism that separates this pipeline from single-model extraction is
**cross-model consensus across models from independent training lineages**.

![Consensus](../assets/learner-7-model-consensus.png)

*The multi-model consensus pool. Each concept must be independently proposed by
multiple models to survive. Independent training lineages ensure uncorrelated
biases that cancel each other.*

### The Condorcet Argument

The theoretical foundation is Condorcet's Jury Theorem (1785): if each
independent judge has a probability greater than 50% of being correct, the
probability that the majority is correct approaches 100% as independent judges
are added.

Applied to LLMs: models from different organizations with different
training corpora and different reinforcement procedures are genuinely
independent. Their errors are uncorrelated, so consensus cancels them out.

**The critical constraint is independence.** Multiple instances of the same model
share training data, RLHF procedure, and architectural biases — they are not
independent judges. Models from different organizations are.

### Provenance-Based Trust

Every brain node carries a provenance weight based on the consensus level
that produced it. Nodes validated by multiple cloud models from different
training lineages carry the highest trust. Single-source nodes are accepted
but flagged for revalidation. This provenance weight propagates through the
knowledge graph, allowing the system to reason about information reliability.

---

## Quality Progression

The pipeline was developed iteratively. Each version introduced measurable
improvements to knowledge quality.

| Version | Key Change | Effect |
|---------|-----------|--------|
| v0.1 | Single local model | Baseline: thin summaries, duplication |
| v0.2 | Multi-model consensus | +1.5 quality points: 75% noise rejected |
| v0.3 | Autonomous self-improvement | Pipeline fixes its own defects |
| v0.4 | Expanded model pool | Fourth independent training lineage added |

### Autonomous Self-Improvement

After each run, Shield identifies defects in the pipeline output, implements
fixes, launches independent audit workers, and verifies improvements — without
human intervention. The pipeline that ingests external knowledge is itself
subject to the same improvement cycle Shield applies to external projects.

---

## Library Clusters

55 clusters have been fully processed as of 2026-03-30 across 13 programming
languages: Python, JavaScript, TypeScript, PHP, C, C++, Rust, Go, Java, Kotlin,
CUDA, ISPC, and Svelte.

The pipeline processes source files through the consensus mechanism and
quality filters, producing a curated set of brain nodes per cluster. On average,
approximately 8 raw validated concepts are consolidated into 1 final brain node.
The brain contains the most distinctive and useful knowledge from each cluster.

---

## Retrieval Architecture

The pipeline avoids vector embeddings entirely. Retrieval is **deterministic**:
the same query always returns the same result, with zero runtime token cost.

The architecture uses a multi-layer lookup system that resolves queries from
high-level concept summaries down to exact source file locations. Total latency
for any query against millions of lines of source material: under 5 milliseconds,
at zero API token cost.

Compared to RAG-based retrieval: no chunking artifacts, no embedding drift, no
cosine similarity approximation, no vector store infrastructure. The tradeoff is
upfront processing cost during ingestion. The benefit is that every retrieval
is auditable and deterministic.

---

## Namespace Isolation

Library nodes are isolated from project nodes. Brain search activates in phases:
project knowledge is searched first (experience outranks theory), and library
knowledge is activated only when project knowledge is insufficient — with
domain-specific filtering to prevent cross-domain contamination.

---

## Design Principles

- **Independence over quantity**: Consensus from 3 independent models beats 10 instances of the same model
- **Determinism over approximation**: Keyword index over vector similarity
- **Quality over volume**: Caps force consolidation — the most distinctive concepts survive
- **Experience over theory**: Project nodes always outrank library nodes in retrieval priority
- **Self-improvement**: The pipeline applies to itself the same quality cycle it applies to projects
