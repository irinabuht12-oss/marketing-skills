---
name: linkedin-ads-audit
description: LinkedIn Ads campaign analysis for B2B marketers detecting CTR issues, audience quality problems, lead gen form friction, and budget inefficiencies. Use when pasting LinkedIn campaign exports, analyzing B2B ad performance, or auditing LinkedIn advertising spend.
metadata:
  platform: LinkedIn
---

# LinkedIn Ads Audit

Analyze LinkedIn ad campaigns for B2B performance optimization.

## Process

1. **Request campaign data** - Campaign Manager export or pasted metrics
2. **Benchmark performance** - Compare against LinkedIn B2B benchmarks
3. **Analyze audience quality** - Job titles, seniority, company size targeting
4. **Check lead gen forms** - Field count, friction points, completion rates
5. **Evaluate budget efficiency** - CPL, CPC, spend distribution
6. **Deliver prioritized fixes**

## LinkedIn Ads Benchmarks (B2B)

| Metric | Good | Average | Poor |
|--------|------|---------|------|
| CTR (Sponsored Content) | >0.5% | 0.3-0.5% | <0.3% |
| CTR (Text Ads) | >0.03% | 0.01-0.03% | <0.01% |
| CPC | <$5 | $5-10 | >$10 |
| CPL (Lead Gen Forms) | <$50 | $50-150 | >$150 |
| Lead Gen Form Completion | >15% | 10-15% | <10% |
| Engagement Rate | >2% | 1-2% | <1% |

## Audience Quality Checklist

- [ ] Job titles specific (not just "Manager")
- [ ] Seniority levels appropriate for offer
- [ ] Company size matches ICP
- [ ] Industry targeting narrow enough
- [ ] Excluding irrelevant titles (students, job seekers)
- [ ] Audience size 50K-500K (sweet spot)

## Lead Gen Form Friction Analysis

| Fields | Expected Completion Rate |
|--------|-------------------------|
| 3-4 fields | 15-25% |
| 5-6 fields | 10-15% |
| 7+ fields | <10% |

**High-friction fields to avoid:**
- Phone number (unless essential)
- Company revenue
- Custom text fields
- Multiple dropdowns

**Use instead:**
- Pre-filled LinkedIn data (name, email, company, title)
- Single dropdown for key qualification

## Budget Efficiency Issues

| Issue | Signal | Fix |
|-------|--------|-----|
| Overspending on awareness | High impressions, low CTR | Narrow audience |
| Audience too broad | Low CPL but poor lead quality | Add exclusions |
| Creative fatigue | CTR declining week-over-week | Refresh ads |
| Wrong objective | High CPC on brand awareness | Switch to lead gen |

## Output Format

```
## LinkedIn Ads Audit

**Account**: [Name]
**Analysis Period**: [Date Range]
**Total Spend**: $[Amount]

### Performance vs Benchmarks
| Metric | Your Performance | Benchmark | Status |
|--------|-----------------|-----------|--------|
| CTR | | 0.4% | 🟢/🟡/🔴 |
| CPC | | $7 | 🟢/🟡/🔴 |
| CPL | | $100 | 🟢/🟡/🔴 |

### Audience Quality Assessment
- **Targeting**: [Evaluation]
- **Exclusions**: [Missing exclusions]
- **Size**: [Too broad/narrow/optimal]

### Lead Gen Form Analysis
- **Fields**: [Count]
- **Completion Rate**: [X]%
- **Friction Points**: [List]

### Top Issues
| Priority | Issue | Impact | Fix |
|----------|-------|--------|-----|
| 1 | | | |
| 2 | | | |

### Budget Recommendations
- [Recommendation 1]
- [Recommendation 2]

### Confidence Level: [HIGH/MEDIUM/LOW]
```

## Example

**Input**: "LinkedIn campaign: $5K spend, 500K impressions, 1,200 clicks, 45 leads. Targeting: Marketing Managers, Directors at companies 50-1000 employees. Lead form has 7 fields."

**Output**:
```
## LinkedIn Ads Audit

**Total Spend**: $5,000
**Leads**: 45

### Performance vs Benchmarks
| Metric | Your Performance | Benchmark | Status |
|--------|-----------------|-----------|--------|
| CTR | 0.24% | 0.4% | 🔴 Below |
| CPC | $4.17 | $7 | 🟢 Good |
| CPL | $111 | $100 | 🟡 Average |

### Lead Gen Form Analysis
- **Fields**: 7 (too many)
- **Expected Completion Rate**: <10%
- **Friction Points**: Reduce to 4 fields, use pre-filled data

### Top Issues
| Priority | Issue | Impact | Fix |
|----------|-------|--------|-----|
| 1 | Low CTR (0.24%) | Wasted impressions | Test new creative, tighten audience |
| 2 | 7 form fields | Low completion | Reduce to 4, remove phone |

### Confidence Level: HIGH
```

## Guidelines

- Always compare against B2B benchmarks, not general LinkedIn stats
- Lead quality matters more than CPL - ask about lead-to-opportunity rate
- If no benchmark data provided, use industry averages
- Flag if audience size is <20K (too narrow) or >1M (too broad)
