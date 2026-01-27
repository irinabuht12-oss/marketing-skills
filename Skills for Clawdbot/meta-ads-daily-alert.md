# Meta Ads Daily Alert

## Purpose
Send me a daily summary of my Meta (Facebook/Instagram) ads performance.

## When to Run
Every day at 8:30 AM

## What to Do

1. Connect to Meta Ads account
2. Pull yesterday's performance:
   - Total spend
   - Impressions
   - Link clicks
   - Purchases (or leads)
   - Cost per purchase/lead
   - ROAS (if e-commerce)

3. Break down by:
   - Top 3 ad sets by results
   - Top 3 ads by results
   - Worst 3 ads by cost per result

## Message Format

```
📘 Meta Ads Update — Yesterday

💰 Spend: $XXX
👀 Impressions: XX,XXX
👆 Clicks: XXX
🎯 Purchases: XX
📊 Cost per purchase: $XX.XX
💵 ROAS: X.Xx

🏆 Best Performers:
1. [Ad Set/Ad Name] — XX purchases at $XX
2. [Ad Set/Ad Name] — XX purchases at $XX
3. [Ad Set/Ad Name] — XX purchases at $XX

⚠️ Underperformers:
1. [Ad Name] — $XXX spent, X purchases
2. [Ad Name] — $XXX spent, X purchases
3. [Ad Name] — $XXX spent, X purchases

💡 [One quick insight or suggestion]
```

## If Something Goes Wrong
- API error → "Couldn't pull Meta data — check connection"
- No spend → "No Meta spend yesterday"
