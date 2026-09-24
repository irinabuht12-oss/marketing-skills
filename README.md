# Claude Skills for Marketing: 49 free marketing skills for Claude Code and claude.ai

[![Claude Skills for Marketers](https://raw.githubusercontent.com/irinabuht12-oss/marketing-skills/main/ghf-toplight.png)](https://get-ryze.ai/blog/claude-marketing-skills-complete-guide)

49 free Claude skills for marketing (marketing skills for Claude Code, Claude Desktop and claude.ai): Google Ads, Meta Ads, SEO and AI visibility, with the Ryze MCP (a Google Ads MCP and Meta Ads MCP in one connector) for live account data. Built by Ryze AI.

## Install in 30 seconds

**1. Connect the Ryze MCP** (free, gives Claude your live Google Ads / Meta Ads / GA4 / Search Console data):

```
claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp
```

In claude.ai or Claude Desktop: Settings → Connectors → Add custom connector → paste `https://connector.get-ryze.ai/mcp`. Works in Cursor and ChatGPT too. [2-minute setup guide →](https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp)

**2. Install the skills** as a Claude Code plugin (the connector comes bundled):

```
claude plugin marketplace add irinabuht12-oss/marketing-skills
claude plugin install marketing-skills@ryze
```

Or copy them by hand:

```bash
git clone https://github.com/irinabuht12-oss/marketing-skills && cp -r marketing-skills/skills/* ~/.claude/skills/
```

Or download everything: [all-marketing-skills.zip](https://github.com/irinabuht12-oss/marketing-skills/blob/main/all-marketing-skills.zip)

Product pages: [Google Ads MCP](https://www.get-ryze.ai/google-ads-mcp) · [Meta Ads MCP](https://www.get-ryze.ai/meta-ads-mcp)

**3. Ask:** "audit my Google Ads for wasted spend", "why did my Meta CPA go up this week", "which AI engines cite my site".

**[📖 Full guide: 98 Claude marketing skills, ranked by job →](https://get-ryze.ai/blog/claude-marketing-skills-complete-guide)**

---

## Folders

- **Claude skills for Google Ads** — audits, diagnostics, and optimization skills for Google (and cross-platform Google + Meta) campaigns
- **Claude skills for Meta Ads** — creative fatigue, audience overlap, retargeting, and Meta-specific audits
- **Claude skills for SEO** — end-to-end SEO assistant and programmatic SEO builder
- **Claude skills for AI visibility** — get your brand cited by ChatGPT, Claude, Gemini, Perplexity, and AI Overviews

---

## What's Inside

| Skill | What It Does |
|-------|--------------|
| **Google Ads Audit** | Find wasted spend, search term leaks, negative keyword gaps, bid strategy issues |
| **Meta Ads Audit** | Detect creative fatigue, audience overlap, tracking problems, scaling opportunities |
| **LinkedIn Ads Audit** | Analyze CTR benchmarks, audience quality, lead gen form friction, budget efficiency |
| **Reddit Ads Audit** | Fix community targeting, creative fit, subreddit performance, bid inefficiencies |
| **Ad Spend Allocator** | Get budget reallocation recommendations across channels |
| **A/B Test Analyzer** | Calculate statistical significance and sample size requirements |
| **Competitor Teardown** | Analyze any landing page for positioning and messaging |
| **Landing Page Audit** | Find conversion killers and CTA issues |
| **UTM & Tracking Generator** | Create consistent UTM links and GA4 event names |
| **Email Sequence Writer** | Write full nurture sequences with subject lines |
| **Content Repurposer** | Turn 1 blog post into LinkedIn, Twitter, email, and video content |
| **Programmatic SEO Builder** | Build scalable page templates with schema markup |
| **Programmatic SEO Playbook** | The 7 plays that got Zapier, Clay, Composio, Gamma, Mintlify, HeyGen and HubSpot to #1 in Google and ChatGPT, scored and designed for your company |
| **ICP Research Assistant** | Build buyer personas with pain points, objections, buying triggers |
| **E2E SEO Assistant** | Get technical audits, content gaps, backlink opportunities, content briefs |

---

## Common questions

**What are Claude skills for marketing?** Markdown instructions Claude loads on demand: each skill tells Claude how to audit a Google Ads account, diagnose Meta creative fatigue, build a programmatic SEO plan or check AI visibility, step by step, with the data it should pull.

**How do I install marketing skills in Claude Code?** `claude plugin marketplace add irinabuht12-oss/marketing-skills` then `claude plugin install marketing-skills@ryze`. Or copy the `skills/` folders into `~/.claude/skills/`.

**Do the skills need the Ryze MCP?** No. They run on pasted exports too, but with the free connector (`claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`) Claude reads your live Google Ads, Meta Ads, GA4 and Search Console data itself.

**Do they work in Cursor, ChatGPT or Claude Desktop?** Yes. The skills are plain Markdown and the connector URL is the same in every client.

**Are they free?** Yes, all 49, MIT licensed, no signup.

---

## Requirements

- Claude Pro, Max, Team or Enterprise at [claude.ai](https://claude.ai), or Claude Code / Cursor
- The free [Ryze MCP connector](https://connector.get-ryze.ai/mcp) for live account data (skills also run on pasted exports)

---

## Support

These skills are **100% free**.

Need help? Contact us at **hello@get-ryze.ai**

---

Built by [Ryze AI](https://get-ryze.ai) — AI that runs your paid ads
