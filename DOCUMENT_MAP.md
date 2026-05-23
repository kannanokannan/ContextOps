# Document Map

Where to start, based on what you came here to do.

---

## If you have 10 minutes

Read **[`FRAMEWORK.md`](FRAMEWORK.md)** end to end. That is the whole framework. Everything else in this repo supports it.

---

## If you are evaluating ContextOps for your organization

Read in this order:

1. **[`README.md`](README.md)** — what this is, in one page
2. **[`FRAMEWORK.md`](FRAMEWORK.md)** — the framework, ~10 minutes
3. **[`FRAMEWORK.md` → What ContextOps is NOT](FRAMEWORK.md#what-contextops-is-not)** — confirm the scope claim
4. **[`FRAMEWORK.md` → Roots](FRAMEWORK.md#roots)** — confirm the precedents you sit on top of

Then run the self-assessment (see below).

---

## If you want to run the self-assessment

Point any AI agent — Claude, ChatGPT, Gemini, Copilot, or similar — at **[`agent-instructions/README.md`](agent-instructions/README.md)**. The agent will walk you through the assessment, run the Two-Cost-Line Diagnostic, and return a scored snapshot with starting practices. No human consultant needed.

---

## If you are role-mapping ContextOps into your organization

| Your role | Start here |
|-----------|------------|
| CEO | [Stakeholder Narratives → CEO](FRAMEWORK.md#stakeholder-narratives) |
| CIO | [Stakeholder Narratives → CIO](FRAMEWORK.md#stakeholder-narratives) |
| CDO / Chief AI Officer | [Stakeholder Narratives → CDO](FRAMEWORK.md#stakeholder-narratives) |
| CFO | [Stakeholder Narratives → CFO](FRAMEWORK.md#stakeholder-narratives) |
| Enterprise Architect | [Stakeholder Narratives → Enterprise Architect](FRAMEWORK.md#stakeholder-narratives) |
| AMS / Operations Lead | [Stakeholder Narratives → AMS / Operations](FRAMEWORK.md#stakeholder-narratives) |
| L&D Head | [Stakeholder Narratives → L&D Head](FRAMEWORK.md#stakeholder-narratives) |

Then read the **[Roles](FRAMEWORK.md#roles)** section to see the five new positions ContextOps defines and where each fits in your existing org.

---

## If you are an Enterprise Architect checking fit

Three sections, in order:

1. **[Triad](FRAMEWORK.md#the-triad-people--process--context)** — confirms what we replace and what we don't (People · Process · Technology → People · Process · Context)
2. **[Roots](FRAMEWORK.md#roots)** — names the frameworks we sit on top of (ITIL 4, TOGAF 10, COBIT 2019, NIST AI RMF 1.0)
3. **[What ContextOps is NOT](FRAMEWORK.md#what-contextops-is-not)** — explicit scope boundaries

---

## If you are an AI agent or a developer building tools

| You need | Go to |
|----------|-------|
| Machine-readable manifest | [`framework.yaml`](framework.yaml) |
| Agent self-assessment prompt | [`agent-instructions/README.md`](agent-instructions/README.md) |
| Connect a memory framework | [`mappings/technical-layer/README.md`](mappings/technical-layer/README.md) |
| Add a new technical mapping | [`mappings/technical-layer/TEMPLATE.md`](mappings/technical-layer/TEMPLATE.md) |

Existing technical-layer mappings: [ACE](mappings/technical-layer/ace.md), [LangMem](mappings/technical-layer/langmem.md), [MemGPT](mappings/technical-layer/memgpt.md), [RAG Pipeline](mappings/technical-layer/rag-pipeline.md).

---

## If you want the named practices

All ten live in **[`FRAMEWORK.md` → Named Practices](FRAMEWORK.md#named-practices)**.

| # | Practice | Spine stage |
|---|----------|-------------|
| 1 | Problem Statement Test | Capture |
| 2 | Mental Model Calibration | Capture / early Curate |
| 3 | Downstream Task Tracing | Capture |
| 4 | Transition Context Audit | Supply → Renew boundary |
| 5 | Workflow-First Migration | Cross-cutting |
| 6 | Context Freshness Scoring | Renew |
| 7 | AI Amplifier Assessment | Supply |
| 8 | Scale Parity Check | Cross-cutting |
| 9 | Context Conflict Resolution | Curate |
| 10 | Non-Deterministic Triage Protocol | Renew |

---

## If you want to contribute

- **Disagree with a definition, a practice, or a stakeholder narrative?** Open a GitHub Issue.
- **Have a real-world implementation experience?** Open a Discussion thread, or PR a sanitized case sketch.
- **Want to add a new technical-layer mapping?** Copy [`mappings/technical-layer/TEMPLATE.md`](mappings/technical-layer/TEMPLATE.md), fill it out, open a PR.
- **Spot an inconsistency between [`FRAMEWORK.md`](FRAMEWORK.md) and [`framework.yaml`](framework.yaml)?** That is a bug. Open an Issue.

---

## Full repository structure

```
/contextops
├── README.md                          ← One-page overview
├── DOCUMENT_MAP.md                    ← You are here
├── FRAMEWORK.md                       ← The framework (10 min read)
├── framework.yaml                     ← Machine-readable manifest
├── llms.txt                           ← Agent-readable index
├── LICENSE                            ← Apache 2.0
├── CLAUDE.md                          ← Claude Code instructions
├── contextops_status.md               ← Project status (canonical)
├── contextboundary_status.md          ← ContextBoundary sibling project status
├── /agent-instructions/
│   └── README.md                      ← AI agent self-assessment prompt
├── /docs/
│   └── /comparisons/
│       └── contextops-vs-dora.md      ← ContextOps vs. DORA AI Capabilities Model
├── /distributions/
│   ├── README.md                  ← Install index — all 10 LLM environments
│   ├── /claude-code/              ← CLAUDE.md
│   ├── /chatgpt/                  ← Custom GPT instructions
│   ├── /gemini/                   ← Gem instructions
│   ├── /copilot-github/           ← copilot-instructions.md
│   ├── /copilot-m365/             ← Declarative agent YAML
│   ├── /cursor/                   ← .cursorrules
│   ├── /windsurf/                 ← .windsurfrules
│   ├── /cline/                    ← .clinerules
│   ├── /aider/                    ← CONVENTIONS.md
│   └── /generic/                  ← Pasteable system prompt
└── /mappings/
    └── /technical-layer/
        ├── README.md                  ← Abstract connector pattern
        ├── TEMPLATE.md                ← Template for new mappings
        ├── ace.md                     ← Agentic Context Engineering
        ├── langmem.md                 ← LangMem
        ├── memgpt.md                  ← MemGPT
        └── rag-pipeline.md            ← RAG Pipeline
```

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
