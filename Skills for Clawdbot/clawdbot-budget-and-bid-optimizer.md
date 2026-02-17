---
name: budget-and-bid-optimizer
description: Analyze spend efficiency, recommend bid adjustments and budget reallocations for Google Ads and Meta Ads
metadata: {"clawdbot": {"emoji": "💰"}}
---

# Bid & Budget Manager

Find wasted spend, recommend budget reallocations, and suggest bid adjustments with specific numbers.

## When To Activate

When the user asks about:
- Budget allocation or reallocation
- Bid adjustments or bid strategy changes
- Wasted spend or inefficient spending
- Scaling campaigns up or down
- "Where should I put my money"
- Budget pacing issues

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Platform (Google Ads / Meta Ads / both)
- Target CPA or target ROAS
- Total monthly budget
- Time period of data (default: last 14 days)
- Any constraints (minimum spend on brand, max on prospecting, etc.)

### Step 2: Pull Data via MCP

Campaign-level data:
- Campaign name, status, objective, bid strategy
- Daily budget, total spend in period
- Impressions, clicks, CTR, CPC
- Conversions, CPA, ROAS, conversion rate

If Google: also pull keyword-level CPC data.
If Meta: also pull ad set-level budgets.

### Step 3: Efficiency Analysis

Rank all active campaigns by efficiency:

**Efficiency Score** = (Target CPA / Actual CPA) × 100
- Score > 100 = beating target
- Score 80-100 = acceptable range
- Score 50-80 = underperforming
- Score < 50 = critical, likely pause

Show as table:
| Campaign | Spend | Conv | CPA | Target | Efficiency Score | Verdict |

### Step 4: Budget Reallocation

Calculate optimal budget distribution:

1. Identify campaigns to **cut** (efficiency < 50, or zero conversions with >$200 spend)
2. Identify campaigns to **scale** (efficiency > 120, not budget-capped, or budget-limited with strong efficiency)
3. Calculate exact dollar amounts to move
4. Show before/after budget table

```
BUDGET REALLOCATION:
| Campaign | Current Daily | Recommended Daily | Change | Why |
| ... | $50 | $0 (pause) | -$50 | CPA $127 vs $50 target |
| ... | $100 | $150 | +$50 | CPA $28, budget-limited |
```

### Step 5: Bid Recommendations

For each campaign, evaluate bid strategy fitness:

**Google Ads:**
- Manual CPC → recommend if <15 conversions/month
- Maximize Conversions → recommend if 15-50 conversions/month
- Target CPA → recommend if >50 conversions/month, set at current CPA + 10%
- Target ROAS → recommend if >50 conversions/month and revenue tracking is accurate

**Meta Ads:**
- Lowest Cost → recommend for testing or low-data campaigns
- Cost Cap → recommend if CPA consistency matters, set at target CPA + 15%
- Bid Cap → recommend for strict CPA control, set at target CPA
- ROAS Goal → recommend if >50 purchases/month

For each change:
- Current strategy
- Recommended strategy
- Why
- Expected short-term impact (learning period = 3-7 days of potential CPA increase)

### Step 6: Pause List

Campaigns to pause immediately:
| Campaign | Spend (period) | Conversions | CPA | Wasted Spend Estimate |

**Wasted spend** = total spend minus (conversions × target CPA). If negative, entire spend is waste.

### Step 7: Pacing Check

For each campaign:
- Expected spend at this point in the month
- Actual spend
- Pace: on track / underspending / overspending
- If off pace: why and what to do

## Output Format

Return in this order:
1. Efficiency ranking table (all campaigns)
2. Pause list with wasted spend totals
3. Budget reallocation table with exact amounts
4. Bid strategy recommendations with reasoning
5. Pacing alerts

## Rules

- Always show exact dollar amounts, never "increase budget"
- Round to nearest $5 for daily budgets
- Don't recommend scaling campaigns with fewer than 10 conversions in period
- Don't recommend Target CPA/ROAS if campaign has <50 conversions in 30 days
- Flag if total recommended budget exceeds user's stated monthly budget
- If cutting one campaign, always suggest where that budget goes
- Account for learning periods in impact estimates
