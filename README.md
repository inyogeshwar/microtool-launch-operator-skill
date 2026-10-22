# Micro-Tool Launch Operator Skill

A universal, agent-agnostic skill to take a micro-tool website from idea to live deployment, SEO, indexing, and AdSense monetization.

## Structure

```
skills/microtool-launch-operator/
├── SKILL.md
├── references/
│   ├── full-playbook.md
│   ├── prompts.md
│   ├── corrections.md
│   └── checklist.md
└── templates/
    ├── project-brief.md
    └── handoff.md
```

## Compatible Agents

Works with Claude Code, Cursor, OpenCode, Codex, Antigravity, GitHub Copilot, and any agent using OpenRouter or direct APIs.

## Usage

1. Copy `skills/microtool-launch-operator/` to your agent's skills/rules directory
2. Tell your agent: "Build a micro-tool website from research to AdSense"
3. The skill will guide through phases 0-16 with gates, verification, and safety checks

## Features

- Phase-driven workflow (research → validate → build → deploy → SEO → AdSense)
- Agent-agnostic and model-agnostic
- Evidence-based with decision gates
- Safety stop conditions for destructive actions
- Token-efficient with progressive disclosure
- Hinglish-friendly communication

## License

MIT
