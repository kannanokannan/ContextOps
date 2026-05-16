# LangMem — Mapping to ContextOps

> **Path in repo:** `/mappings/technical-layer/langmem.md`

---

## Source / Origin

LangChain Team. Documentation: https://langchain-ai.github.io/langmem/

## Operating Level

Application-level

## Vendor Neutrality

Vendor-neutral. Part of the LangChain / LangGraph ecosystem but supports multiple model providers and storage backends.

## Key Mechanism

- **Background Memory Manager** extracts, consolidates, and updates knowledge outside the active conversation flow to minimize latency.
- **Namespaces architecture** isolates memories by user, session, or organization ID, enabling multi-tenant data management.
- **Trustcall** provides type-safe memory updates, ensuring information is updated or invalidated correctly based on new evidence.
- Offers **tool-based memory management** that allows agents to explicitly decide when to search or store information.
- **ReflectionExecutor** debounces memory tasks, ensuring only settled, high-signal information enters the long-term store.

## ContextOps Spine Mapping

- **Capture:** Yes — primary. LangMem excels at capturing raw interactions and extracting facts from them.
- **Curate:** Partial. The Background Manager performs technical consolidation, but governance decisions about what should be curated are left to the LLM.
- **Supply:** Yes. Stored memories are supplied back to the agent in future sessions through semantic retrieval.
- **Renew:** Partial. Memory invalidation happens based on new evidence in conversation, not on organizational policy changes.

## Organizational Gap

What LangMem does not handle:

- **Data retention and "Right to Erasure" policies.** LangMem provides the storage mechanism but not the legal or compliance logic for when data must be deleted.
- **Human-in-the-loop curation.** The consolidation logic is owned by the Manager LLM. No native interface for human stewards to audit or approve what is being remembered.
- **Bridge between user facts and organizational policy.** LangMem remembers what users said about themselves. It does not bridge this with corporate policy, regulatory requirements, or organizational truth.
- **PII detection at capture time.** If an agent learns a piece of PII or a proprietary secret during conversation, LangMem will store it. There is no organizational context layer to recognize and redact before storage.
- **Cross-namespace organizational alignment.** Namespaces isolate data; they do not propagate enterprise-wide policy changes.

## Connection Pattern

A ContextOps-aligned organization integrating LangMem would:

1. Use ContextOps Capture practices to define what categories of information are appropriate for the agent to remember at all — before deploying LangMem.
2. Add a Curate gate above LangMem's Background Manager: a Context Owner reviews categories of extracted facts on a defined cadence, not individual extractions.
3. Use namespaces to enforce organizational boundaries — but supplement with explicit Context Inventory documentation about what each namespace should and should not contain.
4. Implement Renew stage practices to push organizational policy changes into the relevant namespaces, since LangMem will not surface stale memories on its own.
5. Apply Transition Context Audit when transferring a LangMem-backed agent from project team to operations.

## Status

Production-ready. Core part of the LangChain / LangGraph ecosystem with persistent backends including Postgres and specialized vector stores.

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
