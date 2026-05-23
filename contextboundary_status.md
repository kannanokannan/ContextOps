# ContextBoundary — Project Status

**Last updated:** 2026-05-23
**Status:** Concept defined. No repo yet. Tracked as ContextOps sibling project.

---

## One-line status

Sibling open-source project to ContextOps. Defines the technical sovereignty layer — compute placement, data classification, and privacy boundary contracts between on-prem infrastructure and frontier AI providers.

---

## What ContextBoundary is

ContextBoundary is the canonical technical-layer connector to ContextOps. Where ContextOps governs *what* context is captured, curated, and supplied, ContextBoundary governs *where* it flows and *under what sovereignty constraints*.

It is not a tool. It is a framework for compute placement decisions and data boundary contracts.

---

## Core definitions (locked)

- **Data Classification Tiers:** Red / Amber / Green
- **Compute Placement Matrix:** on-prem legacy vs. cloud GPU/NPU
- **Orchestration Gateway:** policy-driven routing, redaction, and audit
- **Privacy Boundary Contracts:** between on-prem compute and frontier AI providers (Claude, GPT-4, Gemini, Copilot)

---

## Relationship to ContextOps

- Slots into `mappings/technical-layer/` extension point in the ContextOps repo
- ContextOps governs the organizational layer (context lifecycle, roles, practices)
- ContextBoundary governs the sovereignty layer (where context travels, under what conditions)
- Neither replaces the other

Pending ContextOps task: Update `FRAMEWORK.md` to name ContextBoundary as canonical connector in the Connections to Technical Layer section + add 4th seam + sovereignty vocabulary.

---

## External validation inputs

| Source | Relevance |
|--------|-----------|
| Enterprise AI Architecture doc (Gemini chat, May 2026) | "True Digital Sovereignty = control data + infrastructure + code" — strongest external articulation of the CB problem statement. Use in rationale write-up. |
| Enterprise AI Architecture doc — Clean Room approach | Freeze weights, supply only curated RAG context = on-prem compute pattern CB defines. Cite as implementation pattern. |

---

## To-do

### In flight

- [ ] Write CB rationale using "True Digital Sovereignty" framing from Enterprise AI Architecture doc
- [ ] Define Red/Amber/Green classification criteria (what triggers each tier)
- [ ] Draft compute placement matrix (decision logic, not just labels)
- [ ] Draft privacy boundary contract template (what must be declared before context crosses the boundary)

### Parked (post ContextOps v0.1)

- [ ] Create standalone CB repo
- [ ] Write `mappings/technical-layer/contextboundary.md` in ContextOps repo
- [ ] Update ContextOps `FRAMEWORK.md` with sovereignty vocabulary + CB as 4th seam
- [ ] Add NOT-list bullet in ContextOps on compute boundaries (owned by CB, not ContextOps)
- [ ] Version CB as 0.1 aligned with ContextOps 0.2

---

## Anti-decisions

- Not a SaaS product
- Not vendor-specific
- Not a replacement for ContextOps — sits below it at the technical layer
- Not a security product — sovereignty classification, not threat detection

---

## Open questions

- Does CB get its own repo or lives inside ContextOps repo under `/sovereignty/`? Decision: own repo.
- Apache 2.0 (align with ContextOps) — assumed yes, not confirmed
- First classification criterion to define: Red tier boundary (most important, most contested)

---

*ContextBoundary — concept phase. Sibling to ContextOps v0.1. Apache 2.0 assumed.*
