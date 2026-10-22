# Verified Corrections

| Claim | Correct | Notes |
|---|---|---|
| Cloudflare Pages = 100k views/day | Static Pages unmetered/fair use; 500 builds/month. 100k/day applies to Workers/Pages Functions. | Verify current Cloudflare docs |
| `analytics.com` | `analytics.google.com` | GA4 |
| `ads.g.com` | `adsense.google.com/start/` | AdSense start page; `ads.google.com` is Google Ads |
| Delete all DNS + add `8.8.8.8` | Don't delete MX/TXT. Change nameservers to Cloudflare. `8.8.8.8` is Google DNS, not hosting IP. | Critical |
| `www` as separate custom domain | Prefer root + `www` 301 redirect to root (or vice versa). Avoid duplicate indexable versions. | Canonicalization |
| 10 users/day required for AdSense | Advice, not official minimum. Focus on policy/compliance/content. | No guarantee |
| 600 words = SEO requirement | No fixed word count. Useful depth matters more than length. | Quality > count |
| FAQ schema = guaranteed rich results | FAQ rich results largely removed for most sites. Use for UX, not guaranteed visibility. | Don't rely on it |
| Domain keyword = direct ranking factor | Not a direct ranking factor. Branding/CTR matter more. | Minor signal historically |
| hreflang = ranking factor | No. Helps serve correct language version to users. | Correct implementation important |
| `lang` attribute = language detection | Google doesn't use `lang` for language detection. Good for accessibility. | Don't depend on it |
| Gemini CLI free | Deprecated 18 Jun 2026. | Use alternatives |
| Cloudflare acquired Astro | True (16 Jan 2026). | Contextual |
| Paid links okay if hidden? | Only with `rel="sponsored"` or `rel="nofollow"`. Otherwise link spam. | Policy strict |
| Own-network links safe | Risky if primary purpose is ranking manipulation. Keep editorial, limited, relevant. | Log everything |

## Cloudflare CLI
- `cf` CLI exists (beta, Workers-focused). 
- For Pages static deployments, `wrangler` is still the recommended/common path.
- `cf migrate` can convert Wrangler projects.
- Check current docs before using `cf`.

## OpenRouter (Free Models) Notes
- `openrouter/free` exists; `minimax/minimax-m3.1-flash:free` has large context.
- Free tiers have rate limits (can change). Free models may train on prompts.
- Non-Claude routing is officially unsupported in some contexts.
- Always verify current pricing/limits on OpenRouter.
