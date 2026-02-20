---
name: ad-spend-allocator
description: Multi-channel budget optimization using MER, marginal ROAS, and diminishing returns analysis. Use when pasting multi-channel spend and results data, requesting reallocation recommendations, analyzing budget shift priorities, or optimizing marketing efficiency across Google, Meta, TikTok, and other channels.
metadata:
  platform: Google and Meta
---

# Ad Spend Allocator

Optimize budget distribution across advertising channels using efficiency metrics and diminishing returns analysis.

## Process

1. **Collect channel data** - Spend, revenue, conversions by channel (minimum 30 days)
2. **Calculate efficiency metrics** - MER, aMER, channel ROAS, marginal ROAS
3. **Identify diminishing returns** - Detect channels approaching saturation
4. **Apply allocation framework** - 70-20-10 rule as baseline
5. **Recommend shifts** - 10-20% increments with monitoring periods

## Key Formulas

```
MER (Marketing Efficiency Ratio) = Total Revenue / Total Marketing Spend
Target: 3.0-5.0x (varies by industry, margin structure)

aMER (Acquisition MER) = New Customer Revenue / Total Ad Spend
Purpose: Isolates new customer acquisition efficiency

Channel ROAS = Channel Revenue / Channel Spend
Use for: Channel comparison, baseline performance

Marginal ROAS = (Revenue at Spend B - Revenue at Spend A) / (Spend B - Spend A)
Purpose: Detect diminishing returns before blended ROAS shows issues
```

## 70-20-10 Budget Allocation Rule

| Tier | Allocation | Criteria |
|------|------------|----------|
| **Proven** | 70% | Consistent ROAS, predictable results, 3+ months track record |
| **Scaling** | 20% | Emerging opportunities, positive early signals, testing scale |
| **Testing** | 10% | New channels, creative experiments, unproven strategies |

## Diminishing Returns Indicators

- Higher CPC with same targeting (auction saturation)
- Frequency increasing on Meta (audience exhaustion)
- Conversion rate declining while impressions increase
- CPM inflation without response improvement
- Marginal ROAS dropping below blended ROAS

## Reallocation Decision Framework

1. Calculate marginal ROAS by channel (compare week-over-week at different spend levels)
2. Identify channels approaching saturation (marginal ROAS < blended ROAS)
3. Shift 10-20% at a time to unsaturated channels
4. Monitor for 7-14 days before further changes
5. Document and track impact

## Output Format

```
## Budget Allocation Analysis

**Total Monthly Spend**: $[X]
**Current MER**: [X]x
**Target MER**: [X]x

### Channel Efficiency Summary
| Channel | Spend | Revenue | ROAS | Marginal ROAS | Status |
|---------|-------|---------|------|---------------|--------|
| | | | | | [Scaling/Saturated/Testing] |

### Diminishing Returns Detection
- [Channel]: [Evidence of saturation]

### Recommended Reallocation
| From | To | Amount | Rationale |
|------|-----|--------|-----------|

### 70-20-10 Current vs Recommended
| Tier | Current | Recommended | Gap |
|------|---------|-------------|-----|
| Proven (70%) | | | |
| Scaling (20%) | | | |
| Testing (10%) | | | |

### Expected Impact
- Projected MER improvement: [X]%
- Confidence: [HIGH/MEDIUM/LOW]

### Monitoring Plan
- Review metrics in [X] days
- Key indicators to watch: [List]
```

## Example

**Input**: "Google Ads: $50K, $200K revenue. Meta: $30K, $90K revenue. TikTok: $10K, $25K revenue. Seeing Meta CPMs up 35% last month."

**Output**:
```
## Budget Allocation Analysis

**Total Monthly Spend**: $90,000
**Current MER**: 3.5x ($315K / $90K)

### Channel Efficiency Summary
| Channel | Spend | Revenue | ROAS | Status |
|---------|-------|---------|------|--------|
| Google | $50K (56%) | $200K | 4.0x | Scaling |
| Meta | $30K (33%) | $90K | 3.0x | ⚠️ Saturated |
| TikTok | $10K (11%) | $25K | 2.5x | Testing |

### Diminishing Returns Detection
- **Meta**: 35% CPM increase signals auction saturation/creative fatigue

### Recommended Reallocation
| From | To | Amount | Rationale |
|------|-----|--------|-----------|
| Meta | Google | $6K (20%) | Higher efficiency, room to scale |
| Meta | TikTok | $3K (10%) | Test scaling opportunity |

### Expected Impact
- Projected MER improvement: 8-12%
- Confidence: MEDIUM (need marginal ROAS data for precision)

### Monitoring Plan
- Review in 14 days
- Watch: Google CPC trends, TikTok conv rate, Meta frequency
```

## Guidelines

- Never recommend >20% shifts at once (too disruptive)
- If marginal ROAS data unavailable, note this and use blended metrics with lower confidence
- Account for seasonality - compare year-over-year if possible
- Flag if total spend seems misaligned with business size
