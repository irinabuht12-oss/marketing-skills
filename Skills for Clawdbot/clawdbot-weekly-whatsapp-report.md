---
name: weekly-whatsapp-report
description: Generate a concise weekly performance report for Google Ads and Meta Ads, formatted for WhatsApp or Slack delivery
metadata: {"clawdbot": {"emoji": "📊"}}
---

# Weekly Report Generator

Pull data from ad accounts, generate a concise weekly summary, and send it via WhatsApp, Slack, or Telegram. Built for Monday morning delivery.

## When To Activate

When the user asks about:
- Weekly report or summary
- "How did last week go"
- "Send me a report every Monday"
- Performance summary for a specific week
- Client reporting
- Any scheduled/cron-based report request

Also activate automatically if set up as a cron job (recommended: Monday 8am).

## What To Do

### Step 1: Determine Scope

If not provided, ask:
- Platform(s) to include (Google Ads / Meta Ads / both)
- Report period (default: last 7 days, Monday to Sunday)
- Compare to: previous week, same week last month, or both
- Target CPA or ROAS
- Delivery channel (WhatsApp, Slack, Telegram, or file)
- Include which accounts (if managing multiple)

### Step 2: Pull Data via MCP

**Account-level (both platforms):**
- Total spend, impressions, clicks, CTR
- Conversions, CPA, ROAS
- Week-over-week change for each metric

**Campaign-level (top 5 by spend per platform):**
- Campaign name, spend, conversions, CPA
- WoW change in CPA

**If Meta:** Also pull frequency and reach.
**If Google:** Also pull impression share and search impression share.

### Step 3: Executive Summary

Write a 3-4 sentence summary a busy person can read in 10 seconds:
- Overall performance vs target
- Biggest win
- Biggest concern
- One recommended action

Example:
"Spent $12,400 across Google and Meta last week, 247 conversions at $50 CPA (target: $55). Google non-brand drove 40% of conversions at $42 CPA — best performing segment. Meta prospecting CPA crept up to $68, driven by audience fatigue on LAL 1%. Recommend refreshing Meta prospecting creatives this week."

### Step 4: Key Metrics Table

```
WEEKLY PERFORMANCE ([date range]):

| Metric | This Week | Last Week | Change | Target | Status |
| Spend | $12,400 | $11,800 | +5.1% | $13,000 | ✓ |
| Conversions | 247 | 231 | +6.9% | 230 | ✓ |
| CPA | $50.20 | $51.08 | -1.7% | $55.00 | ✓ |
| ROAS | 3.2x | 3.0x | +6.7% | 3.0x | ✓ |
| CTR | 2.1% | 2.0% | +5.0% | — | — |
| CPM | $14.20 | $13.80 | +2.9% | — | — |
```

Status: ✓ = on/above target, ⚠ = within 10% of target, ✗ = below target

### Step 5: Platform Breakdown

**Google Ads:**
| Campaign | Spend | Conv | CPA | WoW CPA Change |
(Top 5 by spend)

**Meta Ads:**
| Campaign | Spend | Conv | CPA | WoW CPA Change |
(Top 5 by spend)

### Step 6: Wins and Concerns

**Wins (things that improved):**
1. [Specific campaign/metric] — [what happened] — [impact]
2. ...

**Concerns (things that declined):**
1. [Specific campaign/metric] — [what happened] — [recommended action]
2. ...

### Step 7: Top 3 Actions This Week

Prioritized list of what to do next:
1. [Action] — [why] — [expected impact]
2. [Action] — [why] — [expected impact]
3. [Action] — [why] — [expected impact]

### Step 8: Format and Deliver

**For WhatsApp/Telegram (short format):**
Condense to fit mobile screens. Use this structure:

```
📊 Weekly Ads Report
[Date Range]

Spend: $12,400 (+5.1%)
Conversions: 247 (+6.9%)
CPA: $50.20 (-1.7%) ✓
ROAS: 3.2x (+6.7%) ✓

Win: Google non-brand hit $42 CPA
Concern: Meta LAL 1% CPA up to $68

Top action: Refresh Meta prospecting creatives
```

**For Slack (medium format):**
Include executive summary + key metrics table + wins/concerns + top 3 actions.

**For file/email (full format):**
Include all sections above.

## Cron Setup

To run automatically every Monday at 8am:

The user can set this up in Clawdbot's cron/jobs system:
```json
{
  "schedule": "0 8 * * 1",
  "task": "Run weekly ads report for all accounts, send via WhatsApp"
}
```

## Output Format (Full)

```
WEEKLY ADS REPORT — [Date Range]

SUMMARY:
[3-4 sentence executive summary]

KEY METRICS:
[Metrics table with WoW changes and target status]

GOOGLE ADS:
[Top 5 campaigns table]

META ADS:
[Top 5 campaigns table]

WINS:
1. ...
2. ...

CONCERNS:
1. ...
2. ...

THIS WEEK'S ACTIONS:
1. ...
2. ...
3. ...
```

## Rules

- Keep the report scannable — a busy person should get the point in 30 seconds
- Always show week-over-week changes, not just current numbers
- Use actual campaign names, never "Campaign A"
- Only flag concerns that are actionable — don't list problems without solutions
- If a metric changed <5% WoW, don't flag it as a win or concern — that's noise
- WhatsApp format must be under 1000 characters
- Don't include vanity metrics (impressions, reach) unless they explain a CPA change
- If data shows everything is on track, say so briefly — don't manufacture concerns
- Round CPA to nearest cent, spend to nearest dollar, percentages to one decimal
