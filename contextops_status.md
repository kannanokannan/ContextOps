# ContextOps — Project Status

**Version:** 0.1 (Draft)
**Last updated:** 2026-06-11
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
- ✅ Production-readiness wording softened — organizational context, governance, and operating model named explicitly
- ✅ Time-bound pilot-failure statistics removed; Why Now reframed around durable production-readiness failure modes
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

### Framework critique follow-ups

- ✅ Stack positioning aligned with context-stack: ContextOps as organizational context governance, ContextBoundary as egress governance, Sthala as runtime reference implementation, and Griha as product layer.
- ✅ Curate stage strengthened with explicit governed Context Asset outputs: canonical source, owner, validity rule, conflict rule, access boundary, shape constraint, and downstream consumers.
- ✅ Continuous Context Operations (CCO) threaded through the Spine, AMS / Run overlay, and machine-readable manifest.
- ✅ Level 1 foundation readiness path added to `FRAMEWORK.md`, `framework.yaml`, and `agent-instructions/README.md`.
- ✅ Abstract Enterprise Taxonomy connected to Capture and Curate work.
- ✅ Workflow-First Migration tightened with explicit Context Asset governance requirement.
- ✅ Delivery Model Overlays placement reviewed and kept before Roles so readers see attachment points before role accountability.
- ✅ Read-time claim updated from ~10 minutes to ~12 minutes; no document split required for v0.1.
- ✅ Pilot-to-production framing now avoids current-market percentages and focuses on durable governance failure modes.
- ✅ Moving analyst percentages, dated forecasts, and benchmark status claims neutralized across public-facing docs.
---

## In flight

Nothing currently in flight.

---

## Remaining framework critique action items (2026-06-11)

None currently open from the 2026-06-10 framework critique pass.

---

## v0.2 scope (not started)

- Full maturity self-assessment instrument (ten-question scored)
- Pre-flight culture diagnostic (field validation pending)
- Disconfirming criteria per maturity level
- Organizational case sketches (sanitized)
- ContextBoundary rationale write-up + Red/Amber/Green classification criteria
- Second external research pass for forward-looking enterprise AI adoption risks
- Namespace claim — GitHub org, domains (.org/.dev/.io), npm/pypi placeholders
- Services-firm narrative: net-new billable work ContextOps creates

---

## Historical traffic snapshot

Snapshot retained as historical project telemetry, not as a standing market claim.

- Early clone-heavy / view-light pattern suggested LLM-mediated discovery
- `llms.txt` was accessed directly, validating AI-readable distribution as a useful channel
- Primary metrics going forward: unique clones + `llms.txt` views, not page views

---

## Sibling project

**ContextBoundary** — sovereignty and compute placement layer. Tracked in `contextboundary_status.md`.

---

*ContextOps v0.1 — Apache 2.0*
