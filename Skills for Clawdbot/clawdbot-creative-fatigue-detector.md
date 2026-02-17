---
name: creative-fatigue-detector
description: Analyze ad creative performance, spot fatigue, explain why ads work or fail, recommend what to kill, scale, or iterate
metadata: {"clawdbot": {"emoji": "🎨"}}
---

# Creative Analyst

Explain why ads work or fail. Spot creative fatigue before it tanks performance. Tell the user what to kill, scale, and test next.

## When To Activate

When the user asks about:
- Ad performance at the creative level
- Why specific ads are winning or losing
- Creative fatigue or declining performance
- What new creatives to test
- Format comparison (static vs video vs carousel)
- "Which ads should I turn off"

## What To Do

### Step 1: Collect Context

If not provided, ask:
- Platform (Google Ads / Meta Ads / both)
- Campaign objective (purchases, leads, traffic)
- Time period (default: last 14 days)
- Any recent creative changes or tests
- Target CPA or ROAS

### Step 2: Pull Data via MCP

Ad-level data:
- Ad name/ID, campaign name, ad set name
- Status, format (image, video, carousel, responsive)
- Spend, impressions, reach, frequency
- CTR, CPC, CPM
- Conversions, CPA, ROAS
- Thumbstop rate or hook rate (Meta, if available)
- Video watch % (if video)

Pull for current period AND previous period (same length) to calculate trends.

### Step 3: Winners Analysis

Identify top 5 ads by efficiency (lowest CPA or highest ROAS with meaningful spend).

For each winner:
- Performance metrics table
- **Why it works** — analyze the creative angle:
  - Hook type (question, statistic, pain point, curiosity)
  - Value proposition positioning
  - Social proof presence
  - CTA strength
  - Format advantages
- Pattern across winners (what do the top ads have in common)

### Step 4: Losers Analysis

Identify bottom 5 ads by efficiency (highest CPA with >$100 spend, or high spend zero conversions).

For each loser:
- Performance metrics table
- **Why it fails** — diagnose the issue:
  - Low CTR = hook/creative not compelling
  - High CTR but low CVR = landing page mismatch or wrong audience
  - High CPM = audience too narrow or competitive
  - High frequency + declining CTR = fatigue
- Pattern across losers (what do the bottom ads have in common)

### Step 5: Creative Fatigue Check

Flag any ad where:
- Frequency > 3 AND CTR declined >15% vs previous period
- Frequency > 5 (regardless of CTR trend)
- Impressions stable but CTR dropping week over week for 2+ weeks

For each fatigued ad:
| Ad | Frequency | CTR (current) | CTR (previous) | Decline % | Action |

Actions:
- **Kill** — frequency >5 and CTR down >25%
- **Refresh** — frequency 3-5 and CTR down 15-25%, new creative with same angle
- **Watch** — frequency 3-4 and CTR down <15%, check again in 3 days

### Step 6: Format Performance

Compare by format:
| Format | Ads | Spend | Avg CPA | Avg CTR | Avg CPM | Best Performer |

Recommend which formats to prioritize for next round of creative.

### Step 7: Kill / Scale / Iterate List

**KILL** (turn off today):
- Ads with CPA 2x+ target and no improvement trend
- Ads with fatigue signals and no path to recovery

**SCALE** (increase spend):
- Ads with CPA below target and room to run
- Include estimated headroom before fatigue

**ITERATE** (make variations):
- Winning ads approaching fatigue
- Suggest specific variations: new hook with same body, same hook with new visual, etc.

**TEST NEXT** (new concepts):
- Based on winner patterns, suggest 2-3 new angles to test
- Be specific: "Pain point hook + customer quote + soft CTA" not "try something different"

## Output Format

```
TOP PERFORMERS:
| Ad | Format | Spend | Conv | CPA | CTR | Why It Works |

BOTTOM PERFORMERS:
| Ad | Format | Spend | Conv | CPA | CTR | Why It Fails |

FATIGUE ALERTS:
| Ad | Frequency | CTR Change | Action |

FORMAT COMPARISON:
| Format | Avg CPA | Avg CTR | Recommendation |

ACTION LIST:
KILL: [list with reasons]
SCALE: [list with headroom estimates]
ITERATE: [list with specific variation ideas]
TEST NEXT: [2-3 new concepts based on winner patterns]
```

## Rules

- Analyze the creative itself, not just the numbers
- "Low CTR" is not a diagnosis — explain WHY the CTR is low
- Minimum $100 spend to include an ad in analysis (less = not enough data)
- Don't recommend killing ads in learning period (first 3-7 days)
- When suggesting iterations, be specific about what to change and what to keep
- If user has fewer than 5 active ads, note that creative diversity is too low
- Always compare current vs previous period, never just snapshot data
