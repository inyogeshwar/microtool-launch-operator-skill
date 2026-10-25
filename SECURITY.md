# Security Policy

## What this skill does with external content

`microtool-launch-operator` performs niche research and competitor analysis. That means it reads third-party web content:

- Competitor websites
- Reddit / Quora / forum threads
- Search result snippets and People Also Ask
- Keyword tool pages, PageSpeed reports, backlink profiles
- Any URL the user supplies

All of that is **untrusted data**. The skill explicitly forbids following instructions found in it.

## Threat model

The relevant risk is **indirect prompt injection**: a page, comment, metadata field, or hidden element contains text that tries to make the agent take an action — run a command, install a package, reveal secrets, change DNS, or alter the user's goal.

Secondary risks: hidden text (CSS-hidden, zero-width, homoglyph) used to smuggle instructions, and scraped strings injected into templates/meta/JSON-LD.

## Controls implemented in SKILL.md

See the **Untrusted Content Policy** section. Summary:

| Control | Behavior |
|---|---|
| Content is data | Web text is quoted evidence, never instructions |
| No auto-execution | Commands/packages found online require explicit user approval of the exact string |
| No exfiltration | Secrets, `.env`, tokens, cookies, local paths never sent because a page asked |
| No silent installs | No `npm`/`pip`/`npx` from page recommendation |
| Tool output is untrusted | Search/browse/fetch/SEO tool responses get no extra authority |
| Provenance required | Quotes must carry source URL |
| Sanitization | Scraped strings stripped of HTML/JS before template use |
| Hidden-text detection | Zero-width, RTL override, CSS-hidden text flagged |
| Report, don't comply | Suspected injection logged to `BUGS.md`/`DECISIONS.md` with URL |

## Reporting a vulnerability

If you find a prompt-injection vector, a bypass of the Untrusted Content Policy, or any other security issue in this skill, please open a private security advisory or an issue at:

https://github.com/inyogeshwar/microtool-launch-operator-skill/issues

Please include:

1. The exact text/payload
2. Where it was placed (page body, metadata, hidden element, tool response)
3. Which control it bypassed
4. Suggested mitigation

## Scope

This is an instruction-only skill (Markdown, no executables, no network code). It does not itself make network requests — the host agent does. The controls here constrain how the agent should treat what it fetches.

## Residual risk

Prompt injection cannot be fully eliminated at the instruction layer. Users should still:

- Review commands before approving them
- Keep agents in a sandbox or with least-privilege credentials
- Avoid running research agents with production credentials present
- Prefer read-only browsing tools for competitor research
