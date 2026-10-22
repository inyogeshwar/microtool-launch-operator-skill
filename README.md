# Micro-Tool Launch Operator

A universal, agent-agnostic skill to take a micro-tool website from idea to live deployment, SEO, indexing, and AdSense monetization.

Works with **Claude Code, Cursor, OpenCode, Codex, Antigravity, GitHub Copilot, Windsurf** and any AI agent using **OpenRouter** or direct APIs.

## Quick Start

### Vercel Skills CLI (Works with 70+ agents)

The [vercel-labs/skills](https://github.com/vercel-labs/skills) CLI is the fastest and most universal way to install this skill.

```bash
npx skills add inyogeshwar/microtool-launch-operator-skill
```

Browse available skills before installing:

```bash
npx skills add inyogeshwar/microtool-launch-operator-skill --list
```

Install only this skill:

```bash
npx skills add inyogeshwar/microtool-launch-operator-skill --skill microtool-launch-operator
```

> **Note:** Installing a single skill copies only `skills/<name>/`, not the entire repo. You'll still get the core `SKILL.md`, but some files under `references/` may not be copied. For the full experience with prompts, checklists, templates and references, it's recommended to install the whole repo or clone it.

## Prefer a native integration?

### Claude Code (Recommended)

**Option 1: Marketplace**

```bash
/plugin marketplace add https://github.com/inyogeshwar/microtool-launch-operator-skill.git
/plugin install microtool-launch-operator@microtool-launch-operator-skill
```

**Option 2: Local plugin dir**

```bash
git clone https://github.com/inyogeshwar/microtool-launch-operator-skill.git
claude --plugin-dir ./microtool-launch-operator-skill
```

### Cursor

Copy `skills/microtool-launch-operator/` to `.cursor/skills/` in your project. Keep short policies in `.cursor/rules/*.mdc`. Avoid pasting the full skill into rules.

### OpenCode

Copy `skills/microtool-launch-operator/` to `.opencode/skills/` (project-local) or `~/.config/opencode/skills/` (global). Use OpenCode's built-in `skill` tool to load it. You can also add custom commands under `.opencode/commands/` if needed.

### Codex (CLI v0.122+)

```bash
codex plugin marketplace add inyogeshwar/microtool-launch-operator-skill
codex plugin add microtool-launch-operator@microtool-launch-operator-skill
```

Once installed, invoke it in chat with `@microtool-launch-operator`.

### Antigravity

For Google Antigravity, copy `skills/microtool-launch-operator/` to `.agent/skills/` in your project or to the global Antigravity skills directory. See [Antigravity Skills Docs](https://antigravity.google/docs/skills) for the latest path.

### Other Agents

This skill is pure Markdown. It works with any agent that accepts custom instructions, system prompts or rules files. Just copy `skills/microtool-launch-operator/` into your agent's expected location or paste `SKILL.md` directly.

## How to Use

Once loaded, just tell your agent:

```text
Build a micro-tool website from research to AdSense.
```

Or be explicit:

```text
Read skills/microtool-launch-operator/SKILL.md and act as the Micro-Tool Launch Operator. Start at Phase 0. Ask me max 3 questions at a time.
```

The agent will follow the full operator workflow step by step with verification gates, safety checks, and evidence at every phase.

## Structure

```text
skills/microtool-launch-operator/
├── SKILL.md              # Core workflow, gates, stop conditions & rules
├── references/
│   ├── full-playbook.md  # Complete detailed runbook (Phases 0-16)
│   ├── prompts.md        # Ready-to-paste prompts for every phase
│   ├── corrections.md    # Verified fixes (Cloudflare, AdSense, DNS, hreflang, etc.)
│   └── checklist.md      # Phase-wise gates checklist
└── templates/
    ├── project-brief.md  # Project brief template
    └── handoff.md        # Clean phase handoff format
```

## Features

- **Phase-Driven** – Follows a strict path from research to AdSense
- **Agent-Agnostic** – Works across almost every modern coding agent
- **Model-Agnostic** – Runs fine on OpenRouter free/paid models
- **Evidence-Based** – Requires proof before moving to next phase
- **Safety-First** – Asks confirmation before domain, DNS or AdSense actions
- **Token-Efficient** – Progressive disclosure, only loads references when needed
- **Hinglish-Friendly** – Natural, practical communication style

## License

[MIT](LICENSE)
