Google

---
name: google-ads-audit
description: Comprehensive Google Ads account health analysis detecting wasted spend, search term leaks, negative keyword gaps, bid strategy issues, and Quality Score problems. Use when analyzing campaign data, pasting Google Ads exports, reviewing account performance, or requesting a full diagnostic of advertising spend efficiency.
---

# Google Ads Audit

Perform systematic account analysis to identify optimization opportunities and wasted spend.

## Process

1. **Request campaign data** - Ask for exports from Google Ads (campaign, ad group, keyword, search terms reports) or accept pasted data
2. **Analyze wasted spend** - Sort search terms by spend, filter zero-conversion terms
3. **Evaluate structure** - Check campaign organization, ad group themes, keyword count
4. **Assess Quality Scores** - Review Expected CTR, Landing Page Experience, Ad Relevance
5. **Check bid strategy alignment** - Match strategy to campaign goals and conversion volume
6. **Deliver prioritized recommendations** - High impact + Low effort first

## Audit Checklist

### Wasted Spend Detection
- Keywords with 50+ clicks, 0 conversions → Flag for review/pause
- Search terms containing: "free," "jobs," "DIY," "how to," "tutorial," "login," "salary," "reddit" → Add as negatives
- One-word search terms (too broad) → Add as negatives
- Terms with high impressions but CTR <1% → Review relevance

### Negative Keywords
- No negatives added in 30+ days → Flag
- Branded terms appearing in non-brand campaigns → Add negatives
- Check for account-level vs campaign-level lists

### Quality Score Thresholds
| Metric | Target | Red Flag |
|--------|--------|----------|
| Non-brand QS | ≥7 | <5 |
| Brand QS | 10 | <8 |
| CTR | ≥1.5% | <1% |
| Conversion Rate | ≥8% | <3% |
| Search Impression Share | >80% (priority) | <50% |

### Structure Issues
- Ad groups with 20+ keywords → Split into themes
- Display + Search combined → Separate campaigns
- Missing ad extensions → Add sitelinks, callouts, structured snippets
- Performance Max without audience signals → Add signals

## Output Format

```
## Google Ads Audit Summary

**Account Health Score**: [X/100]
**Analysis Period**: [Date Range]
**Total Spend Analyzed**: $[Amount]

### 🔴 Critical Issues (Immediate Action)
1. [Issue] - Est. Wasted Spend: $[X]/month
   - Action: [Specific fix]

### 🟡 Optimization Opportunities
1. [Opportunity] - Potential Impact: [X]%
   - Action: [Specific fix]

### 🟢 What's Working Well
- [Positive finding]

### Priority Action Plan
| Priority | Action | Impact | Effort | Est. Savings |
|----------|--------|--------|--------|--------------|
| 1 | | High | Low | |

### Confidence Level: [HIGH/MEDIUM/LOW]
[Reasoning for confidence assessment]
```

## Example

**Input**: "Here's my campaign data: Brand campaign $5K/month, 3.2% CTR, QS 9. Non-brand: $15K/month, 0.8% CTR, QS 4, 500 search terms with 0 conversions spending $3K"

**Output**:
```
## Google Ads Audit Summary

**Account Health Score**: 45/100
**Total Spend Analyzed**: $20,000/month

### 🔴 Critical Issues
1. **Non-brand Quality Score critically low (4)** - Est. Wasted Spend: $4,500/month
   - Action: Improve ad relevance, tighten keyword-ad group themes, review landing pages

2. **Search term waste ($3K on zero-conversion terms)** - Est. Wasted Spend: $3,000/month
   - Action: Add negative keywords, pause low-performing exact matches

### Priority Action Plan
| Priority | Action | Impact | Effort | Est. Savings |
|----------|--------|--------|--------|--------------|
| 1 | Add negative keywords for 0-conv terms | High | Low | $3,000/mo |
| 2 | Restructure ad groups (SKAG/STAG) | High | High | $2,000/mo |

### Confidence Level: HIGH
Complete data provided for key metrics.
```

## Guidelines

- If data is incomplete, state what's missing and request it
- Never guess at conversion values or assume performance
- Flag anomalies (negative spend, CTR >100%) without processing
- Include confidence level with every assessment
