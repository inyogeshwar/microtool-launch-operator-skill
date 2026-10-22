---
name: microtool-launch-operator
description: Universal, agent-agnostic operator workflow for launching a monetizable micro-tool website from research through deployment, SEO, indexing, and AdSense. Use when building a small utility/tool (calculator, converter, formatter, generator, finder) for organic search traffic and monetization. Works across Claude Code, Cursor, OpenCode, Codex, Antigravity, and any model via OpenRouter.
---

# Micro-Tool Launch Operator

## Overview

A disciplined, evidence-based workflow to go from idea to a live, indexable micro-tool website ready for AdSense. Phase-driven with gates, stop conditions, and verifiable outputs. Model-agnostic and tool-agnostic.

## When to Use

- "Build a micro-tool website from scratch"
- "Validate and launch a utility site for SEO traffic"
- "Go from idea to deployment and monetization"
- "Need a safe, repeatable launch process across any agent"

**Do NOT use for:** Large SaaS with auth/payments, YMYL (medical/legal/financial) without expert review, content farms, programmatic spam, black-hat SEO.

## Core Principles

1. **Operator mindset** - Ask, confirm, show evidence. Don't guess.
2. **Verify first** - Use official docs for commands/limits/prices/URLs. Mark `[UNVERIFIED]` if unknown.
3. **Phase discipline** - Follow order unless explicitly approved to skip.
4. **Evidence-based** - Every phase ends with proof (files/URLs/commands/tests).
5. **Safety first** - Domain purchase, DNS changes, AdSense application require confirmation.
6. **Natural language** - Use clear, direct communication.
7. **Token efficient** - Load `SKILL.md` first, references only when needed.

## Process (Phases 0-16)

### Phase 0: Inputs & Project Brief
- Collect: interests/skills, time/week, budget, target country/language, coding comfort, agent/model, existing domain
- Create `PROJECT.md` with goals and 90-day success metric
- **Gate G0:** Brief confirmed

### Phase 1: Niche & Problem Research
- Generate 10 ideas, score by pain/demand/competition weakness/simplicity/monetization/edge (100 pts)
- Pick top 1, keep backups
- Validate via autocomplete/People Also Ask, forums, keyword tools, trends
- Output: problem statement, demand evidence, 3 competitor URLs
- **Gate G1:** Viable with weak competition

### Phase 2: Competitor Analysis
- Analyze UX, features, gaps, mobile, speed, monetization
- Write differentiation: "We will beat X by Y because Z"
- **Gate G2:** >= 3 concrete improvements

### Phase 3: Keywords & Domain
- Build keyword map (primary/secondary/long-tail/questions)
- Find short `.com` if possible, check availability/price/renewal/trademark
- **Rule:** No domain purchase without confirmation
- **Gate G3:** Domain shortlisted + approved

### Phase 4: Project Setup
- Init Astro project, Git, dependencies
- Add design system/tools as needed
- Create tracking files: `PROJECT.md`, `DECISIONS.md`, `CHECKLIST.md`, `BUGS.md`, `CONTENT-PLAN.md`, `BACKLINKS.md`, `LAUNCH-REPORT.md`
- **Gate G4:** `npm run dev` works, first commit

### Phase 5: Build
- Build order: core tool → layout → content → FAQ → trust pages → SEO/meta → analytics → polish
- Plan first, approve before coding
- Mobile-first, MPA, accessible, fast, no placeholders/copied content/secrets
- **Gate G5:** Core tool works on desktop+mobile

### Phase 6: QA
- Functional, responsive (360-1440), accessibility, performance (LCP/CLS), SEO basics
- Log bugs in `BUGS.md` by severity
- **Gate G6:** No P0/P1 bugs

### Phase 7: On-Page SEO & Content
- Useful content explaining tool/use cases/limits
- Unique title/meta, H1, canonical, OG/Twitter, alt text
- FAQ with real questions
- **Gate G7:** Metadata + content reviewed

### Phase 8: Trust, Legal & Readiness
- Create Privacy Policy, About, Terms, Contact (+ Disclaimer/Cookie if needed)
- Link in header/footer/home, real contact, no prohibited content
- **Gate G8:** Pages live and linked

### Phase 9: Analytics & Search Consoles
- Google Analytics 4
- Google Search Console (domain property, DNS verification)
- Bing Webmaster Tools
- **Gate G9:** Tracking + consoles configured, sitemap ready

### Phase 10: Deployment
- Deploy to Cloudflare Pages (or suitable host)
- Add `public/_headers` to `noindex` `*.pages.dev/*`
- Smoke test all critical paths
- **Gate G10:** Live preview + smoke test passed

### Phase 11: Custom Domain & DNS
- Add domain to host, update nameservers at registrar
- SSL active, www → root 301 redirect
- Keep MX/TXT records intact
- **Confirmation required**
- **Gate G11:** Domain live, SSL valid, redirects correct

### Phase 12: Indexing
- Submit sitemap to GSC, request indexing for key URLs
- Submit to Bing
- Monitor coverage
- **Gate G12:** Sitemap accepted

### Phase 13: AdSense
- Pre-check: useful content, legal pages, policy compliance, live on domain
- Apply via official AdSense
- If approved: add `ads.txt`, deploy, verify, place ads carefully
- No guarantees, follow policies
- **Gate G13:** Ready/applied/approved + ads.txt as applicable

### Phase 14: Post-Launch 30/60/90
- Week 1: fix coverage/mobile/speed
- Day 30: improve low-CTR, add pages, start editorial links
- Day 60: optimize top pages, improve UX
- Day 90: double-down/pivot/kill based on data
- **Gate G14:** `LAUNCH-REPORT.md` with decision

### Phase 15: International Expansion
- Validate demand by country/language
- Choose dedicated site or subpaths with hreflang
- Native content, correct implementation
- **Gate G15:** Strategy + hreflang validated

### Phase 16: Backlinks
- Audit competitors
- Focus on editorial, relevant links
- Follow search engine link spam policies
- Log all outreach in `BACKLINKS.md`
- **Gate G16:** Safe plan in place

## Gates Quick Reference
See `references/checklist.md` for full checklist.

## Stop Conditions
Stop and confirm before proceeding if:
- Domain purchase/DNS/nameserver changes
- AdSense application before readiness check
- Paid/link schemes or spam tactics
- YMYL without expert review
- Copyright/piracy/hacking/fake reviews/income/testimonials/own ad clicks/buying traffic
- Secrets/credentials required
- Repeated failures with no new info

## Response Format
```text
PHASE: <0-16> — <name>
GOAL: <one line>
STATUS: <done/in progress/blocked>
DONE: <completed>
VERIFIED: <proof>
NEED FROM USER: <max 3>
NEXT: <next step>
```

## References
- `references/full-playbook.md` - Complete detailed workflow
- `references/prompts.md` - Copy-paste prompts
- `references/corrections.md` - Verified corrections
- `references/checklist.md` - Gates checklist
- `templates/project-brief.md` - Project brief
- `templates/handoff.md` - Phase handoff

## Quick Start
1. Load this skill
2. Run Phase 0, create `PROJECT.md`
3. Follow phases in order with gates
4. Show evidence at each step
5. Never skip stop conditions
