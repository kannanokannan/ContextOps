# ContextOps vs. DORA AI Capabilities Model

Both ContextOps and the [DORA AI Capabilities Model](https://dora.dev/dora-aicmr) address AI in enterprise organizations. They operate at different layers and are designed to be used together.

---

## Comparison

| Dimension | DORA AI Capabilities Model | ContextOps |
|-----------|---------------------------|------------|
| **Scope** | Software delivery: the SDLC vertical. How AI affects engineering team performance, deployment frequency, and change failure rate. | Enterprise horizontal: how AI agents across the organization acquire, govern, and stay aligned with organizational context. Not limited to engineering teams. |
| **Unit of analysis** | Engineering team and delivery pipeline | AI agent and the organizational context it operates on |
| **Method** | Capability assessment mapped to research-backed performance outcomes. Identifies which AI capabilities correlate with elite software delivery. | Spine-based operating cycle (Capture → Curate → Supply → Renew) with named practices, roles, and a maturity gate. Identifies whether the organizational harness around an agent is production-ready. |
| **Governance posture** | Descriptive: measures the presence and maturity of capabilities that predict outcomes. | Prescriptive: defines named roles (Context Owner, Context Architect), gates (Transition Context Audit, AI Amplifier Assessment), and a continuous operating loop. |
| **Primary concern** | Does AI improve software delivery performance? Which capabilities drive that improvement? | Is the organizational context an agent operates on current, owned, and governable? What fails when it isn't? |
| **Tooling stance** | Framework-neutral; capabilities apply regardless of tooling choices. | Framework-neutral; overlays ITIL, TOGAF, COBIT, NIST AI RMF. No tooling mandated. |
| **Maturity model** | DORA's four-cluster model (Culture, Fast Flow, Fast Feedback, Fast Recovery) applied to AI capabilities. | Five-level model (Ad hoc → Optimizing) gated at Level 2. Below Level 2, foundational work precedes framework application. |
| **When to use** | When the question is: is our engineering team using AI effectively, and what should they change to improve delivery outcomes? | When the question is: do our AI agents have accurate, governed, current context — and what breaks when they don't? |

---

## How they fit together

DORA and ContextOps address adjacent problems. An engineering team can score well on DORA AI capabilities while still deploying agents that operate on stale, unowned, or conflicting organizational context — because DORA measures delivery practices, not context governance. Conversely, an organization can have a ContextOps-compliant context inventory and still underperform on software delivery because those are separate disciplines.

The natural integration point: teams using DORA to assess AI adoption in the SDLC can use ContextOps to govern the context those agents consume. The Transition Context Audit (ContextOps Practice 4) is particularly relevant at the Build-to-Run boundary that DORA's Fast Flow cluster also examines.

DORA's work is empirical — capabilities are grounded in research across thousands of organizations. ContextOps is practitioner-derived — it synthesizes patterns from enterprise platform adoption failures documented across decades. The two approaches are complementary in that sense as well.

---

## Reference

- DORA AI Capabilities Model: [https://dora.dev/dora-aicmr](https://dora.dev/dora-aicmr)
- ContextOps framework: [`FRAMEWORK.md`](../../FRAMEWORK.md)
- ContextOps named practices: [`FRAMEWORK.md` → Named Practices](../../FRAMEWORK.md#named-practices)

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
