---
name: attribution-model-comparison
description: Runs your conversion data through different attribution models side by side — last click, first click, linear, time decay, position based, and data-driven. Shows you how credit shifts between campaigns depending on the model so you can make better budget decisions instead of over-investing in last-touch campaigns. Platform: Google and Meta.
metadata:
  platform: Google and Meta
---

# 26/ Attribution Model Comparison — Google + Meta

## What it does
Runs your conversion data through different attribution models side by side — last click, first click, linear, time decay, position based, and data-driven. Shows you how credit shifts between campaigns depending on the model so you can make better budget decisions instead of over-investing in last-touch campaigns.

## How it works
Claude takes your multi-touch conversion path data and applies each attribution model to the same dataset. It then compares how each campaign's attributed conversions and ROAS change under different models, highlighting campaigns that look great under last-click but contribute nothing at first-touch (and vice versa).

## Practical example
Under last-click attribution, your Google Brand campaign gets credit for 420 conversions at $18 CPA, making it your "best" campaign. But when Claude runs first-click attribution, Brand drops to 31 conversions — most of those users actually discovered you through Meta prospecting (which jumps from 89 to 340 attributed conversions). Linear attribution puts Meta prospecting at 215 and Brand at 190, giving a more balanced picture. Claude recommends shifting 20% of Brand budget to Meta prospecting, which is actually originating most of your pipeline.

## What you get back
- Side-by-side conversion and ROAS comparison across all models for every campaign
- Campaigns most affected by model choice (high variance = their role is misunderstood)
- Upper-funnel campaigns being undervalued under last-click
- Lower-funnel campaigns being over-credited under last-click
- Budget reallocation recommendations based on a blended attribution view
- Recommended "working model" for your specific account based on funnel length and touchpoint patterns

## When to use it
- When making budget allocation decisions to avoid last-click bias
- During QBRs to show clients the full picture of campaign value
- When upper-funnel campaigns are on the chopping block due to "poor" last-click ROAS
- Before cutting any campaign that might be silently feeding conversions elsewhere

## Data access (Ryze MCP)

This skill works best with live account data. Connect the free Ryze MCP once and Claude reads your Google Ads, Meta Ads, GA4 and Search Console directly:

- claude.ai / Claude Desktop: Settings → Connectors → Add custom connector → `https://connector.get-ryze.ai/mcp`
- Claude Code: `claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`
- Cursor: Settings → MCP → add the same URL

Setup guide: https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp
