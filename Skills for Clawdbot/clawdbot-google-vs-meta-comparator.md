---
name: google-vs-meta-comparator
description: Compare Google Ads vs Meta Ads performance side by side, identify where to shift budget between platforms
metadata: {"clawdbot": {"emoji": "⚖️"}}
---

# Cross-Platform Comparator

Compare Google Ads and Meta Ads performance side by side. Figure out which platform is earning its budget and where to shift spend.

## When To Activate

When the user asks about:
- Comparing Google vs Meta performance
- "Where should I spend more"
- "Which platform is working better"
- Cross-channel budget allocation
- Platform-level strategy decisions
- "Should I shift budget from Google to Meta" or vice versa

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Total monthly budget across both platforms
- Current split (how much on Google vs Meta)
- Target CPA or ROAS (same target or different per platform)
- Time period (default: last 30 days for meaningful comparison)
- Business model (ecommerce, lead gen, SaaS, app)
- Are the campaigns targeting the same product/offer

### Step 2: Pull Data via MCP

Pull from both platforms for the same time period:

**Google Ads:**
- Total spend, conversions, CPA, ROAS
- By campaign type: Search, Shopping, Performance Max, Display, YouTube
- Impression share (search campaigns)
- Top converting campaigns

**Meta Ads:**
- Total spend, conversions, CPA, ROAS
- By objective: Conversions, Leads, Traffic
- Frequency and reach
- Top converting campaigns

### Step 3: Platform-Level Comparison

| Metric | Google Ads | Meta Ads | Winner |
|--------|-----------|----------|--------|
| Total Spend | | | |
| Conversions | | | |
| CPA | | | |
| ROAS | | | |
| CVR | | | |
| CTR | | | |
| CPM | | | |
| CPC | | | |
| Cost per 1K Reach | | | |

### Step 4: Efficiency Analysis

**Marginal CPA analysis:**
- For each platform, what's the CPA of the last 20% of spend
- This shows whether the platform is still efficient at the edges or only efficient in the core
- Platform with lower marginal CPA has more room to scale

**Example output:**
```
Google Ads:
- Core CPA (first 80% of spend): $38
- Marginal CPA (last 20% of spend): $67
- Marginal efficiency is declining — platform is near capacity

Meta Ads:
- Core CPA (first 80% of spend): $42
- Marginal CPA (last 20% of spend): $48
- Marginal efficiency is holding — room to scale
```

### Step 5: Campaign Type Breakdown

**Google Ads breakdown:**
| Type | Spend | Conv | CPA | % of Total |
| Search - Brand | | | | |
| Search - Non-Brand | | | | |
| Shopping/PMax | | | | |
| Display | | | | |
| YouTube | | | | |

**Meta Ads breakdown:**
| Type | Spend | Conv | CPA | % of Total |
| Prospecting | | | | |
| Retargeting | | | | |
| Broad | | | | |
| Lookalike | | | | |

### Step 6: Budget Shift Recommendation

Based on efficiency and marginal CPA:

**Scenario A: Current split**
- Google: $X (Y%), Meta: $X (Y%)
- Blended CPA: $X
- Total conversions: X

**Scenario B: Recommended split**
- Google: $X (Y%), Meta: $X (Y%)
- Projected blended CPA: $X
- Projected total conversions: X
- Net change: +/- X conversions at +/- $X CPA

Show exact dollar amounts to move and from which campaigns.

### Step 7: Platform-Specific Recommendations

**Google Ads:**
- Opportunities (impression share gaps, new campaign types to test)
- Cuts (underperforming campaign types)

**Meta Ads:**
- Opportunities (audience expansion, creative tests, new placements)
- Cuts (saturated audiences, fatigued creatives)

## Output Format

```
PLATFORM COMPARISON ([period]):

| Metric | Google | Meta | Winner |
(full comparison table)

EFFICIENCY:
Google core CPA: $X | Marginal CPA: $X
Meta core CPA: $X | Marginal CPA: $X
Scaling headroom: [Google/Meta]

BUDGET RECOMMENDATION:
Current: Google $X (Y%) | Meta $X (Y%)
Recommended: Google $X (Y%) | Meta $X (Y%)
Expected impact: [+/- conversions] at [+/- CPA]

SHIFT DETAILS:
- Move $X from [specific Google campaign] to [specific Meta campaign]
- Reason: [why]

GOOGLE OPPORTUNITIES:
1. ...

META OPPORTUNITIES:
1. ...
```

## Rules

- Only compare when both platforms are running the same offer/product to the same market
- If one platform has <7 days of data, flag that comparison is premature
- Don't compare brand search CPA to Meta prospecting CPA — they're different funnel stages
- When recommending shifts, suggest incremental moves (10-20% at a time), not dramatic swings
- Note attribution differences: Google last-click vs Meta view-through can inflate/deflate numbers
- If user has backend/CRM data, use that as source of truth over platform-reported conversions
- Always caveat that shifting budget takes 7-14 days to stabilize — don't judge results in week 1
- If both platforms are performing well, say so — not every comparison needs a shift
