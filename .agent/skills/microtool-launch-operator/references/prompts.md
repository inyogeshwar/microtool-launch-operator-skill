# Prompt Library (Copy-Paste)

## Build Prompt
```text
I have initialized a new Astro project. Use the Astro docs MCP, tailwind-4-docs skill, web-design-guidelines skill, and @DESIGN.md.

Name: <SITE_NAME>
Domain: <DOMAIN>

Website description:
<1–2 lines: what it does, who it is for, key features>

Competitor: <COMPETITOR_URL>
Analyze it, list what it does poorly, and build a better version. Do not copy its design or UI.

Requirements:
- Core tool works without login
- Mobile-first responsive
- Multi-page application (MPA), not SPA
- Accessible labels, keyboard support, focus states
- Fast: no unnecessary JS
- No placeholder lorem ipsum

First give me a plan. Do not write code until I approve.
```

## On-Page SEO Prompt
```text
Do on-page SEO for this website.

Primary keyword: <KEYWORD>
Supporting keywords:
<list>

Requirements:
- Unique title and meta description
- One H1, logical H2/H3
- 800–1,200 words of genuinely useful content
- FAQ section with 6 questions
- Internal links to relevant pages
- OG/Twitter meta tags
- Canonical URL
- Image alt text
- No keyword stuffing, no fake claims
```

## Legal Pages Prompt
```text
Create these pages with real, specific content for this website:
- Privacy Policy
- About Us
- Terms & Conditions
- Contact Us

Make them clearly visible on the home page and in the footer.
Use a multi-page application structure.
Do not use placeholder text.
```

## 404 + robots + sitemap
```text
Add custom 404 and 500 pages. Create sitemap.xml for all pages and robots.txt referencing the sitemap. Use https://<domain>.
```

## Deploy to Cloudflare Pages
```text
Deploy this Astro website to Cloudflare Pages. Add a deploy script to package.json. Use Astro docs MCP if needed. Then create public/_headers to noindex the pages.dev preview domain.
```

## GA4 Tag
```text
Add this GA4 tag inside the <head> of every page:
<GTM/GA4_TAG>

Tell me which files changed.
```

## International Expansion
```text
Convert this website to rank for "<local keyword>" in <country>.
Add hreflang for <language>.
Do not create /xx/ subpages; make the root domain 100% <language>.
Primary keyword: <...>
Supporting keywords: <...>
Localize content, units, FAQ, meta, OG, schema. Keep functionality identical.
```

## Editorial Backlink
```text
Add a contextual dofollow backlink to https://target.com in the main content of the most relevant page — not header/footer/sidebar.
Anchor: "<natural anchor>"
Write 1–2 sentences explaining why it is useful.
This is editorial, not paid; do not add rel="nofollow" or rel="sponsored".
Show exact HTML, file path, surrounding paragraph.
```
