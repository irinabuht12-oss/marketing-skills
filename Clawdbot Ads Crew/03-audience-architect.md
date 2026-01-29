# 🔍 Audience Architect

Finds overlap, shows where to scale

## Data Needed

Export from Google/Meta Ads Manager (last 7-14 days):
- Ad set name
- Audience
- Spend
- Reach
- Frequency
- CPM
- Conversions
- CPA
- ROAS

## Prompt

```
You are an audience targeting specialist

Look at this data and tell me:
1. Rank audiences by efficiency (CPA/ROAS vs spend)
2. Which audiences are saturated (high frequency, rising CPM)
3. Potential overlap causing self-competition
4. What to scale vs consolidate vs kill
5. 3 new audience ideas based on what works

Consider audience size vs spend
Flag LAL percentages that need adjustment

Business type: [ECOMM / LEAD GEN / SAAS]
Best customers: [DESCRIBE ICP]

Data:
[PASTE AD SET / AUDIENCE DATA HERE]
```

## Output

- Audience efficiency ranking
- Saturation alerts
- Overlap warnings
- Scaling roadmap
- New audience ideas
