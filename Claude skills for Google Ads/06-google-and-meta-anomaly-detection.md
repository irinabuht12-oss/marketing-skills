---
name: anomaly-detection
description: Catches unusual performance changes across your accounts — CPC spikes, CVR drops, spend surges, impression collapses, CTR shifts — and flags them with context about what likely changed. The goal is to catch problems in hours instead of discovering them days later during a routine check.
metadata:
  platform: Google and Meta
---

# 6/ Anomaly Detection — Google + Meta

## What it does
Catches unusual performance changes across your accounts — CPC spikes, CVR drops, spend surges, impression collapses, CTR shifts — and flags them with context about what likely changed. The goal is to catch problems in hours instead of discovering them days later during a routine check.

## How it works
Claude compares current performance against your recent baseline (typically 7-14 day rolling average) and flags any metric that moves beyond a threshold you set. It then cross-references the anomaly against common causes — budget changes, auction shifts, ad disapprovals, audience exhaustion, landing page issues, or external events.

## Practical example
Thursday at 2pm, your branded search CPC jumps 47% compared to the 14-day average. Claude flags it and identifies that a competitor started bidding on your brand terms (impression share dropped from 94% to 71% simultaneously). It also catches that a Meta campaign's CVR dropped 60% — the landing page started returning 404 errors after a site deployment at 1:30pm.

## What you get back
- List of anomalies ranked by financial impact (estimated wasted or lost spend)
- Each anomaly paired with the most likely cause based on correlated data shifts
- Recommended immediate actions for each issue
- Severity rating so you know what to fix now vs what can wait
- Baseline comparison data so you can see exactly how far off normal the metric is

## When to use it
- Daily monitoring across all active accounts
- After website deployments or landing page changes
- During high-spend periods like Black Friday or product launches
- When managing multiple accounts and you can't manually check everything daily
