---
name: e2e-seo-assistant
description: Full SEO workflow covering technical audits, content gaps, backlink opportunities, on-page fixes, and content briefs. Use when given a site and target keywords to get complete SEO analysis and actionable content plans. End-to-end SEO in one skill.
platform: Google
---

# E2E SEO Assistant

Complete SEO workflow from audit to content brief in one pass.

## Process

1. **Technical audit** - Site health, crawlability, Core Web Vitals
2. **On-page analysis** - Title tags, meta descriptions, headers, content
3. **Content gap analysis** - What competitors rank for that you don't
4. **Backlink opportunities** - Where to build links
5. **Keyword mapping** - Match keywords to pages
6. **Content brief** - Ready-to-write brief for priority keyword

## Technical SEO Checklist

### Crawlability
- [ ] Robots.txt not blocking important pages
- [ ] XML sitemap exists and submitted
- [ ] No orphan pages (pages with no internal links)
- [ ] Crawl depth <4 clicks from homepage
- [ ] No redirect chains (max 1 redirect)

### Indexability
- [ ] No accidental noindex tags
- [ ] Canonical tags correctly set
- [ ] No duplicate content issues
- [ ] Hreflang for international (if applicable)

### Core Web Vitals
| Metric | Good | Needs Work | Poor |
|--------|------|------------|------|
| LCP (Largest Contentful Paint) | <2.5s | 2.5-4s | >4s |
| INP (Interaction to Next Paint) | <200ms | 200-500ms | >500ms |
| CLS (Cumulative Layout Shift) | <0.1 | 0.1-0.25 | >0.25 |

### Site Health
- [ ] HTTPS everywhere
- [ ] Mobile-friendly
- [ ] No broken links (4xx errors)
- [ ] No server errors (5xx)
- [ ] Fast page load (<3s)

## On-Page SEO Checklist

### Title Tags
- [ ] Under 60 characters
- [ ] Primary keyword included
- [ ] Unique per page
- [ ] Compelling (not just keyword stuffing)

### Meta Descriptions
- [ ] Under 155 characters
- [ ] Includes keyword naturally
- [ ] Has call-to-action
- [ ] Unique per page

### Headers
- [ ] One H1 per page
- [ ] H1 includes primary keyword
- [ ] Logical H2-H6 hierarchy
- [ ] Keywords in subheadings

### Content
- [ ] Answers search intent
- [ ] Comprehensive (vs competitors)
- [ ] Internal links to related pages
- [ ] External links to authoritative sources
- [ ] Images with alt text

## Content Gap Framework

### Find Gaps By
1. **Competitor keywords** - What they rank for, you don't
2. **Search intent gaps** - Informational content missing
3. **Funnel gaps** - TOFU/MOFU/BOFU content missing
4. **Topic clusters** - Supporting content for pillar pages

### Prioritize By
| Factor | Weight |
|--------|--------|
| Search volume | High |
| Keyword difficulty | Medium (prefer <40 KD) |
| Business value | High |
| Content effort | Medium |

## Backlink Opportunity Types

| Type | How to Find | Effort |
|------|-------------|--------|
| **Resource pages** | "[topic] + resources" | Low |
| **Broken link building** | Competitor 404s | Medium |
| **Guest posts** | "[industry] + write for us" | Medium |
| **HARO/Connectively** | Reporter queries | Low |
| **Competitor backlinks** | Ahrefs/Semrush analysis | Medium |
| **Unlinked mentions** | Brand monitoring | Low |

## Content Brief Template

### Brief Structure
1. **Target keyword** + secondary keywords
2. **Search intent** (informational/transactional/navigational)
3. **Target word count** (based on SERP analysis)
4. **Outline** (H1, H2s, H3s)
5. **Questions to answer** (People Also Ask)
6. **Internal links** to include
7. **Competitor analysis** (what to beat)

## Output Format

```
## SEO Audit: [Domain]

### Technical Health Score: [X/100]

#### Critical Issues
| Issue | Pages Affected | Impact | Fix |
|-------|---------------|--------|-----|
| | | High/Med/Low | |

#### Core Web Vitals
| Metric | Score | Status |
|--------|-------|--------|
| LCP | | 🟢/🟡/🔴 |
| INP | | 🟢/🟡/🔴 |
| CLS | | 🟢/🟡/🔴 |

---

### On-Page Issues

#### Title Tag Problems
| Page | Current Title | Issue | Suggested |
|------|--------------|-------|-----------|
| | | | |

#### Content Gaps
| Keyword | Volume | KD | Competitor Ranking | Priority |
|---------|--------|----|--------------------|----------|
| | | | | High/Med/Low |

---

### Backlink Opportunities
| Opportunity | URL | Approach |
|-------------|-----|----------|
| | | |

---

### Content Brief: [Priority Keyword]

**Target Keyword**: [keyword]
**Secondary Keywords**: [list]
**Search Intent**: [type]
**Target Word Count**: [X] words

**Suggested Title**: [title tag]
**Meta Description**: [description]

**Outline**:
# H1: [title]
## H2: [section]
### H3: [subsection]
...

**Questions to Answer**:
- [PAA question 1]
- [PAA question 2]

**Internal Links**:
- [Page 1] - anchor text: [text]
- [Page 2] - anchor text: [text]

**Competitor Analysis**:
| Competitor | Word Count | Unique Angle |
|------------|------------|--------------|
| | | |

---

### Priority Action Plan
| Priority | Action | Impact | Effort |
|----------|--------|--------|--------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

### Confidence Level: [HIGH/MEDIUM/LOW]
```

## Example

**Input**: "Full SEO audit for a B2B SaaS blog. Target keyword: 'employee onboarding software'"

**Output**:
```
## SEO Audit: [B2B SaaS Blog]

### Content Brief: "employee onboarding software"

**Target Keyword**: employee onboarding software
**Secondary Keywords**: onboarding software for small business, best onboarding tools, HR onboarding platform
**Search Intent**: Commercial investigation (comparing options)
**Target Word Count**: 2,500-3,000 words (competitors average 2,200)

**Suggested Title**: Best Employee Onboarding Software (2025) - Top 10 Compared
**Meta Description**: Compare the best employee onboarding software for 2025. Features, pricing, and pros/cons for HR teams at SMBs and enterprises.

**Outline**:
# H1: Best Employee Onboarding Software for 2025
## H2: What to Look for in Onboarding Software
### H3: Must-Have Features
### H3: Nice-to-Have Features
## H2: Top 10 Employee Onboarding Software
### H3: [Tool 1] - Best for SMBs
### H3: [Tool 2] - Best for Enterprise
... (repeat for each)
## H2: How to Choose the Right Onboarding Software
## H2: Onboarding Software Pricing Comparison
## H2: FAQ

**Questions to Answer**:
- What is employee onboarding software?
- How much does onboarding software cost?
- What's the best free onboarding software?
- How long should employee onboarding take?

**Internal Links**:
- /blog/onboarding-checklist - anchor: "onboarding checklist"
- /product - anchor: "our onboarding solution"

**Competitor Analysis**:
| Competitor | Word Count | Unique Angle |
|------------|------------|--------------|
| G2 | 3,100 | User reviews, badges |
| Capterra | 2,400 | Pricing focus |
| SHRM | 1,800 | HR compliance angle |

**Your angle**: Focus on time-to-productivity metrics + ROI calculator

### Confidence Level: HIGH
```

## Guidelines

- Always check search intent before recommending content
- Prioritize quick wins (high impact, low effort)
- Content briefs should be actionable, not vague
- If no access to site data, note what tools would help (Screaming Frog, Ahrefs, etc.)
- Ask for target keywords if not provided
