---
name: channel-mix-optimizer
description: Given your total budget, recommends the optimal split across Google Search, PMax, Meta prospecting, Meta retargeting, and any other active channels based on your last 60-90 days of marginal ROAS and CPA by channel. Tells you where each additional dollar produces the best return.
metadata:
  platform: Google and Meta
---

# 15/ Channel Mix Optimizer — Google + Meta

## What it does
Given your total budget, recommends the optimal split across Google Search, PMax, Meta prospecting, Meta retargeting, and any other active channels based on your last 60-90 days of marginal ROAS and CPA by channel. Tells you where each additional dollar produces the best return.

## How it works
Claude calculates marginal efficiency for each channel — not average ROAS (which hides diminishing returns), but what your last dollar spent in each channel actually returned. It builds an efficiency curve per channel and recommends the allocation that maximizes total conversions or revenue within your budget constraint.

## Practical example
You're spending $80K/month split evenly across 4 channels: Google Search ($20K), PMax ($20K), Meta prospecting ($20K), Meta retargeting ($20K). Claude's analysis shows Google Search still has headroom with marginal CPA at $34, Meta retargeting is maxed out with marginal CPA at $72 (the audience pool is exhausted), and PMax has middling marginal returns. Recommended reallocation: Google Search $32K, PMax $18K, Meta prospecting $22K, Meta retargeting $8K. Projected result: 23% more conversions at the same total spend.

## What you get back
- Current allocation vs recommended allocation with dollar amounts
- Marginal CPA and ROAS for each channel at current and proposed spend levels
- Projected total conversion and revenue impact of the reallocation
- Diminishing returns curve for each channel showing where efficiency drops off
- Sensitivity analysis showing how the recommendation changes if budget increases or decreases by 20%

## When to use it
- Monthly or quarterly budget allocation reviews
- When total budget changes and you need to redistribute
- When a new channel is added and you need to figure out how much to shift from existing channels
- During planning season when building annual media plans with projected outcomes
