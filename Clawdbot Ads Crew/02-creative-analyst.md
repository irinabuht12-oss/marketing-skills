# 🎨 Creative Analyst

Analyzes ad creative performance and explains why ads work or fail

---

## When to Use

- Performance is dropping
- Planning creative refresh
- Testing new ad concepts
- Scaling winning campaigns
- Monthly creative reviews
- High frequency alerts

---

## Data You Need

Export from Google Ads or Meta Ads Manager (last 7-14 days):

| Field | Required |
| --- | --- |
| Ad name | ✅ |
| Spend | ✅ |
| Impressions | ✅ |
| Clicks | ✅ |
| CTR | ✅ |
| CPC | ✅ |
| Conversions | ✅ |
| CPA | ✅ |
| ROAS | ✅ |
| Frequency | ✅ |
| Video views / ThruPlays | Optional |
| Hook rate (3s views) | Optional |

**Also helpful:**
- Ad copy / primary text
- Headlines
- Descriptions
- Creative format (static/video/carousel)
- Creative angle or theme (if you track this)

---

## Prompt

```
You are a creative strategist analyzing ad performance data

Your job is to explain WHY ads perform the way they do — not just describe metrics

## Your Tasks

1. **Top Performers Analysis**
   - Identify top 3-5 performing ads
   - Explain WHY each one works (hook, angle, format, CTA, emotion)
   - Identify patterns across winners

2. **Underperformers Analysis**
   - Identify bottom 3-5 ads
   - Explain WHY each one fails
   - Identify patterns across losers

3. **Creative Fatigue Check**
   - Flag ads with frequency > 3 and declining CTR
   - Estimate remaining lifespan for fatiguing ads
   - Recommend refresh or pause

4. **Format Analysis**
   - Compare performance by format (static vs video vs carousel)
   - Recommend which formats to prioritize

5. **Action List**
   - Kill list (pause immediately)
   - Scale list (increase budget)
   - Iterate list (create variations of these)
   - New angles to test (based on what's working)

## Rules

- Don't just describe metrics — explain the creative reason behind performance
- Be specific: "The hook works because..." not "The hook is good"
- Reference actual ad copy/creative details when analyzing
- If ad copy is not provided, analyze based on naming patterns and metrics
- Suggest specific creative directions, not vague ideas

## My Context

- Product/Service: [WHAT YOU'RE SELLING]
- Target audience: [WHO YOU'RE TARGETING]
- Platform: [META / GOOGLE / BOTH]
- Main goal: [CONVERSIONS / LEADS / SALES / AWARENESS]

## My Ad Data

[PASTE YOUR AD-LEVEL DATA HERE]

## Ad Copy (if available)

[PASTE AD COPY, HEADLINES, DESCRIPTIONS — OR WRITE "NOT AVAILABLE"]
```

---

## Expected Output

You should get:

1. **Winners breakdown** — top ads with creative analysis
2. **Losers breakdown** — failing ads with reasons
3. **Fatigue alerts** — ads running out of steam
4. **Format insights** — what's working best
5. **Action list** — kill/scale/iterate/test

---

## Follow-Up Questions to Ask

- "What hook styles are working best?"
- "Give me 5 specific headline variations for my top performer"
- "Why do you think video is outperforming static?"
- "What angles should I test next based on this data?"
- "If I can only make 3 new ads this week, what should they be?"

---

## Example Output Format

```
## Top Performers

### 1. "Summer Sale - Video - Testimonial"
**Performance:** $45 CPA (10% below target), 2.1% CTR, 1.8 frequency

**Why it works:**
- Opens with customer result (social proof hook)
- Shows product in use within first 3 seconds
- Clear price anchor ("was $99, now $49")
- Urgency CTA ("Ends Sunday")

**Pattern:** Testimonial + price anchor + urgency

---

### 2. "Problem-Solution - Static - Before/After"
**Performance:** $48 CPA (4% below target), 1.8% CTR, 2.2 frequency

**Why it works:**
- Leads with pain point audience recognizes
- Visual transformation creates curiosity
- Simple, scannable copy
- Single clear CTA

**Pattern:** Problem-agitate-solution with visual proof

---

## Creative Fatigue Alerts

| Ad | Frequency | CTR Trend | Recommendation |
| --- | --- | --- | --- |
| Brand Video V1 | 4.2 | -35% last 7d | Pause, create V2 |
| Static Promo 3 | 3.8 | -20% last 7d | 1 week left, prep replacement |

---

## Action List

**Kill (pause now):**
- "Generic Brand Ad" — 2x target CPA, no improvement
- "Long Form Video" — 0.4% CTR, not resonating

**Scale (increase budget):**
- "Summer Sale - Video - Testimonial"
- "Problem-Solution - Static"

**Iterate (make variations):**
- "Testimonial" format — test different customers
- "Before/After" — test different transformations

**New angles to test:**
1. UGC-style unboxing (based on testimonial success)
2. Comparison to alternative solutions
3. "Day in the life" showing product use
```
