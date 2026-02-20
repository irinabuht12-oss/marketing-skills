---
name: meta-ads-audit
description: Meta/Facebook/Instagram Ads campaign structure analysis detecting creative fatigue, audience overlap, scaling opportunities, and iOS tracking verification issues. Use when pasting Meta account data, analyzing Facebook ad performance, reviewing Instagram campaigns, or requesting audit of social advertising spend.
platform: Meta
---

# Meta Ads Audit

Analyze Meta advertising accounts for structural issues, creative performance, and tracking health.

## Process

1. **Request account data** - Ads Manager exports (campaign, ad set, ad level with time series)
2. **Check creative fatigue signals** - Frequency, CTR trends, CPM inflation
3. **Analyze audience overlap** - Identify cannibalization between ad sets
4. **Verify tracking setup** - Pixel, Conversions API, Event Match Quality
5. **Evaluate campaign structure** - Advantage+ vs Manual decisions
6. **Deliver prioritized recommendations**

## Creative Fatigue Detection

| Signal | Threshold | Action Required |
|--------|-----------|-----------------|
| Frequency | >3-4 | Refresh creative or expand audience |
| CTR declining | >15-20% drop over 7 days | New creative needed |
| CPM rising | >30-40% over 2 weeks | Creative reset required |
| Ad Relevance | "Below Average" ranking | Immediate creative swap |

## Audience Overlap Analysis

**Scoring (use Facebook Audience Overlap Tool)**:
- 0-15% overlap = Safe, continue
- 15-30% overlap = Monitor, consider consolidation
- >30% overlap = Consolidate or add exclusions

## Tracking Verification Checklist

- [ ] Meta Pixel installed (use Pixel Helper Chrome extension)
- [ ] Conversions API (CAPI) configured with server-side events
- [ ] Event Match Quality score ≥6
- [ ] Browser events (blue) AND server events (green) firing in Events Manager
- [ ] iOS 14.5+ ATT prompt implemented
- [ ] Aggregated Event Measurement configured (8 events prioritized)

## Advantage+ vs Manual Decision Logic

**Use Advantage+ Shopping/App campaigns when**:
- Scaling established products
- Prospecting broad audiences
- Budget >$100/day for algorithm learning
- Have 50+ conversions/week

**Use Manual campaigns when**:
- Retargeting specific segments
- Testing new creatives
- Budget <$50/day
- Need precise audience control

## Output Format

```
## Meta Ads Audit Summary

**Account Health Score**: [X/100]
**Analysis Period**: [Date Range]
**Total Spend Analyzed**: $[Amount]

### 🔴 Creative Fatigue Alerts
| Campaign | Frequency | CTR Trend | Action |
|----------|-----------|-----------|--------|

### 🟡 Audience Issues
- Overlap detected: [Ad Set A] ↔ [Ad Set B]: [X]%
- Recommendation: [Action]

### 📊 Tracking Health
- Pixel: [✅/❌]
- CAPI: [✅/❌]
- EMQ Score: [X/10]

### Scaling Opportunities
1. [Campaign] - ROAS [X], ready for [X]% budget increase

### Confidence Level: [HIGH/MEDIUM/LOW]
```

## Example

**Input**: "Campaign A: $5K spend, frequency 5.2, CTR dropped 25% this week. Campaign B: $3K, frequency 2.1, stable CTR. Both targeting 'fitness enthusiasts' with 40% overlap."

**Output**:
```
## Meta Ads Audit Summary

**Account Health Score**: 55/100

### 🔴 Creative Fatigue Alerts
| Campaign | Frequency | CTR Trend | Action |
|----------|-----------|-----------|--------|
| Campaign A | 5.2 (HIGH) | -25% ⚠️ | Immediate creative refresh |
| Campaign B | 2.1 (OK) | Stable | Monitor |

### 🟡 Audience Issues
- Overlap detected: Campaign A ↔ Campaign B: 40% (CRITICAL)
- Recommendation: Consolidate into single campaign or add exclusions. Currently bidding against yourself.

### Priority Actions
1. Pause Campaign A creatives, launch 3-5 new variations
2. Add Campaign B audiences as exclusion to Campaign A (or vice versa)
3. Consider CBO to let algorithm optimize across ad sets

### Confidence Level: HIGH
Time-series data provided for trend analysis.
```

## Guidelines

- Request at minimum 14 days of data for trend analysis
- If tracking data unavailable, note this as critical gap
- Never assume iOS tracking loss percentage - ask for actual data
- Flag frequency >7 as severe (audience exhaustion)
