# ContextOps — Distributions

Ready-to-use ContextOps packs for every major AI coding assistant and LLM platform. Pick your environment and follow the install guide.

## Available distributions

| Environment | Primary file | How to install |
|-------------|-------------|----------------|
| [Generic (any LLM)](./generic/) | `system-prompt.md` | Paste into any system prompt or context window |
| [Claude Code](./claude-code/) | `CLAUDE.md` | Place in project root — Claude Code reads it automatically |
| [ChatGPT](./chatgpt/) | `system-prompt.md` | Paste into Custom Instructions |
| [Gemini](./gemini/) | `gem-instructions.md` | Paste into Gem instructions |
| [GitHub Copilot](./copilot-github/) | `copilot-instructions.md` | Place at `.github/copilot-instructions.md` |
| [Copilot M365](./copilot-m365/) | `agent.yml` | Configure via M365 Copilot Studio |
| [Cursor](./cursor/) | `.cursorrules` | Place in project root |
| [Windsurf](./windsurf/) | `.windsurfrules` | Place in project root |
| [Cline](./cline/) | `.clinerules` | Place in project root |
| [Aider](./aider/) | `CONVENTIONS.md` | Pass via `--conventions` flag |

## How it works

Each distribution is a thin wrapper around the same ContextOps core. One source, adapted for each environment's instruction format.

Full framework: https://github.com/kannanokannan/ContextOps
Canonical terminology and decisions: https://github.com/kannanokannan/context-stack
