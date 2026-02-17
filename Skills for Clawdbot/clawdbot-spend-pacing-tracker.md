---
name: spend-pacing-tracker
description: Monitor daily and monthly budget pacing across Google Ads and Meta Ads, catch over and under delivery before it becomes a problem
metadata: {"clawdbot": {"emoji": "⏱️"}}
---

# Pacing Monitor

Catch pacing issues early. Flag campaigns that are overspending, underspending, or won't hit their monthly targets.

## When To Activate

When the user asks about:
- Budget pacing or delivery
- "Am I on track this month"
- Over or under delivery
- "Why did I spend so much yesterday"
- "Will I hit my budget this month"
- Mid-month budget check-ins
- Any mention of spend being higher or lower than expected

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Platform (Google Ads / Meta Ads / both)
- Monthly budget (total and per campaign if applicable)
- Current date / day of month
- Any planned spend changes (upcoming promos, blackout dates)
- Flight dates if not calendar month

### Step 2: Pull Data via MCP

For each campaign:
- Campaign name, status, daily budget
- Total spend this month (MTD)
- Daily spend for last 7 days
- Remaining days in month/flight

### Step 3: Pacing Calculation

For each campaign:

**Expected spend** = (monthly budget / days in month) × days elapsed
**Actual spend** = MTD spend
**Pacing %** = (actual spend / expected spend) × 100
**Projected end-of-month spend** = (MTD spend / days elapsed) × days in month

Pacing status:
- **On pace** — 90-110% of expected
- **Underspending** — <90% of expected
- **Overspending** — >110% of expected
- **Critical underspend** — <70% of expected
- **Critical overspend** — >130% of expected

### Step 4: Daily Spend Variance

Check last 7 days of daily spend per campaign:
- Average daily spend
- Standard deviation
- Any single day with spend >2x or <0.5x average
- Day-over-day trend (accelerating or decelerating)

Flag specific days with unusual spend and likely causes:
- Overspend on a specific day → audience expansion, auction shift, bid strategy adjustment
- Underspend on a specific day → ad disapprovals, budget exhaustion, low search volume

### Step 5: Projected Outcomes

For each campaign:
| Campaign | Monthly Budget | MTD Spend | Projected EOM | Variance | Status |

For the account overall:
- Total monthly budget
- Total MTD spend
- Projected total EOM spend
- Over/under by how much

### Step 6: Fix Recommendations

**For underspending campaigns:**
- Check if ads are active and approved
- Check if bid is competitive (impression share data on Google)
- Check if audience is too narrow
- Recommend: increase daily budget by X%, broaden targeting, or increase bids by X%

**For overspending campaigns:**
- Check if daily budget was recently changed
- Check if bid strategy is uncapped
- Check if a spike day skewed the pace
- Recommend: reduce daily budget to $X/day to finish month on target, or add a cost cap

**Exact daily budget to finish on target:**
Remaining budget = monthly budget - MTD spend
Required daily = remaining budget / remaining days
Show this for every off-pace campaign.

### Step 7: Alerts Summary

Priority-sorted list:
1. Critical issues (will miss budget by >20%)
2. Warning issues (will miss budget by 10-20%)
3. Watch items (slightly off but self-correcting)

## Output Format

```
PACING SUMMARY (Day [X] of [Y]):

| Campaign | Budget | MTD Spend | Expected | Pacing % | Projected EOM | Status |

ACCOUNT TOTAL:
Budget: $X | MTD: $X | Projected: $X | Variance: +/- $X

CRITICAL:
1. [Campaign] — overspending by $X, will exceed budget by $X
   → Reduce daily budget to $X/day for rest of month

WARNINGS:
1. [Campaign] — underspending, projected to leave $X unspent
   → Check ad approvals, increase bid by X%

DAILY SPEND ANOMALIES:
| Campaign | Date | Daily Spend | Avg Daily | Variance | Likely Cause |
```

## Rules

- Always calculate based on calendar days remaining, not business days
- Account for weekends — some industries see lower weekend spend, don't flag that as underspend
- If it's before day 5 of the month, note that pacing projections are less reliable
- If campaign launched mid-month, adjust expected spend calculation to actual active days
- Don't recommend budget changes for campaigns in learning period
- Show exact dollar amounts for recommended daily budgets, rounded to nearest $5
- If user mentions a promo or event, factor that into projections (heavier spend expected around those dates)
