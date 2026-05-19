# ContextOps

**Enterprise AI Context Framework. ITIL for AI context.**

A vendor-neutral, open-source AI governance methodology for capturing, structuring, governing, and supplying organizational context to AI agents. Built for practitioners doing context engineering for the enterprise — not for individual prompt optimization.

---

## What This Is

88% of enterprise AI agent pilots fail to reach production in 2026 (Forrester and Anaconda, 2026; corroborated by IDC and the MIT Sloan CIO panel). Not because the models are wrong. Forrester's root-cause analysis finds none of the primary failure modes are model-quality problems — they are scoping, governance, and ownership problems. The organizational harness is the primary structural cause.

The tools are capable. The plumbing (MCP, agent frameworks, APIs) is maturing. The methodology layer is missing.

ContextOps fills that gap. It sits on top of ITIL, TOGAF, COBIT, and NIST AI RMF — it does not replace them.

---

## Quick Start

1. **Read** [`FRAMEWORK.md`](FRAMEWORK.md) — the framework in ~10 minutes.
2. **Run a self-assessment** — Point any AI agent (Claude, ChatGPT, Gemini, Copilot) at [`agent-instructions/README.md`](agent-instructions/README.md) and the agent will walk you through it.
3. **Connect your existing AI stack** — See [`mappings/technical-layer/`](mappings/technical-layer/) for connector documentation.

Not sure where to start? See [`DOCUMENT_MAP.md`](DOCUMENT_MAP.md) — a reader's guide by role and goal.

Not sure where to start? See [`DOCUMENT_MAP.md`](DOCUMENT_MAP.md) — a reader's guide by role and goal.

---

## Repository Structure

```
/contextops
├── README.md                          ← You are here
├── DOCUMENT_MAP.md                    ← Reader's guide by role and goal
├── FRAMEWORK.md                       ← The framework (10 min read)
├── LICENSE                            ← Apache 2.0
├── framework.yaml                     ← Machine-readable manifest
├── llms.txt                           ← Agent-readable index (llmstxt.org spec)
├── /agent-instructions/
│   └── README.md                      ← AI agent prompt for self-assessment
├── /docs/
│   └── /comparisons/
│       └── contextops-vs-dora.md      ← ContextOps vs. DORA AI Capabilities Model
└── /mappings/
    └── /technical-layer/
        ├── README.md                  ← Abstract connector pattern
        ├── TEMPLATE.md                ← Template for new mappings
        ├── ace.md                     ← Agentic Context Engineering mapping
        ├── langmem.md                 ← LangMem mapping
        └── memgpt.md                  ← MemGPT mapping
```

---

## Connectors

ContextOps maps to technical agent memory and context-management frameworks via the [`mappings/technical-layer/`](mappings/technical-layer/) directory.

Current connectors: [ACE](mappings/technical-layer/ace.md) (Agentic Context Engineering), [LangMem](mappings/technical-layer/langmem.md), [MemGPT](mappings/technical-layer/memgpt.md).

To add a connector for a framework not listed, copy [`mappings/technical-layer/TEMPLATE.md`](mappings/technical-layer/TEMPLATE.md) and open a PR.

---

## Compare

| vs. | Summary | Doc |
|-----|---------|-----|
| DORA AI Capabilities Model | DORA covers the SDLC vertical; ContextOps covers the enterprise horizontal. Complementary, not competing. | [`docs/comparisons/contextops-vs-dora.md`](docs/comparisons/contextops-vs-dora.md) |

---

## Status

**v0.1** — Draft. Published for feedback, not yet certified or finalized.

Ten named practices documented across the full Spine (Capture → Curate → Supply → Renew). Some sections remain stubbed pending field validation. See `FRAMEWORK.md` for the current state.

---

## How to Contribute

- **Issues** — Disagree with a definition, a practice, or a stakeholder narrative? Open one.
- **Pull requests** — Improvements to the framework, new technical-layer mappings, or organizational case sketches welcome.
- **Discussions** — For broader debate on direction and scope.

---

## License

Apache 2.0. Enterprises can use, modify, and build commercial offerings on top of this framework. See [`LICENSE`](LICENSE) for the full text.

---

*ContextOps is the discipline of building and maintaining shared understanding of context across every link in the corporate ecosystem that touches an AI agent's behavior.*
