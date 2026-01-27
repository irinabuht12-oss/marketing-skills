# Landing Page Health Check

## Purpose
Make sure all landing pages are working. Alert me immediately if any page is down.

## My Landing Pages
- https://example.com/landing-1
- https://example.com/landing-2
- https://example.com/offer
(Add your actual URLs here)

## When to Run
Every 2 hours

## What to Check

For each landing page:

1. **Page loads?**
   - Returns 200 status code
   - Loads in under 5 seconds

2. **Key elements exist?**
   - Headline is visible
   - CTA button is visible
   - Form works (if applicable)

3. **No errors?**
   - No 404, 500, or redirect errors
   - No SSL certificate issues

## Alert Rules

### 🔴 Page Down (Immediate Alert)
- Page returns error (404, 500, etc.)
- Page takes more than 10 seconds to load
- SSL certificate expired

### 🟡 Page Slow (Daily Summary)
- Page takes 5-10 seconds to load
- Some elements missing

## Message Format

```
🔴 LANDING PAGE DOWN

URL: [page URL]
Error: [404 / 500 / timeout / SSL expired]
Time: [when detected]

This page is used in:
• Campaign: [Name] — spending $XX/day
• Campaign: [Name] — spending $XX/day

⚠️ You're paying for clicks to a broken page.

Estimated waste since down: $XX

Fix ASAP or reply "pause campaigns" to stop spend.
```

```
🟡 LANDING PAGE SLOW

URL: [page URL]
Load time: X.X seconds (target: under 5s)

Slow pages hurt conversion rates.
Consider: compress images, faster hosting, fewer scripts.
```

## If I Say "Pause Campaigns"
- Pause all campaigns using that landing page
- Confirm what was paused
- Remind me to unpause when fixed

## If Everything is Fine
Don't message me.
