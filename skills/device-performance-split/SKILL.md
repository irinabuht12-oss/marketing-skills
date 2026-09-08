---
name: device-performance-split
description: Analyzes how your campaigns perform across mobile, desktop, and tablet. Identifies where device performance diverges significantly and recommends bid adjustments, campaign splits, or creative/landing page changes to capture the gap. Platform: Google and Meta.
metadata:
  platform: Google and Meta
---

# 25/ Device Performance Split — Google + Meta

## What it does
Analyzes how your campaigns perform across mobile, desktop, and tablet. Identifies where device performance diverges significantly and recommends bid adjustments, campaign splits, or creative/landing page changes to capture the gap.

## How it works
Claude segments all your campaign data by device type and compares CPA, CVR, CTR, bounce rate, and average order value. It identifies campaigns where one device significantly outperforms or underperforms others, then determines whether the issue is ad-side (creative not working on mobile), landing-page-side (poor mobile experience), or audience-side (different intent by device).

## Practical example
Your B2B lead gen campaigns show desktop CPA at $41 with 3.8% CVR and mobile CPA at $78 with 1.6% CVR. But mobile accounts for 58% of clicks because that's where the impressions are. Claude digs deeper and finds the landing page form has 9 fields that are painful on mobile, and the page load time on mobile is 4.2 seconds vs 1.8 on desktop. Recommendation: create a simplified mobile form (3 fields), fix mobile page speed, and reduce mobile bid adjustments by 25% until the fixes are live to stop the bleeding.

## What you get back
- Device performance comparison across all campaigns with key metrics
- Campaigns with the largest device performance gaps flagged
- Root cause analysis: is the gap from creative, landing page, or audience differences
- Bid adjustment recommendations by device per campaign
- Campaign split recommendations for cases where devices need completely different strategies

## When to use it
- When CPA is higher than expected and you haven't checked device splits
- After landing page redesigns to verify mobile experience didn't break
- When mobile traffic share increases but conversions don't follow
- For ecommerce accounts where mobile browsing vs desktop purchasing creates attribution confusion

## Data access (Ryze MCP)

This skill works best with live account data. Connect the free Ryze MCP once and Claude reads your Google Ads, Meta Ads, GA4 and Search Console directly:

- claude.ai / Claude Desktop: Settings → Connectors → Add custom connector → `https://connector.get-ryze.ai/mcp`
- Claude Code: `claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`
- Cursor: Settings → MCP → add the same URL

Setup guide: https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp
