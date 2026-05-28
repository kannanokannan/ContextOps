# ContextOps

88% of enterprise AI agent pilots fail to reach production. Not model problems — governance, scoping, and ownership problems. Organisations are deploying probabilistic systems without deterministic governance structures to contain them.

ContextOps is the governance layer that fixes this. A vendor-neutral, open-source methodology for capturing, structuring, and supplying organisational context to AI agents — built for enterprise practitioners, not individual prompt optimisation.

**ITIL for AI context. Apache 2.0.**

---

88% of enterprise AI agent pilots fail to reach production in 2026 (Forrester and Anaconda, 2026; corroborated by IDC and the MIT Sloan CIO panel). Not because the models are wrong. Forrester's root-cause analysis finds none of the primary failure modes are model-quality problems — they are scoping, governance, and ownership problems. Organizational context, governance, and operating model gaps are the primary structural cause.

The tools are capable. The plumbing (MCP, agent frameworks, APIs) is maturing. The methodology layer is missing.

ContextOps fills that gap. It sits on top of ITIL, TOGAF, COBIT, and NIST AI RMF — it does not replace them.

---

## Quick Start

1. **Read** [`FRAMEWORK.md`](FRAMEWORK.md) — the framework in ~10 minutes.
2. **Run a self-assessment** — Point any AI agent (Claude, ChatGPT, Gemini, Copilot) at [`agent-instructions/README.md`](agent-instructions/README.md) and the agent will walk you through it.
3. **Connect your existing AI stack** — See [`mappings/technical-layer/`](mappings/technical-layer/) for connector documentation covering RAG pipelines, agent memory frameworks, and orchestration tools.

Not sure where to start? See [`DOCUMENT_MAP.md`](DOCUMENT_MAP.md) — a reader's guide by role and goal.

---

## Repository Structure

```
/contextops
├── README.md                          ← You are here
├── DOCUMENT_MAP.md                    ← Reader's guide by role and goal
├── FRAMEWORK.md                       ← The framework (10 min read)
├── LICENSE                            ← Apache 2.0
├── CLAUDE.md                          ← Claude Code instructions
├── framework.yaml                     ← Machine-readable manifest
├── llms.txt                           ← Agent-readable index (llmstxt.org spec)
├── contextops_status.md               ← Project status (canonical)
├── contextboundary_status.md          ← ContextBoundary sibling project status
├── /agent-instructions/
│   └── README.md                      ← AI agent prompt for self-assessment
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
        ├── ace.md                     ← Agentic Context Engineering mapping
        ├── langmem.md                 ← LangMem mapping
        ├── memgpt.md                  ← MemGPT mapping
        └── rag-pipeline.md            ← RAG Pipeline mapping
```

---

## Connectors

ContextOps maps to technical agent memory and context-management frameworks via the [`mappings/technical-layer/`](mappings/technical-layer/) directory.

Current connectors: [ACE](mappings/technical-layer/ace.md) (Agentic Context Engineering), [LangMem](mappings/technical-layer/langmem.md), [MemGPT](mappings/technical-layer/memgpt.md), [RAG Pipeline](mappings/technical-layer/rag-pipeline.md).

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

---

## Part of the Stack

This project is one of three sibling open-source projects under [github.com/kannanokannan](https://github.com/kannanokannan).

| Project | Question | Repo |
|---------|----------|------|
| ContextOps | How does an org govern its AI context? | [github.com/kannanokannan/ContextOps](https://github.com/kannanokannan/ContextOps) |
| ContextBoundary | Where is data allowed to go? | [github.com/kannanokannan/ContextBoundary](https://github.com/kannanokannan/ContextBoundary) |
| Sthala | Where does the AI actually run? | [github.com/kannanokannan/Sthala](https://github.com/kannanokannan/Sthala) |

Canonical terminology and cross-project decisions: [context-stack](https://github.com/kannanokannan/context-stack)
