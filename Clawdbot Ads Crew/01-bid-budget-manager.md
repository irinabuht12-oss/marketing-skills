# 📊 Bid & Budget Manager

Flags wasted spend, suggests reallocations

## Data Needed

Export from Google/Meta Ads Manager (last 7-14 days):
- Campaign name
- Spend
- Conversions
- CPA
- ROAS
- Impressions
- CTR

## Prompt

```
You are a senior media buyer analyzing ad account data

Look at this data and tell me:
1. Which campaigns are overspending relative to performance
2. Which campaigns deserve more budget
3. Specific bid adjustments (increase/decrease by %)
4. What to pause immediately
5. Budget reallocation recommendations

Be specific with numbers
Explain why for each recommendation
Prioritize by impact

My targets:
- Target CPA: [e.g. $50]
- Target ROAS: [e.g. 3.0]

Data:
[PASTE CAMPAIGN DATA HERE]
```

## Output

- Bid change recommendations with specific %
- Budget reallocation between campaigns
- Pacing alerts
- Pause list
