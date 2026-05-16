# [Framework Name] — Mapping to ContextOps

> **Path in repo:** `/mappings/technical-layer/[framework-name].md`
>
> Copy this template, fill in each section, and submit as a pull request.

---

## Source / Origin

Who built it. Paper, repository, or product link. One or two lines.

## Operating Level

Choose one. Delete the others.

- Model-level (built into the model weights or training process)
- Agent-level (managed by the agent during reasoning)
- Application-level (managed by the orchestration layer around the agent)
- Organizational-level (governance, ownership, policy — this is where ContextOps operates)

## Vendor Neutrality

State whether the framework is vendor-neutral (works with multiple model providers) or vendor-specific. One line.

## Key Mechanism

3–5 bullet points on the core technical approach. Be specific. Avoid marketing language.

## ContextOps Spine Mapping

For each stage, indicate whether the framework addresses it and how.

- **Capture:** [yes / partial / no] — [how, if yes]
- **Curate:** [yes / partial / no] — [how, if yes]
- **Supply:** [yes / partial / no] — [how, if yes]
- **Renew:** [yes / partial / no] — [how, if yes]

## Organizational Gap

What this framework does NOT handle that requires human organizational decisions. 3–5 bullets. Be specific — name the actual gaps, not generic statements.

Examples of gaps to look for:
- Ground truth definition (who decides what is correct)
- Multi-tenant permissions (who is authorized to do what)
- Organizational context import (policies, runbooks, role definitions)
- Cross-agent reconciliation (when multiple agents diverge)
- Compliance and audit (regulatory requirements)
- Lifecycle management (when does context retire)

## Connection Pattern

A 3–5 step description of how a ContextOps-aligned organization would integrate this framework. Each step should reference a specific ContextOps practice or stage.

## Status

Production-ready / Early adopter / Research only.

One line of evidence.

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
