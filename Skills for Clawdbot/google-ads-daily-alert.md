# Google Ads Daily Alert

## Purpose
Send me a daily summary of my Google Ads performance on Telegram/WhatsApp every morning.

## When to Run
Every day at 8:00 AM

## What to Do

1. Connect to Google Ads account
2. Pull yesterday's performance data:
   - Total spend
   - Total clicks
   - Total conversions
   - Cost per conversion
   - Top 3 performing campaigns by conversions
   - Worst 3 campaigns by cost per conversion

3. Format the message like this:

```
☀️ Good morning! Here's your ads update:

💰 Spent: $XXX
👆 Clicks: XXX
🎯 Conversions: XX
📊 Cost/Conv: $XX.XX

🏆 Winners:
1. [Campaign Name] — XX conversions at $XX
2. [Campaign Name] — XX conversions at $XX
3. [Campaign Name] — XX conversions at $XX

⚠️ Needs attention:
1. [Campaign Name] — $XXX spent, X conversions
2. [Campaign Name] — $XXX spent, X conversions
3. [Campaign Name] — $XXX spent, X conversions
```

4. Send to me via Telegram

## If Something Goes Wrong
- If API connection fails, tell me "Couldn't connect to Google Ads — check API key"
- If no data, tell me "No spend yesterday"
