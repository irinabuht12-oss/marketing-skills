---
name: ab-test-setup-and-analysis
description: Designs statistically valid split tests for ads, audiences, landing pages, or bid strategies. Calculates required sample sizes before you start, monitors results during the test, and calls winners when statistical significance is actually reached — not when you feel like one is winning.
metadata:
  platform: Google and Meta
---

# 28/ A/B Test Setup and Analysis — Google + Meta

## What it does
Designs statistically valid split tests for ads, audiences, landing pages, or bid strategies. Calculates required sample sizes before you start, monitors results during the test, and calls winners when statistical significance is actually reached — not when you feel like one is winning.

## How it works
Claude takes your test hypothesis, current baseline metrics, and the minimum detectable effect you care about, then calculates how much traffic and time the test needs to produce a reliable result. During the test, it tracks results and tells you whether differences are statistically significant or just noise. It prevents premature test calls that waste the effort.

## Practical example
You want to test a new headline variant against your current best performer. Your current ad gets a 2.8% CTR with 1,200 daily impressions. Claude calculates that to detect a 15% improvement (3.22% CTR) with 95% confidence, you need approximately 12,400 impressions per variant — about 10 days at current traffic levels. After 7 days, the new variant shows 3.1% CTR vs 2.7% for control. Claude tells you it's trending positive but not yet significant (p=0.14, need p<0.05) — keep running for 4 more days before making a call.

## What you get back
- Test design with clear hypothesis, control, variant, and success metric
- Required sample size and estimated test duration before you start
- Daily monitoring with current results, confidence level, and days remaining
- Winner call only when significance is reached, with effect size and confidence interval
- Post-test recommendations: roll out winner, iterate further, or test something else

## When to use it
- Before launching any creative, audience, or landing page test
- When someone on the team wants to call a winner after 2 days of data
- For structured testing programs where you need a pipeline of tests running sequentially
- When clients ask "is this result real or just noise" and you need a definitive answer
