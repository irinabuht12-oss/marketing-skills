---
name: audience-saturation-scanner
description: Analyze audience and targeting performance, detect saturation, flag overlap, recommend new audiences and scaling paths
metadata: {"clawdbot": {"emoji": "👥"}}
---

# Audience Architect

Find which audiences are saturated, which are efficient, where there's overlap, and what to test next.

## When To Activate

When the user asks about:
- Audience or targeting performance
- Rising CPMs or frequency
- Audience saturation
- Scaling to new audiences
- Lookalike expansion
- "My costs are going up" (often an audience issue)
- Audience overlap concerns

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Platform (Google Ads / Meta Ads / both)
- Target CPA or ROAS
- Monthly budget
- Current audience types in use (interest, lookalike, custom, broad, etc.)
- Time period (default: last 14 days)
- Are they trying to scale or optimize current spend

### Step 2: Pull Data via MCP

Ad set or audience-level data:
- Ad set name, audience description, targeting details
- Spend, impressions, reach, frequency
- CPM, CTR, CPC
- Conversions, CPA, ROAS
- Audience size (if available)

Pull current period AND previous period for trend comparison.

### Step 3: Audience Efficiency Ranking

Rank all audiences by efficiency:

| Ad Set | Audience Type | Spend | Conv | CPA | CPM | Freq | Efficiency |

Efficiency tiers:
- **Top tier** — CPA below target, frequency <3, CPM stable
- **Mid tier** — CPA near target, frequency 2-4, CPM rising slightly
- **Saturated** — CPA above target, frequency >3, CPM rising >15%
- **Dead** — CPA 2x+ target or zero conversions with meaningful spend

### Step 4: Saturation Analysis

An audience is saturated when:
- Frequency >3 AND CPM increased >15% vs previous period
- Frequency >4 (regardless of CPM trend)
- Reach has plateaued (less than 5% new reach in last 7 days)
- CTR declining while frequency rising

For each saturated audience:
| Audience | Frequency | CPM Change | Reach Trend | Days to Exhaustion | Action |

**Days to Exhaustion** estimate = (audience size - total reach) / daily reach rate

### Step 5: Overlap Check

Flag potential overlap issues:
- Multiple ad sets targeting similar interests or demographics
- Lookalikes from the same seed at different %
- Broad campaigns competing with targeted campaigns

For each overlap:
- Which audiences overlap
- Estimated overlap % (based on targeting similarities)
- Which is more efficient
- Recommendation: consolidate, exclude, or separate

### Step 6: Scaling Roadmap

Based on what's working, recommend expansion paths:

**For Meta:**
- Current LAL 1% working → test 1-3%, 3-5%
- Interest targeting working → test broader interest combos
- Custom audiences working → test similar seed sources
- Everything saturated → test broad with creative differentiation

**For Google:**
- In-market working → test affinity layers
- Custom intent working → expand keyword lists
- Remarketing working → test observation audiences
- Search working → test Performance Max

For each recommendation:
- What to test
- Expected audience size
- Budget recommendation for test
- Minimum test duration
- Success criteria

### Step 7: New Audiences to Test

Suggest 3-5 specific new audiences based on:
- What's working (similar but untapped)
- Gaps in current coverage
- Platform-specific opportunities

Be specific: "Lookalike 3-5% based on purchasers last 90 days" not "try broader audiences"

## Output Format

```
AUDIENCE EFFICIENCY RANKING:
| Audience | Type | Spend | CPA | CPM | Frequency | Status |

SATURATION ALERTS:
| Audience | Frequency | CPM Change | Action | Urgency |

OVERLAP ISSUES:
| Audience A | Audience B | Est Overlap | Keep | Action |

SCALING ROADMAP:
1. [Next audience to test] — [why] — [budget needed] — [test duration]
2. ...
3. ...

NEW AUDIENCES TO TEST:
1. [Specific targeting] — [expected size] — [rationale]
2. ...
3. ...
```

## Rules

- Frequency thresholds differ by funnel stage: prospecting >3 is high, retargeting >8 is high
- Don't flag retargeting audiences for saturation unless frequency >8
- CPM increases alone don't mean saturation — check if it's platform-wide (auction dynamics) or audience-specific
- Minimum 7 days of data to make saturation calls
- When recommending new audiences, estimate size and ensure it's large enough for the budget
- If account is spending <$5K/month, recommend fewer, larger audiences over many small ones
- Always note that overlap analysis is estimated — actual overlap requires Meta's audience overlap tool
