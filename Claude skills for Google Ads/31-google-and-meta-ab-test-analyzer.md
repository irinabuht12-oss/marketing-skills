---
name: ab-test-analyzer
description: Statistical significance calculator for A/B test results with sample size requirements, segment breakdowns, and hypothesis generation. Use when feeding test results, checking statistical significance, calculating sample sizes, analyzing experiment outcomes, or generating next test ideas based on results.
metadata:
  platform: Google and Meta
---

# A/B Test Analyzer

Evaluate A/B test results with statistical rigor and generate actionable next steps.

## Process

1. **Collect test data** - Variations, sample sizes, conversions, time period
2. **Check validity** - Runtime, sample size, peeking issues
3. **Calculate significance** - Z-score, p-value, confidence interval
4. **Segment analysis** - Device, source, new vs returning
5. **Interpret results** - Statistical vs practical significance
6. **Generate hypotheses** - "Why it worked" and next test ideas

## Sample Size Calculator

```
n = 2 × (Zα/2 + Zβ)² × p(1-p) / δ²

Where:
- n = sample size per variation
- Zα/2 = 1.96 (95% confidence) or 2.58 (99%)
- Zβ = 0.84 (80% power) or 1.28 (90%)
- p = baseline conversion rate
- δ = minimum detectable effect (absolute)
```

**Quick Reference (95% confidence, 80% power)**:
| Baseline CR | 10% Relative MDE | 20% Relative MDE |
|-------------|------------------|------------------|
| 2% | 78,000/var | 19,500/var |
| 5% | 30,000/var | 7,500/var |
| 10% | 14,300/var | 3,600/var |

## Significance Calculation

```
Z-score = (pB - pA) / √(SE²_A + SE²_B)
SE = √(p × (1-p) / n)

If |Z| > 1.96 → Significant at 95%
If |Z| > 2.58 → Significant at 99%
```

## Validity Checklist

- [ ] Ran for minimum 14 days (day-of-week effects)
- [ ] Met required sample size before concluding
- [ ] No "peeking" at results during test (inflates false positives to 40%+)
- [ ] Traffic split was random and consistent
- [ ] No external factors (holidays, outages, campaigns)

## Bayesian vs Frequentist

| Use Case | Approach |
|----------|----------|
| Large samples (>10K), yes/no decision | Frequentist |
| Continuous monitoring, early stopping | Bayesian |
| Regulatory/legal requirements | Frequentist |
| Want probability statements | Bayesian |

## Output Format

```
## A/B Test Analysis

### Test Summary
- **Test Name**: [Name]
- **Hypothesis**: [What you expected]
- **Runtime**: [X days]
- **Sample Size**: Control [n] / Variant [n]

### Results
| Metric | Control | Variant | Lift | Significant? |
|--------|---------|---------|------|--------------|
| Conversion Rate | X% | Y% | +Z% | ✅/❌ |

### Statistical Details
- Z-score: [X]
- P-value: [X]
- Confidence Interval: [X% to Y%]
- Power achieved: [X]%

### Validity Assessment
- ✅/❌ Minimum runtime met
- ✅/❌ Sample size requirement met
- ✅/❌ No external confounds identified

### Segment Breakdown
| Segment | Control CR | Variant CR | Lift | Notes |
|---------|-----------|------------|------|-------|
| Mobile | | | | |
| Desktop | | | | |

### Interpretation
[Statistical significance vs practical significance discussion]

### "Why It Worked" Hypotheses
1. [Hypothesis about mechanism]
2. [Alternative explanation]

### Next Test Ideas
1. [Follow-up test based on learnings]
2. [Adjacent hypothesis to explore]

### Confidence Level: [HIGH/MEDIUM/LOW]
```

## Example

**Input**: "Tested new headline. Control: 10,000 visitors, 250 conversions. Variant: 10,000 visitors, 300 conversions. Ran for 7 days."

**Output**:
```
## A/B Test Analysis

### Test Summary
- **Hypothesis**: New headline increases conversions
- **Runtime**: 7 days ⚠️
- **Sample Size**: Control 10,000 / Variant 10,000

### Results
| Metric | Control | Variant | Lift | Significant? |
|--------|---------|---------|------|--------------|
| Conversion Rate | 2.5% | 3.0% | +20% | ✅ Yes (95%) |

### Statistical Details
- Z-score: 2.28
- P-value: 0.023
- Confidence Interval: +2.3% to +37.7%
- Power achieved: 62% ⚠️

### Validity Assessment
- ❌ Minimum runtime NOT met (7 days < 14 days recommended)
- ⚠️ Sample size marginal for 20% MDE
- ❓ Cannot assess external confounds without more context

### Interpretation
Result is **statistically significant** but validity concerns exist:
1. 7-day runtime may miss day-of-week patterns
2. Wide confidence interval (+2% to +38%) indicates uncertainty
3. Recommend extending test 7 more days to confirm

### "Why It Worked" Hypotheses
1. New headline more clearly communicates value proposition
2. Specificity/numbers in headline increased credibility

### Next Test Ideas
1. Test headline variations that emphasize the winning element
2. Apply same messaging pattern to subheadline

### Confidence Level: MEDIUM
Statistical significance achieved, but short runtime reduces confidence.
```

## Guidelines

- Never declare a winner without checking validity
- Distinguish statistical significance from practical significance
- If test ran <7 days, always recommend extending
- If sample size insufficient, calculate required runtime to reach it
- Ask for segment data if not provided - results often differ by device/source
