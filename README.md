# ContextOps

Enterprise AI agent pilots often fail to reach durable production when governance, scoping, ownership, and operating context are unclear. The failure mode is usually not the model alone. Organizations are deploying probabilistic systems without deterministic governance structures to contain them.

ContextOps is the organizational context governance layer in the context-stack. It answers one question: how does an org govern the context its AI agents depend on? It is vendor-neutral, open-source, and built for enterprise practitioners — not individual prompt optimization.

**ITIL for AI context. Apache 2.0.**

## The Problem

Modern AI systems let interpretation, decision-making, and execution share one trust boundary. That lets probabilistic systems directly own deterministic consequences — the root cause of prompt injection, unsafe automation, context contamination, and authority confusion.

This project is part of the context-stack, which separates interpretation from authority: intelligence proposes, governance validates, execution authorizes. Intelligence can suggest anything. Authority stays deterministic.

Full doctrine: https://github.com/kannanokannan/context-stack

---

Enterprise AI agent pilots routinely stall before durable production. Not because the models are always wrong, but because the surrounding system is under-specified: unclear success criteria, weak tool and data access, stale evaluation coverage, missing ownership, and no operating loop for context drift. Organizational context, governance, and operating model gaps are the structural cause.

The tools are capable. The plumbing (MCP, agent frameworks, APIs) is maturing. The methodology layer is missing.

ContextOps fills that gap. It sits on top of ITIL, TOGAF, COBIT, and NIST AI RMF — it does not replace them.

---

## Quick Start

1. **Read** [`FRAMEWORK.md`](FRAMEWORK.md) — the framework in ~12 minutes.
2. **Run a self-assessment** — Point any AI agent (Claude, ChatGPT, Gemini, Copilot) at [`agent-instructions/README.md`](agent-instructions/README.md) and the agent will walk you through it.
3. **Connect your existing AI stack** — See [`mappings/technical-layer/`](mappings/technical-layer/) for connector documentation covering RAG pipelines, agent memory frameworks, and orchestration tools.

Not sure where to start? See [`DOCUMENT_MAP.md`](DOCUMENT_MAP.md) — a reader's guide by role and goal.

---

## Repository Structure

```
/contextops
├── README.md                          ← You are here
├── DOCUMENT_MAP.md                    ← Reader's guide by role and goal
├── FRAMEWORK.md                       ← The framework (12 min read)
├── LICENSE                            ← Apache 2.0
├── CLAUDE.md                          ← Claude Code instructions
├── framework.yaml                     ← Machine-readable manifest
├── llms.txt                           ← Agent-readable index (llmstxt.org spec)
├── contextops_status.md               ← Project status (canonical)
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

**v0.1** — Active. Published for feedback and field validation.

Ten named practices documented across the full Spine (Capture → Curate → Supply → Renew). See `FRAMEWORK.md` for the current state.

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

This project is part of the [context-stack](https://github.com/kannanokannan/context-stack), a family of open-source projects under [github.com/kannanokannan](https://github.com/kannanokannan). ContextOps, ContextBoundary, and Sthala are the three governance projects. Griha is the product layer above them.

| Project | Layer | Question | Repo |
|---------|-------|----------|------|
| ContextOps | Organizational context governance | How does an org govern its AI context? | [github.com/kannanokannan/ContextOps](https://github.com/kannanokannan/ContextOps) |
| ContextBoundary | Egress governance | Where is data allowed to go? | [github.com/kannanokannan/ContextBoundary](https://github.com/kannanokannan/ContextBoundary) |
| Sthala | Governed runtime reference | Where does the AI actually run? | [github.com/kannanokannan/Sthala](https://github.com/kannanokannan/Sthala) |
| Griha | Product layer | How do the stack principles appear in a working system? | [github.com/kannanokannan/Griha](https://github.com/kannanokannan/Griha) |

Canonical terminology and cross-project decisions live in [context-stack](https://github.com/kannanokannan/context-stack).
