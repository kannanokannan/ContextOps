# Technical Layer Mappings

> **Path in repo:** `/mappings/technical-layer/README.md`

ContextOps operates at the organizational layer — it defines how human institutions capture, curate, supply, and renew context for AI agents.

Technical frameworks (ACE, LangMem, MemGPT, Semantic Kernel, OpenAI memory, Anthropic context management, Mem0, and others) operate at the agent or application layer — they define how an agent manages its own working context, memory, and retrieval.

These layers are complementary, not competing. This directory documents how specific technical frameworks connect to ContextOps practices.

---

## The Three Connection Seams

Every technical framework that manages agent context connects to ContextOps at three seams:

| Technical Operation | ContextOps Stage |
|---------------------|-----------------|
| Acquire / Ingest / Capture / Grow | **Capture** |
| Refine / Compress / Curate / Consolidate | **Curate** |
| Reflect / Renew / Update / Evolve | **Renew** |

Most technical frameworks focus on one or two of these seams. None of them governs the human decisions of who owns context, who approves it, when it must be updated for organizational (not technical) reasons, or how cross-agent consensus is maintained when multiple agents diverge.

That is where ContextOps operates.

---

## Why This Directory Exists

A framework author's job is not to prescribe which technical tools an organization should use. The technical landscape moves too fast — what is standard today may be deprecated within 18 months. ContextOps is therefore framework-neutral by design.

This directory exists for two reasons:

1. **To help practitioners connect what they already have to what they need.** If an organization is already running LangChain agents with LangMem, ContextOps tells them which Spine stages those tools already cover and which gaps they need to fill organizationally.

2. **To make the seam explicit.** The boundary between "what the technical layer does" and "what the organization must do" is not obvious. These mappings name the seam concretely for each framework.

---

## Available Mappings

- [ACE — Agentic Context Engineering](ace.md)
- [LangMem — Long-term agent memory SDK](langmem.md)
- [MemGPT — Virtual context management](memgpt.md)

Additional mappings to be added as the technical landscape evolves and as contributors submit them.

---

## Adding a Mapping

Use [TEMPLATE.md](TEMPLATE.md) to document a new framework's connection to ContextOps. Pull requests welcome.

Criteria for inclusion:
- The framework must be publicly documented (paper, repo, or product documentation)
- It must operate at the agent, application, or model layer — not the organizational layer
- The mapping must be specific to ContextOps stages, not generic statements about AI

---

## What This Directory Is Not

- Not an endorsement of any specific technical framework
- Not a comparison or ranking
- Not a buying guide
- Not a substitute for evaluating frameworks against your organization's actual requirements

ContextOps is vendor-neutral and framework-neutral. The mappings exist to help practitioners understand the seam between technical tooling and organizational methodology.

---

*Part of ContextOps v0.1. Licensed under Apache 2.0.*
