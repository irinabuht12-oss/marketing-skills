---
name: retargeting-window-analysis
description: Analyzes your conversion lag data to determine the optimal retargeting window for each audience segment. Tells you whether your 30-day retargeting window should actually be 7 days, 14 days, or 60 days based on when people actually convert after their first visit.
platform: Meta
---

# 22/ Retargeting Window Analysis — Meta

## What it does
Analyzes your conversion lag data to determine the optimal retargeting window for each audience segment. Tells you whether your 30-day retargeting window should actually be 7 days, 14 days, or 60 days based on when people actually convert after their first visit.

## How it works
Claude looks at time-to-conversion data across your retargeting audiences — how many days between first site visit and conversion. It segments this by traffic source, product category, and audience type to find the window where most conversions happen and where retargeting spend stops producing returns.

## Practical example
Your default retargeting window is 30 days for all audiences. Claude's analysis shows that 78% of conversions from Meta prospecting traffic happen within 7 days, and only 4% happen after day 14. But for Google Search traffic, conversions are spread more evenly with 35% happening between days 14-30. Claude recommends splitting your retargeting: a 7-day high-bid window for Meta traffic (where urgency is highest), a 14-day standard window for search traffic, and cutting the 14-30 day window for Meta-sourced visitors entirely — saving $1,900/month in retargeting spend on users who weren't going to convert.

## What you get back
- Conversion lag distribution by traffic source and audience segment
- Optimal retargeting window for each segment with confidence levels
- Current spend in each window period with conversion contribution
- Recommended window adjustments with projected savings
- Bid adjustment recommendations by recency (higher bids for recent visitors, lower for older)

## When to use it
- When setting up retargeting campaigns for new accounts
- When retargeting CPA is creeping up and audience pools need tightening
- After significant changes in conversion funnel or product offering
- Quarterly to check if conversion behavior patterns have shifted
