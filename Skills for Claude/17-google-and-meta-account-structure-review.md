---
name: account-structure-review
description: Evaluates your campaign and ad set structure against your actual goals and budget. Flags over-segmentation that fragments your data, under-segmentation that hides performance differences, budget allocation issues, and consolidation opportunities that would improve algorithmic delivery and your ability to optimize.
metadata:
  platform: Google and Meta
---

# 17/ Account Structure Review — Google + Meta

## What it does
Evaluates your campaign and ad set structure against your actual goals and budget. Flags over-segmentation that fragments your data, under-segmentation that hides performance differences, budget allocation issues, and consolidation opportunities that would improve algorithmic delivery and your ability to optimize.

## How it works
Claude maps your entire account structure — campaigns, ad sets/ad groups, targeting, budgets, and bid strategies — and evaluates it against best practices for your specific situation. It considers conversion volume per campaign (enough for algorithms to learn), budget distribution (too many campaigns splitting too little budget), targeting overlap, and whether your structure supports clean testing and reporting.

## Practical example
Your Google Ads account has 34 search campaigns. Claude finds that 19 of them have fewer than 10 conversions per month — not enough for automated bidding to work. Twelve campaigns have daily budgets under $15, meaning they run out by noon. Three campaigns target nearly identical keyword sets in different geographies but could be consolidated with geo bid adjustments. Recommendation: consolidate down to 14 campaigns, which would give each campaign 25+ monthly conversions and $40+ daily budgets while maintaining clean reporting segments.

## What you get back
- Full account structure map with performance metrics at each level
- Campaigns flagged for insufficient conversion volume, budget fragmentation, or targeting overlap
- Specific consolidation recommendations with projected performance impact
- Recommended structure with campaign/ad group grouping logic explained
- Migration plan showing how to consolidate without losing historical data or disrupting active campaigns

## When to use it
- When inheriting a new account from a previous team or agency
- Quarterly account health checks
- When performance plateaus and structural issues might be holding back algorithms
- Before scaling, because a messy structure at $20K/month becomes a disaster at $100K/month
