# ContextOps

**Enterprise AI Context Framework**

> **Version:** 0.1 (Draft)
> **Read time:** ~10 minutes
> **License:** Apache 2.0

---

## What is ContextOps

ContextOps is a vendor-neutral, open-source methodology for enterprise AI context governance. It gives organizations a standardized way to capture, structure, govern, and supply organizational context to AI agents.

Context — the policies, runbooks, data dictionaries, role definitions, and escalation paths an agent needs to operate sensibly — is the primary bottleneck in enterprise AI adoption. The tools are capable. The plumbing (MCP, agent frameworks, APIs) is maturing. The methodology layer is missing.

ContextOps fills that gap. It sits on top of ITIL, TOGAF, COBIT, and NIST AI RMF. It does not replace them.

**North Star:** ITIL for AI context.

---

## Why Now

88% of enterprise AI agent pilots fail to reach production in 2026. Not because the models are wrong. Because the organizational harness around the agent — the context, governance, and operating model — is broken.

Enterprise AI spend is doubling. Budget share flowing to "AI context and data operations" has grown from 10% to 30% in 24 months. The market has moved from buying models to asking: how do we actually run these things?

Forrester predicts 60% of Fortune 100 companies will appoint a Head of AI Governance or equivalent by 2027. The role is emerging. The methodology it needs does not yet exist.

More than 40% of agentic AI projects are projected to be cancelled by 2027 — not for lack of investment (98% of organizations are increasing AI spend) but for lack of methodology.

ContextOps is the methodology.

---

## Core Vocabulary

Precise vocabulary is itself a deliverable. Buzzword drift — where "agent," "context," and "automation" mean different things to different stakeholders in the same room — kills shared understanding. Shared understanding is the only foundation an AI operating model can stand on.

**Context Asset** — any structured piece of organizational knowledge an AI agent needs: policies, runbooks, data dictionaries, role definitions, escalation paths.

**Context Inventory** — the catalog of all Context Assets across an organization.

**Context Owner** — the accountable person for a Context Asset. Domain-level responsibility.

**Context Architect** — the role that designs the enterprise's Context Inventory and the operating loop that governs it.

**Context Drift** — divergence between an AI agent's working context and current organizational reality. The primary failure mode in production AI systems.

**Continuous Context Operations (CCO)** — the practice of keeping AI agents continuously aligned with organizational reality. Replaces the traditional Build vs. AMS split for AI workloads, because done is no longer a meaningful state.

**AI-Anchored Vertical** — the correct unit of AI integration: the end-to-end workflow including what happens to the agent's output, not just what the agent does. Replaces the narrower and misleading "AI use case" framing.

**Pilot-to-Production Conversion Rate** — the percentage of AI pilots that reach persistent production deployment within 12 months. The primary health metric for an enterprise AI program.

---

## The Triad: People · Process · Context

The IT era ran on People · Process · Technology. The AI era requires an upgrade to the third leg.

**People** is not end-users alone. It is the entire corporate ecosystem from CEO to delivery engineer. Every stakeholder in the chain consumes context. Every link is an adoption gate. Context is only as good as the most-disconnected link in the chain.

**Process** is not workflow diagrams. It is vocabulary alignment. When every stakeholder describes the AI elephant differently — CEO sees strategy, CIO sees risk, engineer sees code, end-user sees chat — there is no shared understanding to build on. Shared understanding is the root of every working system and the death of every failed one.

**Context** is the fluid that flows between People and through Process. Policies, runbooks, data, roles, escalation paths. It drifts. It dies in handovers. It lives in heads. Governing it is the primary operational discipline of the AI era.

ContextOps owns the Context leg. It connects People and Process to make Context governable.

---

## The Spine: Capture → Curate → Supply → Renew

The ContextOps operating cycle runs in four stages. Each stage is a practice area with named roles, activities, and outputs. The loop is continuous. Done is not a meaningful state.

**Capture** — Extract context from the places where it currently lives: expert heads, legacy documentation, system configurations, process maps. Key activities include confirming the nature of the problem before designing for it (wicked vs. tame), mapping what happens to the agent's output downstream, and calibrating the mental models stakeholders hold before design begins.

**Curate** — Structure, assign ownership, approve, and version Context Assets. Raw knowledge becomes governable context here. Key activities include building the Context Inventory, assigning Context Owners per domain, and defining tolerance bands — standards define guardrails, not exact shapes, because 50% of any system reflects the builder's judgment even with standards in place.

**Supply** — Deliver context to agents via MCP and APIs, manage access permissions, and onboard new agents with complete context packages. The critical gate is the Transition Context Audit: before any Build-to-Run handover, the receiving operations team must verify inventory completeness, ownership transfer, renewal triggers, and escalation path preservation.

**Renew** — Monitor context drift, refresh aging assets, retire obsolete context, and trigger re-Capture when organizational reality changes. This stage is what separates ContextOps from a one-time documentation project.

---

## Roles

Five roles the framework defines, names, and enables. Each is a viable professional title — something a practitioner would put in their LinkedIn headline.

| Role | Level | Spine Stages | Primary Accountability |
|------|-------|-------------|----------------------|
| Context Architect | Enterprise | All | Designs the full operating loop |
| Context Owner | Domain | Curate | Accuracy and currency of domain assets |
| Context Curator | Practitioner | Capture, Curate | Hands-on extraction and structuring |
| AI Onboarding Manager | Project | Supply | Every new agent goes live with full context |
| Agent Operations Lead | Operations | Supply, Renew | Production health and drift monitoring |

---

## Maturity Model

Five levels. Used as a gate, not a ladder. Organizations below Level 2 should address foundational capability before applying ContextOps practices.

| Level | Name | Characteristic |
|-------|------|----------------|
| 1 | Ad hoc | AI used; context supplied per-prompt by individuals |
| 2 | Repeatable | Teams maintain shared prompt libraries; no governance |
| 3 | Defined | Context Owners exist per domain; Context Inventory documented |
| 4 | Managed | Continuous Context Operations in place; drift monitored |
| 5 | Optimizing | Framework metrics drive AI investment decisions |

**Gate rule:** ContextOps practices apply at Level 2 and above. Below Level 2, the intervention is foundational — shared vocabulary, problem definition, stakeholder alignment. Applying ContextOps to a Level 1 organization adds paperwork to confusion.

---

## Named Practices

> 🚧 Five practices documented below. Three to five additional practices will be added in v0.2.

**1. Problem Statement Test** *(Capture)*
Before any context design begins, classify the use case: tame problem (clear inputs, clear outputs, repeatable) or wicked problem (requirements change as you work, stakeholders disagree on success, no test for done). Almost every AI initiative is the second type, planned as if it were the first. Explicit classification changes the engagement model. Applying PMBOK-style planning to a wicked problem produces paperwork, not progress.

**2. Mental Model Calibration** *(Capture / early Curate)*
Document the actual mental model each stakeholder type holds about the agent being built. Gap-analyze against the capability being deployed. Define the enablement required to close each gap. If end-users believe the agent is a search box, designing for agentic composability will not land. The agent will be 10% useful to a user who could have made it 1000% useful with a different mental model.

**3. Downstream Task Tracing** *(Capture)*
Map not just what the agent does, but what happens to its output. Who acts on it. What decision it drives. What breaks if the output is wrong. Automating a report that still requires a person to read, interpret, and act on it has not removed the bottleneck — it has dressed it up. This trace determines whether the right unit of integration is an agent, a full AI-anchored vertical, or something in between.

**4. Transition Context Audit** *(Supply → Renew boundary)*
Before any Build-to-Run handover, the receiving operations team verifies: (a) context inventory is complete, (b) context ownership transfers are explicitly named, (c) renewal triggers are identified, (d) escalation paths to original builders are preserved. The AMS scramble — where operations teams land with limited transition knowledge and rebuild from scratch in their own way — is consistent enough across organizations to require a named gate. AI agents inherit this failure pattern without this practice.

**5. Workflow-First Migration** *(Cross-cutting)*
When ContextOps is deployed in a tool-replacement context, the unit of migration must be the workflow with its affordances — not the tool. Tool-for-tool replacement fails because users' workflows are built around the old tool's specific capabilities. Replacing a legacy collaboration platform with a modern suite by mapping features rather than workflows fails not because of the tools but because the workflow affordances were never mapped or preserved. The Two-Cost-Line Diagnostic is the detection mechanism.

> 🚧 **STUB — Practices 6–10:** Likely candidates include Context Freshness Scoring, Agent Blast Radius Assessment, Scale Parity Check, Context Conflict Resolution, and Non-Deterministic Triage Protocol.

---

## What ContextOps is NOT

- Not a SaaS product or tool
- Not tied to any AI vendor or model provider
- Not a replacement for ITIL, TOGAF, COBIT, or NIST AI RMF — it sits on top
- Not applicable below Maturity Level 2 — foundational work must come first
- Not a solution to wicked problems — it governs context, it does not define strategy
- Not consulting-as-a-product — though services firms will implement it

ContextOps does not own problem definition, human and political dynamics beyond the context chain, or vendor and tooling decisions. It owns context discipline and the AI operating model. Being explicit about what the framework does not own makes the claim on what it does own credible.

---

## Stakeholder Narratives

Each of the seven roles below sees a different version of the same problem. ContextOps gives them shared vocabulary to describe it.

**CEO** — Projects arrive on the executive's desk pre-framed by tool name before anyone has defined the business outcome. "An AI project." "A Copilot rollout." "An agentic workflow." Nobody asked what the business outcome was. Nobody can describe what success looks like. The strategic frustration is real: massive investment, unclear return, and a workforce that doesn't know how to use what's been deployed. ContextOps gives the CEO a vocabulary to demand outcome-framing before tool-buying.

**CIO** — Governance, audit, risk. The traditional frameworks — ITIL, COBIT — were designed for deterministic systems. AI agents are probabilistic. The CIO faces an "infrastructure of evidence" gap: no way to prove to the board that AI agents are operating on current, approved information. As Daryl Plummer (Gartner) put it at IT Symposium 2025: *"Treating AI like a wizard could set us back 10 years."* The methodology vacuum is what creates the wizard-thinking. ContextOps gives the CIO an audit-grade structure: named Context Owners, versioned Context Assets, documented renewal triggers, and explicit escalation paths.

**CDO / Chief AI Officer** — Speed to value is the mandate. The bottleneck is not the model — it is the context engineering cycle that restarts from scratch every time a new pilot is proposed. As Josh Bersin observed in late 2024: *"We don't have any idea what 'Agents' will do in partnership with humans."* That uncertainty compounds when every team rebuilds context from zero. ContextOps cuts setup time for each new agent by establishing inventory and ownership structures once, not per-project. The CDO becomes the steward of the Context Inventory across the enterprise.

**CFO** — Predictability and cost control. The Two-Cost-Line problem: organizations paying for both legacy and AI systems simultaneously because adoption stalled. Marcin Nowak (Forbes Technology Council, 2025) captured the scale: *"Companies pour massive investments into AI, to the tune of $30 to $40 billion. On the other hand, a staggering 95% of organizations are seeing no return on that spending."* ContextOps is the diagnostic and the intervention. Vendor-neutral design also prevents context lock-in — protecting the organization from paying for context engineering twice when models change.

**Enterprise Architect** — Fit without rip-and-replace. ContextOps overlays ITIL, TOGAF, and COBIT. The Context layer maps to existing data architecture concepts. The roles map to existing RACI structures. The spine maps to existing service lifecycle thinking. No new tooling mandated — ServiceNow, Confluence, Jira, GitHub, Power Platform all continue unchanged. The Enterprise Architect uses ContextOps to standardize how context flows through the existing estate, not to introduce a parallel one.

**AMS / Operations Lead** — Continuity when staff turn over and context lives in heads. The Transition Context Audit and the Renew stage practices are designed for AMS reality: high turnover, limited knowledge transfer, tool complexity compounded by process complexity. The "AMS scramble" — landing on an island with insufficient transition knowledge and rebuilding context from scratch in a new way — is consistent enough across organizations to require a named gate. ContextOps gives operations leads a structured handover protocol instead of a scramble.

**L&D Head** — Workforce readiness without external hiring. As Patricia Frost (Seagate CHRO) put it on the Josh Bersin Company Podcast in 2025: *"First, we had to take the anxiety down from our workforce. So my approach this year is leave no one behind."* The five named roles in ContextOps (Architect, Owner, Curator, Onboarding Manager, Operations Lead) are internal career paths, not new headcount requirements. L&D's job is the competency map for each role and the enablement curriculum. ContextOps provides the role definitions. L&D provides the pathway.

---

## Assessment Instruments

> 🚧 Full instruments are v0.2 scope. Minimal versions below serve as v0.1 starting points.

### Two-Cost-Line Diagnostic

Three questions for any enterprise running an AI program alongside a legacy system:

1. Is the organization still paying for the legacy system the AI was meant to replace?
2. If yes, has it been more than 12 months since AI deployment began?
3. If yes, the migration was tool-for-tool. Context discipline was not established. ContextOps is the intervention.

### Proposed Shared Metrics

| Metric | Definition | Signal |
|--------|------------|--------|
| Pilot-to-Production Conversion Rate | % of AI pilots reaching persistent production within 12 months | Industry average: ~12%. Target: >40%. |
| Context Freshness Score | Average age of Context Assets actively supplied to production agents | Rising age = drift risk |
| Two-Cost-Line Ratio | Legacy system spend ÷ AI system spend, post-migration | Should converge toward 0 over 24 months |

### Self-Assessment via AI Agent

Point any AI agent (Claude, ChatGPT, Gemini, Copilot, or similar) at [`agent-instructions/README.md`](agent-instructions/README.md). The agent will walk through a maturity assessment, run the Two-Cost-Line Diagnostic, and produce a scored snapshot with recommended starting points.

> 🚧 **STUB:** Ten-question pre-flight culture diagnostic. Pending field validation.

---

## Connections to the Technical Layer

ContextOps operates at the organizational layer. Technical frameworks — agent memory systems, context-management libraries, agent orchestration tools — operate at the agent or application layer. They are complementary disciplines.

Three operational seams connect any technical framework to ContextOps:

| Technical Operation | ContextOps Stage |
|---------------------|-----------------|
| Acquire / Ingest / Capture / Grow | Capture |
| Refine / Compress / Consolidate | Curate |
| Reflect / Update / Evolve | Renew |

See [`mappings/technical-layer/`](mappings/technical-layer/) for connector documentation. The technical layer is a community-extensible directory; ContextOps itself remains framework-neutral.

---

## Framework Disclosure

ContextOps is itself a project. Its implementation is subject to the same failures it describes.

Apply it selectively. Adapt it to your organizational context. Do not implement it in its entirety. Do not treat it as the cure for prior AI failures. A framework applied dogmatically to a wicked problem adds paperwork to confusion — this is true of ContextOps as much as it is of PMBOK, ITIL, or TOGAF.

Implement one stage, one practice, one role at a time. The maturity gate exists precisely because the framework should not be applied to organizations that are not ready for it.

*"Leave no future operator cursing your name."* That is the ethic this framework is built on. The framework holds itself to the same standard.

---

## Roots

The patterns named in this framework — wicked-problem dynamics, panacea effects, point-vs-platform mistakes, the gap between tool and workflow, vocabulary drift, the new-product factor — are not new. They were documented across enterprise platform adoption waves in the 1980s, 1990s, 2000s, and 2010s, by practitioners, academics, and analysts working in enterprise IT, organizational design, and complexity theory.

The contribution of ContextOps is the synthesis of those patterns into a methodology for AI agents specifically — and the insistence that the methodology layer is itself the missing piece of enterprise AI today.

ContextOps sits on top of:
- ITIL 4 (Service Management)
- TOGAF 10 (Enterprise Architecture)
- COBIT 2019 (IT Governance)
- NIST AI RMF 1.0 (Risk Management)

It does not replace any of them.

---

*ContextOps v0.1 — Draft. Stubs marked. Feedback welcome via GitHub Issues.*

*Licensed under Apache 2.0.*
