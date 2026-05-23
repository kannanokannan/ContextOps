# RAG Pipeline — Mapping to ContextOps

> **Path in repo:** `/mappings/technical-layer/rag-pipeline.md`

---

## Source / Origin

Retrieval-Augmented Generation (RAG) is a hybrid pipeline pattern combining vector retrieval with generative LLM inference. Applied broadly across sovereign and air-gapped enterprise deployments where context cannot be encoded in model weights. No single origin; the pattern is documented across academic literature and production deployments from 2020 onward.

## Operating Level

- Application-level (managed by the orchestration layer around the agent)

The RAG pipeline governs how context reaches the model at inference time. It does not operate at the model-weight level and does not require agent-level memory management, though it may compose with both.

## Vendor Neutrality

Vendor-neutral. The pattern applies regardless of embedding model, vector database, or LLM provider. Specific implementation choices (chunking strategy, embedding model, retrieval algorithm, reranker) are out of scope for ContextOps.

## Key Mechanism

- **Ingestion:** Source documents are chunked, embedded, and stored in a vector index with associated metadata.
- **Retrieval:** At inference time, a query embedding is compared against the index; top-k chunks are returned.
- **Prompt assembly:** Retrieved chunks are inserted into the prompt context window alongside the user query.
- **Generation:** The LLM produces output grounded in the retrieved context rather than relying solely on parametric knowledge.
- **Guardrails / telemetry:** Output is filtered for hallucination signals; retrieval quality metrics feed drift monitoring.

## ContextOps Spine Mapping

| Pipeline component | ContextOps Spine stage |
|---|---|
| Data Ingestion / OCR / Chunking | Capture |
| Vector Database / Embedding / Metadata enrichment | Curate |
| Orchestration / RAG retrieval / Prompt assembly | Supply |
| Guardrails / Telemetry / Drift monitoring | Renew |

- **Capture:** yes — ingestion pipelines extract context from source documents (SoR, Knowledge Corpus, Telemetry tiers). ContextOps governs which sources are approved for ingestion and who owns them.
- **Curate:** yes — embedding and metadata enrichment determine retrieval quality. Context Owners define which chunks are authoritative; Context Conflict Resolution applies when multiple sources return contradictory chunks.
- **Supply:** yes — RAG retrieval and prompt assembly are the delivery mechanism for context to the agent. The AI Amplifier Assessment applies before production rollout.
- **Renew:** yes — vector indexes age as source documents update. Context Freshness Scoring governs re-ingestion triggers. Drift monitoring feeds the Non-Deterministic Triage Protocol.

## Organizational Gap

RAG pipelines handle the technical delivery of context. They do not handle:

- **Source authorization:** which documents are approved for ingestion is an organizational decision, not a pipeline decision. A RAG pipeline ingests what it is pointed at.
- **Ownership assignment:** vector indexes have no native concept of a Context Owner. When a retrieved chunk is wrong, the pipeline cannot identify who is accountable.
- **Conflict precedence:** when two ingestion sources return contradictory chunks on the same topic, the pipeline surfaces both. Precedence rules are an organizational governance decision.
- **Freshness policy:** pipelines do not know how stale is too stale for a given asset. Freshness budgets are set by Context Owners, not by retrieval infrastructure.
- **Compliance and audit:** which context an agent acted on at a given inference call is not captured by default. Audit trails require explicit instrumentation governed at the organizational layer.

## Connection Pattern

1. **Capture:** Identify the source tiers (SoR, Knowledge Corpus, Telemetry, Cognitive Memory) that will feed the ingestion pipeline. Apply the Downstream Task Tracing practice to confirm the agent's output consumers and their tolerance for stale or conflicting context.
2. **Curate:** For each ingestion source, assign a Context Owner responsible for quality and currency. Apply Context Conflict Resolution to define precedence when multiple sources cover the same topic. Run token optimization at chunking design time — chunk boundaries determine what the agent sees.
3. **Supply:** Before production deployment, run the AI Amplifier Assessment to confirm the consuming workflow is ready to be amplified by retrieval-grounded output. Complete the Transition Context Audit before any Build-to-Run handover of the pipeline.
4. **Renew:** Tag each source document class with a freshness budget via Context Freshness Scoring. Wire re-ingestion triggers to budget expiry, not just to source document changes. Route grounding failures (AI_ERR_01) through the Non-Deterministic Triage Protocol rather than closing them as "model errors."
5. **Ongoing:** Monitor retrieval quality metrics as a Context Drift signal. Embedding drift — where the same query returns different chunks over time as the index evolves — is a form of context drift that ContextOps Renew practices directly address.

## Note on Scope

ContextOps governs the organizational layer: what context is approved, owned, and versioned. The RAG pipeline is the delivery mechanism. ContextOps does not specify chunking strategy, embedding model, vector database choice, reranking algorithm, or retrieval hyperparameters. Those are implementation decisions that belong in the pipeline's own documentation.

## Status

Production-ready pattern. RAG pipelines are in enterprise production across regulated industries (finance, healthcare, legal, government) as of 2025. Air-gapped sovereign deployments using RAG are documented across defense and critical infrastructure sectors.

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
