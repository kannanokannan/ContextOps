# Agent Authority

**A ContextOps governance module for agentic AI.**

Version: 0.1 (2026-07-06) · License: Apache 2.0

---

## Why this module exists

The core ContextOps framework governs *context* as an asset. When AI agents act — invoking tools, calling other agents, taking side-effectful steps — a second governance question appears that the base practices do not answer on their own: **who is accountable for what an agent is permitted to do, and how much autonomy it holds.**

This module does not introduce a new framework. It extends existing ContextOps responsibilities to the agent case and maps them to the external standards that emerged through 2026 (OECD, IMDA, OWASP, and the least-agency literature). ContextOps defines the responsibility. Enforcement is a ContextBoundary concern — see `ContextBoundary/agent-authority-enforcement.md`.

Positioning holds to the doctrine: **ContextOps defines governance, ContextBoundary enforces it.** Nothing here specifies runtime mechanism.

---

## Core vocabulary

**Agent Accountability** — Every agent has a single named accountable owner (a human role, not the agent itself). Extends the base *Accountability* and *Context Ownership* responsibilities. An agent with no accountable owner is an ungoverned agent and is out of policy by definition.

**Autonomy Tier** — A classification of how much an agent may do before a human decision is required. This is the base *Trust Classification* responsibility applied to action rather than to context. Tiers are graduated, from narrate-only through to bounded autonomous action within an approved envelope.

**Least Agency** — The default stance: an agent is granted the minimum Autonomy Tier and the minimum tool surface sufficient for its purpose. Any escalation is explicit, owned, and time-bound. Mirrors least-privilege, applied to agent action.

**Tool Supply Policy** — Which tool and MCP sources an agent is permitted to consume. Extends the base *Context Supply* and *Consumption Policy* responsibilities. Agent-connected tools are treated as a supply chain: each source has a trust classification, and untrusted sources are not consumable regardless of capability.

---

## The four responsibilities

| # | Responsibility | Extends (base ContextOps) | External anchor |
|---|----------------|---------------------------|-----------------|
| A1 | Every agent has a named accountable owner | Accountability / Context Ownership | IMDA agent identity; OWASP ASI |
| A2 | Every agent carries an Autonomy Tier | Trust Classification | OECD autonomy-level distinction; IMDA graduated autonomy |
| A3 | Least Agency is the default; escalation is explicit | (new default stance) | Least-agency literature; OWASP ASI |
| A4 | Agent tool/MCP sources are governed as a supply chain | Context Supply / Consumption Policy | Tool-as-supply-chain-risk literature |

These are governance responsibilities that must exist. As with the rest of ContextOps, the module does not prescribe who performs them or the mechanism — only that the responsibility is owned.

---

## Where this maps on the Spine

- **Capture** — record each agent, its owner, its purpose, its Autonomy Tier at creation.
- **Curate** — review Autonomy Tier and tool surface against purpose; strip unused capability (Least Agency).
- **Supply** — apply Tool Supply Policy; only trusted-source tools reach the agent.
- **Renew** — re-review autonomy on a defined cadence; escalations expire and must be re-owned.

---

## What this module is NOT

- Not a runtime control. Discovery gating, invocation gating, and identity-at-invocation live in ContextBoundary.
- Not an agent framework or orchestrator. Orchestration is the Hanumaan vision; this governs what any orchestrator is permitted to do.
- Not a new maturity model. It rides the existing five-level ContextOps maturity scale.
- Not vendor- or model-specific.

---

## Changelog

- **2026-07-06** — v0.1 created. Agent-authority governance responsibilities (A1–A4) defined and mapped to base ContextOps responsibilities, the Spine, and external standards (OECD / IMDA / OWASP / least-agency). Authored by Chanakya; registered by Hanuman in `DOCUMENT_MAP.md`, `framework.yaml`, and `llms.txt`.
