# Auto-Pause Underperforming Ads

## Purpose
Automatically pause ads that are wasting money and alert me.

## When to Run
Every 6 hours

## Rules for Pausing

Pause an ad if ANY of these are true:

1. **High spend, no results**
   - Spent more than $50 AND zero conversions

2. **Terrible CTR**
   - More than 1,000 impressions AND CTR below 0.5%

3. **Cost per conversion too high**
   - Cost per conversion is 3x higher than account average

## What to Do

1. Check all enabled ads in the account
2. Apply the rules above
3. Pause any ad that matches
4. Send me a message:

```
🛑 Paused [X] ads

[Ad Name] — Campaign: [Name]
Reason: Spent $XX with 0 conversions

[Ad Name] — Campaign: [Name]  
Reason: CTR 0.3% (below 0.5% threshold)

[Ad Name] — Campaign: [Name]
Reason: CPA $85 (account avg: $25)

💡 Review these in Google Ads if needed.
```

## If Nothing to Pause
Don't message me. Stay quiet.

## Safety Rules
- Never pause more than 5 ads at once
- If more than 5 qualify, pause top 5 worst performers and tell me "X more ads need review"
- Never pause ads in campaigns with "Brand" in the name
