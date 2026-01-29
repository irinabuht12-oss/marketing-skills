# 📊 Bid & Budget Manager

Analyzes spend efficiency and recommends bid/budget adjustments

---

## When to Use

- Weekly budget reviews
- Before scaling campaigns
- When CPA/ROAS targets are off
- After significant performance changes
- Monthly budget planning

---

## Data You Need

Export from Google Ads or Meta Ads Manager (last 7-14 days):

| Field | Required |
| --- | --- |
| Campaign name | ✅ |
| Spend | ✅ |
| Conversions | ✅ |
| CPA | ✅ |
| ROAS | ✅ |
| Impressions | ✅ |
| Clicks | ✅ |
| CTR | ✅ |
| CPM | Optional |
| Impression Share | Optional (Google) |
| Frequency | Optional (Meta) |

Export as CSV or copy-paste table directly

---

## Prompt

```
You are a senior media buyer analyzing campaign performance data

Your job is to analyze this data and provide specific, actionable recommendations

## Your Tasks

1. **Efficiency Analysis**
   - Rank campaigns by efficiency (CPA or ROAS relative to spend)
   - Identify which campaigns are overspending relative to results
   - Identify which campaigns deserve more budget

2. **Bid Recommendations**
   - Recommend specific bid adjustments (example: "Increase bid by 15%")
   - Explain the reasoning for each adjustment
   - Flag campaigns where bid strategy might need changing

3. **Budget Reallocation**
   - Suggest how to redistribute budget across campaigns
   - Show exact amounts to move (example: "Move $500 from Campaign A to Campaign B")
   - Prioritize by expected impact

4. **Pause List**
   - List campaigns that should be paused immediately
   - Explain why each should be paused
   - Estimate wasted spend if not paused

5. **Pacing Check**
   - Flag campaigns that will over-deliver or under-deliver
   - Recommend pacing adjustments

## Rules

- Be specific with numbers, not vague
- Every recommendation needs a "why"
- Prioritize recommendations by impact (highest impact first)
- If data is insufficient for a recommendation, say so
- Use tables for clarity

## My Targets

- Target CPA: [ENTER YOUR TARGET CPA]
- Target ROAS: [ENTER YOUR TARGET ROAS]
- Monthly budget: [ENTER TOTAL BUDGET]
- Platform: [GOOGLE / META / BOTH]

## My Data

[PASTE YOUR CAMPAIGN DATA HERE]
```

---

## Expected Output

You should get:

1. **Efficiency ranking table** — all campaigns ranked by performance
2. **Bid adjustments** — specific % changes with reasoning
3. **Budget reallocation plan** — exact amounts to move
4. **Pause list** — what to stop immediately
5. **Pacing alerts** — delivery issues to fix

---

## Follow-Up Questions to Ask

After initial analysis, dig deeper:

- "What if I need to cut total budget by 20%?"
- "Which campaigns have the most room to scale?"
- "Why is Campaign X underperforming vs Campaign Y?"
- "What bid strategy would you recommend for Campaign X?"
- "Show me the math behind your top recommendation"

---

## Example Output Format

The agent should return something like:

```
## Efficiency Ranking

| Campaign | Spend | Conv | CPA | vs Target | Action |
| --- | --- | --- | --- | --- | --- |
| Campaign A | $2,500 | 62 | $40 | -20% ✅ | Scale |
| Campaign B | $1,800 | 30 | $60 | +20% ⚠️ | Optimize |
| Campaign C | $3,200 | 40 | $80 | +60% ❌ | Pause |

## Recommended Actions

**1. Pause Campaign C immediately**
- Current CPA ($80) is 60% above target ($50)
- Wasting ~$1,200/week at current performance
- No improvement trend in last 7 days

**2. Increase Campaign A budget by 40%**
- Best performing campaign (CPA $40, 20% below target)
- Currently limited by budget
- Move $1,000 from Campaign C

...
```
