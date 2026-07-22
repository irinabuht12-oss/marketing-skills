---
name: reddit-ads-audit
description: Reddit Ads campaign analysis detecting community targeting issues, creative fatigue, bid inefficiencies, and subreddit performance problems. Use when pasting Reddit Ads data, analyzing subreddit targeting, or auditing Reddit advertising spend for B2B or B2C campaigns.
metadata:
  platform: Reddit
---

# Reddit Ads Audit

Analyze Reddit ad campaigns for community-driven performance optimization.

## Process

1. **Request campaign data** - Reddit Ads Manager export or pasted metrics
2. **Analyze subreddit targeting** - Community relevance, size, engagement
3. **Check creative fit** - Native vs promotional feel
4. **Evaluate bidding** - CPM/CPC efficiency by placement
5. **Identify audience issues** - Interest targeting vs subreddit targeting
6. **Deliver prioritized fixes**

## Reddit Ads Benchmarks

| Metric | Good | Average | Poor |
|--------|------|---------|------|
| CTR (Feed) | >0.5% | 0.2-0.5% | <0.2% |
| CTR (Conversation) | >1% | 0.5-1% | <0.5% |
| CPC | <$1.50 | $1.50-3 | >$3 |
| CPM | <$5 | $5-10 | >$10 |
| Engagement Rate | >3% | 1-3% | <1% |
| Conversion Rate | >2% | 1-2% | <1% |

## Subreddit Targeting Analysis

### Red Flags
- Targeting broad interest categories only (no specific subreddits)
- Subreddits with <50K members (too small for scale)
- Subreddits with >5M members (too broad, wasted spend)
- Mismatched subreddit culture (promotional tone in anti-ad communities)
- Not excluding default/general subreddits

### Sweet Spot
- 100K-1M member subreddits
- Niche but active communities
- Communities where your product is naturally discussed
- Multiple related subreddits grouped by theme

## Creative Fit Checklist

Reddit users hate obvious ads. Check:

- [ ] Headline sounds like a Reddit post (not ad copy)
- [ ] No stock photos (use screenshots, real images)
- [ ] Copy uses community language
- [ ] Not overly promotional/salesy
- [ ] Includes social proof or results
- [ ] CTA is soft (not "BUY NOW")

**Good**: "We built a tool that does X. Here's what we learned."
**Bad**: "🚀 Amazing Software - 50% OFF - Limited Time! 🚀"

## Bidding & Budget Issues

| Issue | Signal | Fix |
|-------|--------|-----|
| Overpaying for impressions | High CPM, low CTR | Switch to CPC bidding |
| Low delivery | Budget not spending | Increase bid or broaden targeting |
| Poor placement mix | All spend on one placement | Test conversation ads |
| Audience too narrow | High CPC, low volume | Add related subreddits |

## Output Format

```
## Reddit Ads Audit

**Account**: [Name]
**Analysis Period**: [Date Range]
**Total Spend**: $[Amount]

### Performance vs Benchmarks
| Metric | Your Performance | Benchmark | Status |
|--------|-----------------|-----------|--------|
| CTR | | 0.4% | 🟢/🟡/🔴 |
| CPC | | $2 | 🟢/🟡/🔴 |
| CPM | | $7 | 🟢/🟡/🔴 |

### Subreddit Targeting Assessment
**Current targeting**: [List]
**Issues**:
- [Issue 1]
- [Issue 2]

**Recommended subreddits to add**:
- r/[subreddit] - [reason]

**Recommended exclusions**:
- r/[subreddit] - [reason]

### Creative Fit Score: [X/10]
- [What's working]
- [What needs fixing]

### Top Issues
| Priority | Issue | Impact | Fix |
|----------|-------|--------|-----|
| 1 | | | |
| 2 | | | |

### Confidence Level: [HIGH/MEDIUM/LOW]
```

## Example

**Input**: "Reddit campaign for SaaS tool: $2K spend, targeting 'Technology' interest, 800K impressions, 1,500 clicks, 8 conversions. Creative headline: 'Best Project Management Software - Try Free!'"

**Output**:
```
## Reddit Ads Audit

**Total Spend**: $2,000
**Conversions**: 8

### Performance vs Benchmarks
| Metric | Your Performance | Benchmark | Status |
|--------|-----------------|-----------|--------|
| CTR | 0.19% | 0.4% | 🔴 Below |
| CPC | $1.33 | $2 | 🟢 Good |
| Conv Rate | 0.53% | 1.5% | 🔴 Below |
| CPA | $250 | - | 🔴 High |

### Subreddit Targeting Assessment
**Current targeting**: Broad "Technology" interest
**Issues**:
- Too broad - reaching millions who don't need PM software
- No specific subreddits selected
- Wasting budget on irrelevant impressions

**Recommended subreddits to add**:
- r/projectmanagement (200K) - direct audience
- r/startups (800K) - decision makers
- r/SaaS (50K) - software buyers
- r/Entrepreneur (2M) - business owners

### Creative Fit Score: 3/10
- ❌ "Best" claim = instant skip
- ❌ Sounds like generic ad copy
- ❌ No social proof or story

**Suggested rewrite**: "We switched from Asana to our own tool. Here's why (and the template we use)"

### Top Issues
| Priority | Issue | Impact | Fix |
|----------|-------|--------|-----|
| 1 | Broad interest targeting | 80% wasted spend | Target specific subreddits |
| 2 | Promotional creative | Low CTR | Rewrite as native content |

### Confidence Level: HIGH
```

## Guidelines

- Reddit audience hates obvious advertising - always check creative fit
- Subreddit targeting beats interest targeting 90% of the time
- If CTR is low, creative is usually the problem
- Recommend specific subreddits based on the product/service
- Ask about comment sentiment if available (negative comments kill performance)
