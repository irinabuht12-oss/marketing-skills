---
name: campaign-naming-convention-builder
description: Builds a consistent, filterable naming convention across your Google and Meta accounts based on your campaign types, objectives, targeting, and reporting needs. Makes filtering, reporting, and cross-platform analysis actually work instead of guessing what "Campaign_v3_Final_NEW" means. Platform: Google and Meta.
metadata:
  platform: Google and Meta
---

# 23/ Campaign Naming Convention Builder — Google + Meta

## What it does
Builds a consistent, filterable naming convention across your Google and Meta accounts based on your campaign types, objectives, targeting, and reporting needs. Makes filtering, reporting, and cross-platform analysis actually work instead of guessing what "Campaign_v3_Final_NEW" means.

## How it works
Claude looks at your current account structure, campaign types, targeting approaches, and reporting requirements, then designs a naming taxonomy that encodes the key attributes you need to slice data by. It covers campaigns, ad sets/ad groups, and ads — all with a consistent format that works across platforms and with your reporting tools.

## Practical example
Your current naming is a mix of "Spring Sale - Lookalike" and "FB_Prospecting_Interest_test2_FINAL". Claude designs a convention: [Platform]_[Objective]_[Funnel Stage]_[Targeting Type]_[Audience/Keyword Theme]_[Geo]_[Date]. So "META_CONV_PROSP_LAL_1pct-Purchasers_US_2024Q2" tells you everything at a glance. It also generates a reference sheet, naming rules for new campaigns, and a script to bulk-rename existing campaigns to the new format.

## What you get back
- Naming convention format with each component explained
- Full taxonomy of values for each component (all targeting types, objectives, funnel stages you use)
- Reference sheet for anyone on the team to follow
- Bulk rename list mapping current names to new convention
- Recommendations for UTM parameter alignment so your naming convention matches analytics tracking

## When to use it
- When onboarding a new team member who needs to navigate the account
- When taking over messy accounts and need to bring order before optimizing
- Before scaling to multiple markets or products where naming discipline becomes critical
- When building cross-platform reporting dashboards that need consistent naming to aggregate data correctly

## Data access (Ryze MCP)

This skill works best with live account data. Connect the free Ryze MCP once and Claude reads your Google Ads, Meta Ads, GA4 and Search Console directly:

- claude.ai / Claude Desktop: Settings → Connectors → Add custom connector → `https://connector.get-ryze.ai/mcp`
- Claude Code: `claude mcp add ryze --transport http https://connector.get-ryze.ai/mcp`
- Cursor: Settings → MCP → add the same URL

Setup guide: https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp
