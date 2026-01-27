# Budget Pacing Alert

## Purpose
Alert me immediately if spending is way off track — too fast or too slow.

## My Budget Settings
- Monthly budget: $5,000
- Daily target: ~$165

## When to Run
Every 4 hours during the day (8am, 12pm, 4pm, 8pm)

## Alert Rules

### 🔴 Overspending Alert
Alert me if:
- Daily spend is 50% higher than target by noon
- Daily spend is 30% higher than target by 4pm
- On pace to exceed monthly budget by more than 10%

### 🟡 Underspending Alert
Alert me if:
- Daily spend is 50% below target by 4pm
- On pace to underspend monthly budget by more than 20%

### ⚫ Zero Spend Alert
Alert me immediately if:
- Any campaign has $0 spend for 6+ hours (during business hours)
- Could mean: payment issue, campaign paused, disapproved ads

## Message Format

```
🔴 OVERSPEND ALERT

Today's spend: $XXX (target: $165)
You're XX% over pace.

At this rate, monthly spend = $X,XXX (budget: $5,000)

Top spending campaigns:
1. [Name] — $XX today
2. [Name] — $XX today

Action needed? Reply "pause [campaign]" or "reduce [campaign] budget to $X"
```

```
🟡 UNDERSPEND ALERT

Today's spend: $XX (target: $165)
You're XX% under pace.

Possible causes:
- Low search volume
- Budget caps hit
- Ads not showing

Want me to investigate? Reply "diagnose"
```

```
⚫ ZERO SPEND WARNING

[Campaign Name] has spent $0 in the last 6 hours.

This might mean:
- Payment failed
- Campaign accidentally paused
- Ads disapproved

Want me to check? Reply "check [campaign]"
```

## If Everything is Normal
Don't message me. Only alert when something is wrong.
