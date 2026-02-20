---
name: quality-score-breakdown
description: Breaks down Quality Score components for your Google Ads keywords — expected CTR, ad relevance, and landing page experience — and tells you exactly which component is dragging each keyword down, with specific fixes ranked by potential CPC impact.
metadata:
  platform: Google
---

# 14/ Quality Score Breakdown — Google

## What it does
Breaks down Quality Score components for your Google Ads keywords — expected CTR, ad relevance, and landing page experience — and tells you exactly which component is dragging each keyword down, with specific fixes ranked by potential CPC impact.

## How it works
Claude pulls your keyword-level Quality Score data along with historical QS trends, CTR benchmarks, ad copy relevance signals, and landing page metrics. It identifies which of the three components is below average for each keyword and cross-references with your actual ad copy and landing pages to pinpoint the exact issue.

## Practical example
You have 340 active keywords. Claude identifies 47 with Quality Score 5 or below. Of those, 28 have below-average landing page experience (mostly because 3 landing pages have slow mobile load times), 14 have below-average ad relevance (the ad groups contain too many unrelated keywords diluting relevance), and 5 have below-average expected CTR (they're in ad groups where CTR is dragged down by poor-performing ad copy variants). Fixing the 3 landing pages alone would impact 28 keywords and potentially reduce CPC by 15-25%.

## What you get back
- Every keyword with QS below 7 flagged with the specific underperforming component
- Root cause analysis for each component (not just "below average" but why)
- Prioritized fix list ranked by potential CPC savings and conversion volume impact
- Ad group restructuring recommendations where relevance is the issue
- Landing page specific issues tied back to keyword groups they affect

## When to use it
- Monthly QS audits to catch degradation early
- When CPCs rise without competitive or market explanation
- After landing page or website changes that might have affected page experience scores
- When restructuring accounts and you want to improve efficiency across the board
