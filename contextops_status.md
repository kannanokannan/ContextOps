# ContextOps — Project Status

**Version:** 0.1 (Draft)
**Last updated:** 2026-05-23
**Canonical source:** This file. Do not track status elsewhere.

---

## Overall status

In active development. Core framework documented and published. Distribution packs shipped across 10 LLM environments. Field validation is v0.2 scope.

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
| ContextBoundary project status | `contextboundary_status.md` | ✅ Active (concept phase) |
| Distribution Packs | `distributions/` | ✅ Complete (v0.1) — 10 LLM environments |
| License | `LICENSE` | ✅ Apache 2.0 |

---

## Done

### FRAMEWORK.md edits

- ✅ Differentiation paragraph added (ContextOps vs. ITIL SKMS/CMDB)
- ✅ "Organizational harness" softened — word "harness" removed entirely
- ✅ Forrester attribution added to 88% pilot failure stat
- ✅ Abstract Enterprise Taxonomy table added (SoR / Knowledge Corpus / Telemetry / Cognitive Memory)
- ✅ Token optimization sentence added to Curate stage
- ✅ Convergence citation added to Practice 10 (Non-Deterministic Triage Protocol)
- ✅ Practice 9 tightened — Kautilya Rule of Three applied to canonicalization
- ✅ Roots section — Rittel & Webber (1973) cited for wicked-problem framing

### framework.yaml

- ✅ `sits_alongside` added: DORA AI Capabilities Model + DAMA-DMBOK
- ✅ `ai-amplifier-assessment` confirmed as consistent identifier

### New files

- ✅ `mappings/technical-layer/rag-pipeline.md` — RAG Pipeline connector
- ✅ `docs/comparisons/contextops-vs-dora.md` — DORA comparison
- ✅ `contextboundary_status.md` — ContextBoundary sibling project tracking
- ✅ `distributions/` — 10 LLM-specific install packs (Claude Code, Cursor, Windsurf, Cline, Aider, Copilot GitHub, Copilot M365, ChatGPT, Gemini, Generic)

### Structural fixes

- ✅ `agent-instructions/README.md` — moved from flat file to correct subdirectory
- ✅ `README.md` — repo tree updated, rag-pipeline added to connectors
- ✅ `DOCUMENT_MAP.md` — repo tree updated, rag-pipeline added to mappings list
- ✅ `llms.txt` — LLM-addressed note added
- ✅ `.gitignore` — `.claude/` added to prevent Claude Code worktree files from being committed

### Discoverability

- ✅ `llms.txt` created at repo root (llmstxt.org spec)
- ✅ README.md opener rewritten with search-relevant phrases
- ✅ GitHub repo topics set: ai-governance, enterprise-ai, context-engineering, ai-operations, mcp, llmops, ai-framework

---

## In flight

Nothing currently in flight.

---

## v0.2 scope (not started)

- Full maturity self-assessment instrument (ten-question scored)
- Pre-flight culture diagnostic (field validation pending)
- Disconfirming criteria per maturity level
- Organizational case sketches (sanitized)
- ContextBoundary rationale write-up + Red/Amber/Green classification criteria
- Second Gemini Deep Research (2027–2029 predictions angle)
- Namespace claim — GitHub org, domains (.org/.dev/.io), npm/pypi placeholders
- Services-firm narrative: net-new billable work ContextOps creates

---

## Traffic signals (as of 2026-05-23)

- 64 clones / 45 unique cloners in 14 days — zero promotion
- Clone-heavy / view-light pattern = LLM-mediated discovery confirmed
- `chatgpt.com` appearing as referrer — GPT web tool indexing via Bing
- `llms.txt` accessed directly — AI-native distribution working
- Primary metrics going forward: unique clones + llms.txt views (not page views)

---

## Sibling project

**ContextBoundary** — sovereignty and compute placement layer. Tracked in `contextboundary_status.md`.

---

*ContextOps v0.1 — Apache 2.0*
