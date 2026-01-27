# Ad Creative Test Monitor

## Purpose
Track A/B tests on ad creatives and tell me when we have a clear winner.

## When to Run
Every day at 2:00 PM

## How to Identify Tests
Ads in the same ad group (Google) or ad set (Meta) are being tested against each other.

## Rules for Declaring a Winner

A creative wins when:
1. At least 100 clicks each (statistical significance)
2. Winner has 20%+ better conversion rate
3. Test has run for at least 7 days

## What to Do

### Step 1: Find Active Tests
Look for ad groups/ad sets with 2+ active ads

### Step 2: Check if Winner Exists
Apply the rules above

### Step 3: Alert Me

```
🧪 Creative Test Results

✅ WINNER FOUND:

Ad Set: [Name]
Test duration: X days

🏆 Winner: [Ad Name]
• Clicks: XXX
• Conversions: XX
• Conv Rate: X.X%
• CPA: $XX

❌ Loser: [Ad Name]
• Clicks: XXX
• Conversions: XX
• Conv Rate: X.X%
• CPA: $XX

Difference: Winner converts XX% better

📌 Recommendation: Pause loser, scale winner

Want me to pause the loser? Reply "pause loser"
```

### Tests Still Running

```
⏳ TESTS IN PROGRESS:

Ad Set: [Name]
• [Ad A]: XXX clicks, X.X% conv rate
• [Ad B]: XXX clicks, X.X% conv rate
• Need ~XX more clicks for significance
• Estimated: X more days
```

## If No Active Tests
Don't message me.

## If I Say "Pause Loser"
- Pause the losing ad
- Confirm: "Done. [Ad Name] paused."
