# CLAUDE.md — ContextOps Agent Briefing

This file briefs any Claude agent working on the ContextOps project.
Read this before touching any file in this repo.

---

## Canonical Reference

Before introducing any new term: check https://github.com/kannanokannan/context-stack/blob/main/GLOSSARY.md

Before making any cross-project decision: check https://github.com/kannanokannan/context-stack/blob/main/DECISIONS.md

Terminology defined in GLOSSARY.md overrides any local usage in this repo.

---

## What This Project Is

**ContextOps** is a vendor-neutral, open-source enterprise AI context governance framework.
Tagline: ITIL for AI context. License: Apache 2.0.
Repo: https://github.com/kannanokannan/ContextOps

---

## The One-Line Answer

> ContextOps answers: **how does an organisation govern its AI context?**

---

## The Framework Family

ContextOps is one of three sibling governance projects in the context-stack. Griha is the product layer above them. Do not conflate these scopes.

| Project | Layer | Answers | Repo |
|---------|-------|---------|------|
| **ContextOps** | Organizational context governance | How does an org govern its AI context? | https://github.com/kannanokannan/ContextOps |
| **ContextBoundary** | Egress governance | Where is data allowed to go? | https://github.com/kannanokannan/ContextBoundary |
| **Sthala** | Governed runtime reference | Where does the AI actually run? | https://github.com/kannanokannan/Sthala |
| **Griha** | Product layer | How do the stack principles appear in a working system? | https://github.com/kannanokannan/Griha |

**Key relationship rules:**
- ContextOps governs the organisational layer
- ContextBoundary governs the egress layer (horizontal, deployment-agnostic)
- Sthala is one compliant vertical implementation under ContextBoundary
- Griha is the product layer above the three governance projects
- Do not conflate these scopes

---

## Core Constants (Locked)

- **Triad:** People · Process · Context
- **Spine:** Capture → Curate → Supply → Renew
- **5 Roles:** Context Architect, Context Owner, Context Curator, AI Onboarding Manager, Agent Operations Lead
- **Maturity model:** 5 levels. Apply at Level 2+. Never below.
- **Sits on top of:** ITIL 4, TOGAF 10, COBIT 2019, NIST AI RMF 1.0 — does not replace any

---

## What ContextOps Is NOT

- Not a SaaS product
- Not vendor-specific
- Not a replacement for ITIL, TOGAF, COBIT, or NIST AI RMF
- Not applicable below Maturity Level 2
- No new tools required — overlays ServiceNow, Confluence, Jira, GitHub, Power Platform
- Services firms are distribution channels, not competitors

---

## Key Files

- `FRAMEWORK.md` — core framework specification (source of truth)
- `README.md` — project overview
- `DOCUMENT_MAP.md` — navigation across all artifacts
- `framework.yaml` — machine-readable manifest
- `agent-instructions/README.md` — AI self-assessment agent
- `mappings/technical-layer/README.md` — ACE, LangMem, MemGPT mappings

---

## Commit Style

Single-topic commits. Descriptive message with bullet breakdown.

---

*ContextOps v0.1 · Apache 2.0*
