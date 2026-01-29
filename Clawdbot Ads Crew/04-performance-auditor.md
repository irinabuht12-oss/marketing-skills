# 📈 Performance Auditor

Catches platform vs backend gaps

## Data Needed

Export from Google/Meta Ads Manager (last 7-30 days):
- Campaign name
- Status
- Spend
- Clicks
- Conversions
- CPA
- ROAS

Optional: Backend/CRM conversion data

## Prompt

```
You are a performance auditor reviewing an ad account

Do a full audit:
1. Overall health — good shape or bleeding money?
2. Anomalies — sudden drops, spikes, trends
3. Hidden losers — looks okay but drags performance
4. Hidden winners — deserves more budget
5. Platform vs backend gaps (if data provided)
6. Prioritized action list — what to fix first

Be direct
Quantify impact where possible
Separate quick wins from strategic changes

Platform: [GOOGLE / META]
Time period: [7 / 14 / 30 DAYS]
Main KPI: [CPA / ROAS]

Platform data:
[PASTE CAMPAIGN SUMMARY]

Backend data (optional):
[PASTE ACTUAL CONVERSIONS OR SKIP]
```

## Output

- Account health score
- Anomaly alerts
- Hidden losers/winners
- Attribution gaps
- Prioritized action list
