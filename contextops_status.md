# ContextOps — Project Status

**Version:** 0.1 (Draft)
**Last updated:** 2026-05-19
**Canonical source:** This file. Do not track status elsewhere.

---

## Overall status

In active development. Core framework is documented and published. Instruments and field validation are v0.2 scope.

---

## Canonical artifacts

| Artifact | Location | Status |
|----------|----------|--------|
| Framework document | `FRAMEWORK.md` | ✅ Complete (v0.1) |
| Machine-readable manifest | `framework.yaml` | ✅ Complete (v0.1) |
| Reader navigation guide | `DOCUMENT_MAP.md` | ✅ Complete (v0.1) |
| One-page overview | `README.md` | ✅ Complete (v0.1) |
| Agent self-assessment prompt | `agent-instructions/README.md` | ✅ Complete (v0.1) |
| Agent-readable index | `llms.txt` | ✅ Complete (v0.1) |
| Technical layer — ACE mapping | `mappings/technical-layer/ace.md` | ✅ Complete (v0.1) |
| Technical layer — LangMem mapping | `mappings/technical-layer/langmem.md` | ✅ Complete (v0.1) |
| Technical layer — MemGPT mapping | `mappings/technical-layer/memgpt.md` | ✅ Complete (v0.1) |
| Technical layer — RAG Pipeline mapping | `mappings/technical-layer/rag-pipeline.md` | ✅ Complete (v0.1) |
| Comparison — ContextOps vs. DORA | `docs/comparisons/contextops-vs-dora.md` | ✅ Complete (v0.1) |
| License | `LICENSE` | ✅ Apache 2.0 |

---

## Done

### FRAMEWORK.md edits (v0.1 pass)

- ✅ **1a** — Differentiation paragraph added (ContextOps vs. ITIL SKMS/CMDB). Location: end of "What is ContextOps" section, before "Why Now".
- ✅ **1b** — "Organizational harness" softened to "organizational context, governance, and operating model". Word "harness" removed from FRAMEWORK.md entirely.
- ✅ **1c** — Forrester attribution added to 88% pilot failure stat. Full citation: Forrester and Anaconda 2026, corroborated by IDC and MIT Sloan CIO panel. Root-cause breakdown included.
- ✅ **1d** — Abstract Enterprise Taxonomy table added after Core Vocabulary section. Four tiers: SoR, Knowledge Corpus, Telemetry, Cognitive Memory.
- ✅ **1e** — Token optimization sentence added to Curate stage description in the Spine section.
- ✅ **1f** — Convergence citation added to end of Practice 10 (Non-Deterministic Triage Protocol). References sovereign air-gapped architecture (2026) three-tier escalation model and AI_ERR_01 error code.

### framework.yaml updates (v0.1 pass)

- ✅ **2a** — `sits_alongside` key added under `mappings:`. Entries: DORA AI Capabilities Model (SDLC vertical) and DAMA-DMBOK (Data Management).
- ✅ **2b** — `ai-amplifier-assessment` confirmed as the consistent identifier throughout. No `agent-blast-radius` references present.

### New technical-layer mapping

- ✅ **3** — `mappings/technical-layer/rag-pipeline.md` created. Covers: what RAG is, Spine mapping table (four pipeline components to four stages), four applicable ContextOps practices, organizational gap analysis, five-step connection pattern, scope note.

### README.md

- ✅ **4** — Quick Start step 3 updated to reference RAG pipelines, agent memory frameworks, and orchestration tools without naming specific products. Duplicate "Not sure where to start?" line removed.

### Discoverability pass (separate PR, merged)

- ✅ `llms.txt` created at repo root (llmstxt.org spec)
- ✅ README.md opener rewritten with natural search-relevant phrases
- ✅ Connectors section added to README.md (ACE, LangMem, MemGPT)
- ✅ Compare section added to README.md
- ✅ `docs/comparisons/contextops-vs-dora.md` created
- ✅ GitHub repo topics set: ai-governance, enterprise-ai, context-engineering, ai-operations, mcp, llmops, ai-framework

---

## In flight

Nothing currently in flight.

---

## v0.2 scope (not started)

- Full maturity self-assessment instrument (ten-question scored)
- Pre-flight culture diagnostic (ten questions, field validation pending)
- Organizational case sketches (sanitized real-world examples)
- Additional technical-layer mappings (community contributions)
- Assessment instrument tooling

---

## Sibling project

**ContextBoundary** — sovereignty and compute placement layer. Tracked separately in `contextboundary_status.md`. Do not conflate with ContextOps.

---

*ContextOps v0.1 — Apache 2.0*
