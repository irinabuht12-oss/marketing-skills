# ROAS & CPA Threshold Alert

## Purpose
Alert me when campaigns fall below my profitability targets.

## My Targets

### Google Ads
- Target CPA: $30
- Alert if CPA goes above: $45 (1.5x target)
- Critical if CPA goes above: $60 (2x target)

### Meta Ads
- Target ROAS: 3.0x
- Alert if ROAS drops below: 2.0x
- Critical if ROAS drops below: 1.5x

(Adjust these numbers to your business)

## When to Run
Every 4 hours

## What to Check

Look at last 3 days performance for each campaign:
- Current CPA or ROAS
- Compare to targets
- Check if trending worse

## Alert Levels

### 🟡 Warning (Needs Attention)
- CPA 1.5x above target OR
- ROAS below 2.0x
- Has spent at least $100 in period

### 🔴 Critical (Losing Money)
- CPA 2x above target OR
- ROAS below 1.5x
- Has spent at least $100 in period

## Message Format

```
🔴 CRITICAL: Campaigns Losing Money

GOOGLE ADS:
[Campaign Name]
• CPA: $72 (target: $30) ⚠️ 2.4x over
• Spend (3 days): $XXX
• Conversions: X
• Action: Pause or fix NOW

META ADS:
[Campaign Name]
• ROAS: 1.2x (target: 3.0x) ⚠️ 60% below
• Spend (3 days): $XXX
• Revenue: $XXX
• Action: Pause or fix NOW

💸 Estimated loss: $XXX

Reply "pause [campaign name]" to stop bleeding
Reply "details [campaign name]" for breakdown
```

```
🟡 WARNING: Campaigns Underperforming

[Campaign Name]
• CPA: $48 (target: $30)
• Trending: Getting worse ↗️
• Watch for: 24 more hours

[Campaign Name]
• ROAS: 1.9x (target: 3.0x)
• Trending: Stable →
• Watch for: 24 more hours

No action needed yet. Monitoring.
```

## If I Say "Pause [Campaign]"
- Pause that campaign
- Confirm: "Paused [Campaign]. Was spending $XX/day."

## If I Say "Details [Campaign]"
- Show breakdown by ad group, audience, or placement
- Show what's dragging performance down

## If Everything is On Target
Don't message me.
