# 📈 Performance Auditor

Full account health check — finds what's broken and what's being missed

---

## When to Use

- Weekly account review (start here)
- Performance suddenly changed
- Taking over a new account
- Monthly reporting
- Before budget discussions
- Something feels off but you can't pinpoint it

---

## Data You Need

Export from Google Ads or Meta Ads Manager (last 7-30 days):

| Field | Required |
| --- | --- |
| Campaign name | ✅ |
| Status | ✅ |
| Spend | ✅ |
| Impressions | ✅ |
| Clicks | ✅ |
| CTR | ✅ |
| CPC | ✅ |
| Conversions | ✅ |
| CPA | ✅ |
| ROAS | ✅ |
| Conv. Rate | ✅ |

**Backend data (highly recommended):**
- Actual conversions from CRM
- Actual revenue
- Lead quality scores
- Customer acquisition data

**Comparison data (helpful):**
- Previous period (last week, last month)
- Same period last year

---

## Prompt

```
You are a performance auditor reviewing an ad account

Your job is to find what's broken, what's being missed, and what to fix first

## Your Tasks

1. **Account Health Score**
   - Overall assessment: Healthy / Warning / Critical
   - Total spend efficiency vs targets
   - Trend direction (improving / stable / declining)

2. **Anomaly Detection**
   - Sudden performance drops (>20% change)
   - Unexpected spikes
   - Unusual patterns
   - For each anomaly: possible causes and how to investigate

3. **Hidden Losers**
   - Campaigns/ad sets that look okay but drag overall performance
   - Things spending budget without proportional results
   - "Zombie" campaigns (running but barely performing)

4. **Hidden Winners**
   - Campaigns that deserve more budget but aren't getting it
   - High performers limited by budget or bid caps
   - Opportunities being left on the table

5. **Attribution Check** (if backend data provided)
   - Platform-reported vs actual conversions
   - Discrepancy % by campaign
   - Which campaigns over-report vs under-report

6. **Prioritized Action List**
   - Quick wins (fix today, immediate impact)
   - This week (important but need more work)
   - Strategic (longer-term improvements)

## Rules

- Be brutally honest — no sugarcoating
- Quantify everything: "This is wasting $X per week"
- Prioritize by impact, not by ease
- Flag data quality issues if you see them
- If something looks suspicious, say so

## My Context

- Platform: [GOOGLE / META / BOTH]
- Time period: [7 / 14 / 30 DAYS]
- Main KPI: [CPA / ROAS / LEAD VOLUME / REVENUE]
- Target CPA: [YOUR TARGET]
- Target ROAS: [YOUR TARGET]
- Business context: [ANY RELEVANT CONTEXT — SEASONALITY, PROMOS, CHANGES]

## Platform Data

[PASTE YOUR CAMPAIGN SUMMARY DATA HERE]

## Backend Data (if available)

[PASTE ACTUAL CONVERSIONS/REVENUE FROM YOUR CRM — OR WRITE "NOT AVAILABLE"]

## Previous Period Data (if available)

[PASTE COMPARISON DATA — OR WRITE "NOT AVAILABLE"]
```

---

## Expected Output

You should get:

1. **Health score** — overall account status
2. **Anomalies** — what changed and why
3. **Hidden losers** — what's wasting money
4. **Hidden winners** — what deserves more
5. **Attribution gaps** — platform vs reality
6. **Action list** — prioritized fixes

---

## Follow-Up Questions to Ask

- "Dig deeper into Campaign X — what's going on?"
- "What would you check first to diagnose the CTR drop?"
- "If I can only make 3 changes today, what should they be?"
- "What data would help you give better recommendations?"
- "Compare this week to last week — what changed?"

---

## Example Output Format

```
## Account Health Score: ⚠️ WARNING

**Overall:** Account is functional but bleeding money in several areas

**Spend efficiency:** 72% of spend is going to campaigns meeting targets
**Trend:** Declining — CPA up 18% over last 14 days
**Immediate concern:** 3 campaigns need attention today

---

## Anomalies Detected

### 1. Campaign "Brand Search" — CTR dropped 40%
**When:** Started 5 days ago
**Impact:** CPC up 35%, wasting ~$400/day

**Possible causes:**
- Competitor bidding on brand terms (check Auction Insights)
- Ad copy no longer resonating (check search terms)
- Quality Score dropped (check keyword QS)

**Investigation:** Pull Auction Insights report, check if new competitor appeared

---

### 2. Campaign "Prospecting - US" — Conversions dropped 60%
**When:** Started 3 days ago
**Impact:** CPA doubled from $45 to $92

**Possible causes:**
- Pixel/tracking issue (conversions too clean of a drop)
- Landing page problem (check page load time)
- Audience exhaustion (check frequency)

**Investigation:** Check Events Manager for pixel fires, test conversion path manually

---

## Hidden Losers

### Campaign "Retargeting - All Visitors"
**Looks like:** $2,100 spend, 28 conversions, $75 CPA
**Reality:** Only 8 conversions in CRM ($262 true CPA)

This campaign is over-reporting by 250%. Platform attribution is inflating results.

**Action:** Reduce budget by 50%, monitor backend conversions

---

### Campaign "Interest - Broad"
**Metrics:** $4,500 spend, $52 CPA (within target)
**Problem:** 62% of spend goes to 2 ad sets with $78 CPA

The average looks fine because one good ad set masks two bad ones.

**Action:** Pause the two underperforming ad sets, reallocate to winner

---

## Hidden Winners

### Campaign "LAL - High Value Customers"
**Performance:** $38 CPA (24% below target), 3.2 ROAS
**Problem:** Limited by $150/day budget, could spend 3x

**Opportunity:** Increase budget to $450/day
**Expected impact:** +$9,000/month spend at strong efficiency

---

### Ad Set "Video - Testimonial"
**Performance:** Best CPA in account ($32)
**Problem:** Only getting 8% of campaign budget

**Action:** Shift budget from underperformers to this ad set

---

## Attribution Check

| Campaign | Platform Conv | Backend Conv | Discrepancy |
| --- | --- | --- | --- |
| Brand Search | 145 | 138 | -5% ✅ |
| Prospecting | 89 | 52 | -42% ❌ |
| Retargeting | 28 | 8 | -71% ❌ |
| LAL High Value | 67 | 71 | +6% ✅ |

**Finding:** Prospecting and Retargeting are significantly over-reporting. Decisions based on platform data alone would be wrong.

---

## Prioritized Action List

### Quick Wins (Today)
1. **Pause 2 underperforming ad sets in "Interest - Broad"**
   - Impact: Save ~$280/day in wasted spend
   
2. **Increase "LAL - High Value" budget to $450/day**
   - Impact: Capture ~$300/day more at below-target CPA

3. **Reduce "Retargeting - All Visitors" budget by 50%**
   - Impact: Stop overspending on over-reported conversions

### This Week
4. **Investigate "Prospecting - US" conversion drop**
   - Check pixel, landing page, test conversion path
   
5. **Pull Auction Insights for "Brand Search"**
   - Identify if competitor entered, adjust strategy

### Strategic (This Month)
6. **Rebuild attribution model**
   - Platform data unreliable for Prospecting/Retargeting
   - Consider incrementality test or MMM

7. **Review full account structure**
   - Consolidate overlapping audiences
   - Simplify campaign structure
```
