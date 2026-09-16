---
name: programmatic-seo-playbook
description: Replicate the 7 programmatic SEO plays that took Zapier, Clay, Composio, Gamma, Mintlify, HeyGen and HubSpot to #1 in Google and ChatGPT. Use when a company wants to generate pages at scale from its own data (integrations, companies, languages, user content, customer backlinks, free tools) and needs the page type, URL pattern, data source, template and rollout plan chosen for its business. Platform: Google + AI search.
metadata:
  platform: Google, ChatGPT, Perplexity, AI Overviews
---

# Programmatic SEO Playbook

Seven plays, each proven by a company at $100M+ ARR. The skill picks the plays that fit the user's business, then produces the data model, URL pattern, page template, rollout plan and the AI-citation checks for each one.

Numbers below come from the companies' own sitemaps and Ahrefs (pulled Sep 2026). Quote them, don't invent new ones.

## Process

1. **Learn the business** - product, who buys it, what data the company already owns (integrations, customers, catalog, languages, user content), CMS, and how many pages it can realistically ship per week
2. **Score the 7 plays** - for each play: do they have the data, is there search demand, does the page answer a real question (see scoring table)
3. **Pick 1 to 3 plays** - never all seven; one play done at 1,000+ pages beats seven done at 50
4. **Design each play** - entity list, URL pattern, title formula, template sections, unique data per page, internal links, schema
5. **Plan the rollout** - first 50 pages by hand-checked quality, then batches, index monitoring, and the "thin page" kill rule
6. **Set the AI-citation checks** - the query set to test in ChatGPT, Perplexity and AI Overviews, and what to change when a page ranks in Google but isn't cited

## The 7 plays

| # | Play | Who proved it | Data you need | Pages built | Result |
|---|------|---------------|---------------|-------------|--------|
| 1 | A page for every entity in your database | Clay | Your own dataset (companies, people, products) | 20,692 company dossier pages + 476 "generate [industry] leads" tools | 15K AI citations/mo, Perplexity cites Clay 4K times/mo |
| 2 | A page for every pair of things you connect | Zapier | List of integrations or compatible items | 110,000 "[App A] + [App B]" pages | 4.2M organic visits/mo, 161K AI citations/mo (most of any SaaS) |
| 3 | A page for every item × every environment | Composio | Items × frameworks, platforms, use cases | 18,395 "[app] for [framework]" pages | 47K organic visits/mo on 582 keywords |
| 4 | Let users publish the pages | Gamma | Public user-generated content | 120,000+ indexed user decks + 410 guide pages × 24 languages | 3.4M organic visits/mo from 21K keywords |
| 5 | Make every customer link back | Mintlify | A product that lives on the customer's domain | 2,506 pages of its own, 19,800 referring domains | DR 90, ChatGPT cites it more than Perplexity, Gemini and Copilot combined |
| 6 | A page for every language and locale | HeyGen | Languages, regions, formats you support | 102 translate pairs, 68 TTS languages, 260 tool pages, × 12 locales | 1.5M organic visits/mo, 26K AI citations/mo, $200M ARR |
| 7 | A free tool for every job your buyer does | HubSpot | Small jobs adjacent to the product | Website grader, email signature maker, 64 "[tool] vs HubSpot" pages + 7,800 blog posts | 4.0M organic visits/mo, 84K AI citations/mo |

## Scoring table

Score each play 0 to 3 on every column, sum, pick the top scores. Skip any play with a 0 in "answers a question".

| Column | 0 | 1 | 2 | 3 |
|--------|---|---|---|---|
| We have the data | none | could scrape or buy it | partial, in our product | complete, in our database today |
| Search demand exists | nobody searches the pattern | long tail only | steady monthly volume | competitors already rank for it |
| Answers a question | page would be a name swap | answers with one fact | answers with data others don't have | answers and lets the visitor act (tool, download, signup) |
| Path to signup | none | link in footer | CTA relevant to the page | the page IS the product entry point |

## Play design cards

For every chosen play, fill this card:

```
Play: [1-7]
Entity list: [what each page is about, count, where the list lives]
URL pattern: /[type]/[entity-slug]
Title formula: [Entity] [modifier] - [Brand]   (mirror the exact words people search and ask AI)
H1: same as title without the brand
Unique data per page: [3+ fields that change per page, not just the name]
Template sections: intro (entity-specific, 80-150 words) / data block / how-to or use case / related entities / CTA
Internal links: hub page -> every spoke; every spoke -> hub + 3-5 siblings + 1 comparison page
Schema: [Product | SoftwareApplication | Organization | Person | ItemList | FAQPage] + BreadcrumbList
Index rule: noindex until the page has [unique data threshold]; kill pages with 0 impressions after 90 days
First 50: hand-check for accuracy, then batch 500/week
```

### Play notes

**1. Entity pages (Clay).** Works when the data is yours and public elsewhere is scattered. The dossier page answers "who is the CEO of X" or "how much did X raise" and the CTA is "enrich this lead". Google traffic is small (73K/mo), AI citations are large (15K/mo): entity pages get cited more than they get clicked. Add a "generate [industry] leads" tool page per vertical.

**2. Pair pages (Zapier).** The strongest pattern in the set. One template, every combination. Requirements: the pair must be real (both sides exist), the page must show what the pair does (triggers, actions, examples), and the CTA must start the pair. 110,000 pages need a sitemap index, hub pages per app, and a canonical rule so A+B and B+A don't compete.

**3. Item × environment (Composio).** Same idea as pairs but crossed with frameworks, platforms or use cases. Warning from Composio's numbers: 47K Google visits, only 9 ChatGPT citations a month. These pages rank for the integration name ("connect agent to Gmail") but AI is asked the problem ("how do I let my agent use Gmail"). Add the problem phrasing to the title or an FAQ block on every page, or the play ranks in Google and stays invisible in AI.

**4. User-generated pages (Gamma).** Requires a product where users make something shareable. Make public documents indexable by default (Gamma allows crawlers into /docs), give each a clean title from the user's content, add an "explore" layer of guide pages that answer buyer questions ("can AI make a full presentation for me") and translate that layer. Google AI Mode cites Gamma 14.6K times a month off user pages.

**5. Customer backlinks (Mintlify).** Only for products that render on the customer's domain (docs, widgets, hosted pages, badges). Every instance carries a link home. 19,800 referring domains off 2,500 pages gives DR 90. Ask: can our product leave a link on the customer's site by default? If yes, this outranks any content play.

**6. Language pages (HeyGen).** One page per language pair, per language feature, per small tool, then mirror the set into every locale you sell in. Titles mirror the search ("translate video from English to Spanish"). Every added language becomes hundreds of URLs. Use hreflang, one sitemap per locale, and native-quality copy for the top 5 locales.

**7. Free tools (HubSpot).** Build small tools for jobs adjacent to the product (grader, generator, calculator, checker). Tools get cited by AI more than articles about the same topic. Wrap each tool in a "[tool] vs [competitor]" page and 3-5 how-to posts that link to it. Same keyword count as Zapier, half the AI citations: tools beat essays, pair pages beat tools.

## Rollout plan

| Week | Do | Check |
|------|----|-------|
| 1 | Entity list, URL pattern, template, 10 pages by hand | Every page answers its question without the template showing |
| 2 | First 50 pages, hub page, sitemap, schema | Search Console: all 50 indexed within 14 days |
| 3-4 | 500 pages/week | Impressions per page; noindex anything at 0 impressions after 90 days |
| 5+ | Add comparison pages and FAQ blocks with the problem phrasing | AI citation checks below |

## AI-citation checks

Google ranking is not AI citation (Composio ranks, gets 9 ChatGPT citations a month). For every play, build a list of 20-40 buyer questions and run them monthly in ChatGPT, Perplexity and Google AI Overviews. If a page ranks in Google and is not cited:

- Retitle to mirror the question wording ("how do I connect X to Y", not "X Y integration")
- Add an FAQ block with the question as the H2 and a direct 2-sentence answer
- Confirm the page is indexed in Bing (no Bing index, no ChatGPT citation)
- Get the page mentioned on one third-party site: a listicle, a Reddit answer, a partner's docs

## Output format

1. Business summary and the data the company already owns
2. Scoring table with all 7 plays scored
3. Play design cards for the chosen 1 to 3 plays
4. Rollout plan with page counts per week
5. The 20-40 question list for AI-citation checks
6. Risks: thin-content exposure, duplicate pairs, index bloat, and the kill rules for each

## Data access (Ryze MCP)

This skill works best with live account data. Connect the free Ryze MCP once and Claude reads your Google Ads, Meta Ads, GA4 and Search Console directly:

- claude.ai / Claude Desktop: Settings → Connectors → Add custom connector → `https://connector.get-ryze.ai/mcp`
- Claude Code: `claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`
- Cursor: Settings → MCP → add the same URL

Setup guide: https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp
