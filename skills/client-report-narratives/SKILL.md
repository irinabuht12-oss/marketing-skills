---
name: client-report-narratives
description: Takes your raw campaign performance data and writes the executive summary paragraph that goes at the top of the report. The plain English explanation of what happened, why it happened, and what's being done about it. The part every client actually reads. Platform: Google and Meta.
metadata:
  platform: Google and Meta
---

# 5/ Client Report Narratives — Google + Meta

## What it does
Takes your raw campaign performance data and writes the executive summary paragraph that goes at the top of the report. The plain English explanation of what happened, why it happened, and what's being done about it. The part every client actually reads.

## How it works
Feed Claude the key metrics for the period — spend, conversions, CPA, ROAS, CTR, impression share, and any notable changes. It identifies the most important trends, connects them to likely causes, and writes a clear narrative that a non-technical stakeholder can understand without asking follow-up questions.

## Practical example
You paste in last month's data: $45K spend, 1,180 leads at $38 CPA (down from $44), ROAS 4.2x. Claude writes: "March delivered 1,180 leads at $38 CPA, a 14% improvement over February. The primary driver was the new UGC creative set launched mid-month which outperformed static images by 2.3x on Meta prospecting. Google Search held steady at $29 CPA with branded terms contributing 34% of volume. One area to watch — Meta retargeting CPA increased 18% as the audience pool shrinks, recommending a lookalike refresh for April."

## What you get back
- Executive summary paragraph ready to paste into your report
- Key wins highlighted with specific numbers
- Problem areas flagged with context, not just red numbers
- Forward-looking recommendations tied to the data
- Written in a tone that matches client communication, not ad platform jargon

## When to use it
- Weekly and monthly client reporting
- Internal stakeholder updates where you need to explain performance fast
- QBR prep when you need narratives for multiple accounts
- Any time you're staring at a spreadsheet and need to turn it into words

## Data access (Ryze MCP)

This skill works best with live account data. Connect the free Ryze MCP once and Claude reads your Google Ads, Meta Ads, GA4 and Search Console directly:

- claude.ai / Claude Desktop: Settings → Connectors → Add custom connector → `https://connector.get-ryze.ai/mcp`
- Claude Code: `claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`
- Cursor: Settings → MCP → add the same URL

Setup guide: https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp
