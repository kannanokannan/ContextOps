# MemGPT (Letta) — Mapping to ContextOps

> **Path in repo:** `/mappings/technical-layer/memgpt.md`

---

## Source / Origin

UC Berkeley (research paper: *"MemGPT: Towards LLMs as Operating Systems"*). Now maintained by Letta.

- Paper: https://arxiv.org/abs/2310.08560
- Documentation: https://docs.letta.com/

## Operating Level

Agent-level

## Vendor Neutrality

Vendor-neutral. Supports multiple model backends.

## Key Mechanism

- Distinguishes between **Main Context** (immediate prompt tokens) and **External Context** (archival and episodic storage tiers).
- Equips the agent with **Self-Editing Memory tools** — the model explicitly writes facts to archival memory or retrieves data via search functions.
- Uses an **event-based control flow** where the system can signal "memory pressure" to the LLM, prompting it to summarize or offload data.
- Integrates a git-backed **MemFS** (Memory Filesystem) that provides full versioning and history for every change the agent makes to its memory.
- Treats the context window as a managed resource, shifting memory management from developer to agent.

## ContextOps Spine Mapping

- **Capture:** Yes. The agent captures unbounded history through interaction.
- **Curate:** Partial. The agent's self-editing performs consolidation, but no human curation layer exists by default.
- **Supply:** Yes. The paging mechanism supplies relevant context from external tiers into the active prompt.
- **Renew:** Yes. The Self-Editing capability is renewal at the agent level — but driven by the agent's own judgment.

## Organizational Gap

What MemGPT does not handle:

- **Compliance firewall.** No organizational governance layer to stop an agent from archiving sensitive data, PII, or regulated records.
- **Organizational context synchronization.** No mechanism to push updated corporate policies into the agent's External Context automatically. The agent renews based on conversation, not on organizational change.
- **Cross-agent memory reconciliation.** Multiple MemGPT agents may have conflicting archival memories of the same business process with no built-in resolution.
- **Deterministic audit.** The agent decides what to page in and out. Organizations lose the ability to know definitively what the agent "knew" at a specific point in time without inspecting MemFS history manually.
- **Permission scoping at the memory level.** Self-Editing assumes the agent has authority to write whatever it deems relevant. No tier-based authorization model.

## Connection Pattern

A ContextOps-aligned organization integrating MemGPT (or Letta) would:

1. Use ContextOps Capture practices to define what the agent should be allowed to remember and at what tier before deployment.
2. Use the MemFS versioning capability as the technical substrate for organizational auditability — but supplement with a Context Owner who has approval authority over what can be archived.
3. Treat MemGPT's paging as a Supply mechanism only — not as a substitute for organizational Curation.
4. Implement explicit Renew stage practices to push policy changes into External Context tiers on a defined cadence, since MemGPT will not pull them in autonomously.
5. Apply Transition Context Audit when an MemGPT-based agent moves from build to production, with specific attention to what is currently in archival memory.

## Status

Early adopter pattern for stateful agent deployments. Evaluate fit against memory governance, auditability, data retention, and Context Owner approval requirements before enterprise use.

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
