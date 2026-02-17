---
name: account-health-audit
description: Full account health check for Google Ads and Meta Ads, flags anomalies, finds hidden losers and winners, prioritizes actions
metadata: {"clawdbot": {"emoji": "🔍"}}
---

# Performance Auditor

Run a full health check on Google Ads or Meta Ads accounts. Find what's broken, what's quietly wasting money, and what's working but underfunded.

## When To Activate

When the user asks about:
- Account health or performance overview
- "What's going wrong" or "what should I fix"
- Weekly or monthly performance reviews
- Taking over a new account
- "Something feels off" with their ads
- General audit requests

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Platform (Google Ads / Meta Ads / both)
- Target CPA or target ROAS
- Monthly budget
- Time period to analyze (default to last 14 days)
- Any known issues or recent changes

### Step 2: Pull Data via MCP

Pull campaign-level data:
- Campaign name, status, objective
- Spend, impressions, clicks, CTR
- Conversions, CPA, ROAS
- Budget, budget type (daily/lifetime)

If Meta: also pull ad set and ad level data.
If Google: also pull search term report and keyword data.

### Step 3: Account Health Score

Score the account 1-10 based on:
- % of budget going to campaigns above target CPA (weight: 30%)
- Number of active campaigns with zero conversions in period (weight: 20%)
- Budget pacing accuracy — actual vs expected spend (weight: 15%)
- Conversion trend — improving or declining week over week (weight: 15%)
- Wasted spend ratio — spend on paused/underperforming elements (weight: 20%)

### Step 4: Analysis

1. **Hidden Losers**
   - Campaigns spending steadily but CPA 1.5x+ above target
   - Campaigns with high impressions, low CTR, and no conversions
   - Show: campaign name, spend, conversions, CPA, days active

2. **Hidden Winners**
   - Campaigns with CPA well below target but limited by budget
   - Campaigns with strong efficiency but low spend allocation
   - Show: campaign name, CPA vs target, current budget, headroom estimate

3. **Anomalies**
   - Sudden CPA spikes (>30% week over week)
   - CTR drops (>20% week over week)
   - Impression volume changes (>40% week over week)
   - For each: what changed, likely cause, recommended action

4. **Attribution Check** (if backend data provided)
   - Compare platform-reported conversions vs backend/CRM
   - Flag campaigns with >25% discrepancy
   - Note which campaigns look better or worse with backend data

### Step 5: Prioritized Action List

Rank all recommendations by estimated impact (highest first):
- Immediate actions (do today)
- This week actions
- Monitor and revisit next week

## Output Format

```
ACCOUNT HEALTH SCORE: [X]/10

IMMEDIATE ACTIONS:
1. [Action] — [Campaign name] — [Why] — [Estimated impact]
2. ...

HIDDEN LOSERS (pause or fix):
| Campaign | Spend | Conv | CPA | Target CPA | Action |
| ... | ... | ... | ... | ... | ... |

HIDDEN WINNERS (scale):
| Campaign | Spend | Conv | CPA | Target CPA | Headroom |
| ... | ... | ... | ... | ... | ... |

ANOMALIES:
| Campaign | Metric | Change | Likely Cause | Action |
| ... | ... | ... | ... | ... |

THIS WEEK:
1. ...
2. ...

MONITOR:
1. ...
```

## Rules

- Use actual campaign names, never generic labels
- Every recommendation needs a specific "why"
- Include dollar amounts and percentages, not vague language
- If data is insufficient for a section, say so and say what data is needed
- Don't recommend changes during learning periods unless something is clearly broken
- Flag if account has fewer than 30 conversions in period — recommendations will be less reliable
