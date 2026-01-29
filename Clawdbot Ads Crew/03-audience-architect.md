# 🔍 Audience Architect

Analyzes audience performance, finds saturation issues, and recommends targeting strategy

---

## When to Use

- CPMs are rising
- Frequency above 3
- Planning to scale spend
- Performance declining without creative changes
- Monthly targeting review
- Building new campaigns

---

## Data You Need

Export from Google Ads or Meta Ads Manager (last 7-14 days):

| Field | Required |
| --- | --- |
| Ad set name | ✅ |
| Audience name/type | ✅ |
| Spend | ✅ |
| Reach | ✅ |
| Impressions | ✅ |
| Frequency | ✅ |
| CPM | ✅ |
| Clicks | ✅ |
| Conversions | ✅ |
| CPA | ✅ |
| ROAS | ✅ |

**For Meta specifically:**
- Audience size (if available)
- LAL percentage (1%, 2%, etc.)
- Interest/behavior targeting details

**For Google specifically:**
- Audience type (in-market, custom intent, remarketing)
- Audience segment names

---

## Prompt

```
You are an audience targeting specialist analyzing ad set performance

Your job is to identify targeting issues and recommend audience strategy

## Your Tasks

1. **Efficiency Ranking**
   - Rank all audiences by efficiency (CPA/ROAS relative to spend)
   - Identify best performing audience segments
   - Identify worst performing segments

2. **Saturation Analysis**
   - Flag audiences with frequency > 3
   - Flag audiences with rising CPMs (if trend data available)
   - Estimate how much runway each audience has left
   - Recommend when to pause vs refresh

3. **Overlap Detection**
   - Identify audiences that likely overlap
   - Flag potential auction self-competition
   - Recommend consolidation or exclusions

4. **Scaling Recommendations**
   - Which audiences have room to scale
   - LAL expansion recommendations (1% → 3%, etc.)
   - New audience ideas based on what's working

5. **Audience Structure**
   - Review prospecting vs retargeting balance
   - Check exclusion logic
   - Recommend structure improvements

## Rules

- Consider audience size vs spend (small audiences max out fast)
- Factor in frequency AND CPM together for saturation
- Be specific with LAL recommendations (exact percentages)
- Suggest specific new audiences, not vague ideas
- Flag data limitations if audience details are missing

## My Context

- Business type: [ECOMM / LEAD GEN / SAAS / APP / OTHER]
- Best customers are: [DESCRIBE YOUR ICP]
- Platform: [META / GOOGLE / BOTH]
- Monthly spend: [YOUR BUDGET]
- Current funnel: [DESCRIBE PROSPECTING VS RETARGETING SETUP]

## My Data

[PASTE YOUR AD SET / AUDIENCE DATA HERE]
```

---

## Expected Output

You should get:

1. **Efficiency ranking** — audiences ranked by performance
2. **Saturation alerts** — what's maxed out
3. **Overlap warnings** — where you're competing with yourself
4. **Scaling roadmap** — where to put more money
5. **New audience ideas** — based on patterns

---

## Follow-Up Questions to Ask

- "How should I structure audiences for a $50K scaling push?"
- "Which LAL source is likely driving best performance?"
- "What exclusions should I add?"
- "Give me 5 new interest stacks to test on Meta"
- "How do I reduce overlap between these ad sets?"

---

## Example Output Format

```
## Audience Efficiency Ranking

| Audience | Spend | CPA | ROAS | Freq | CPM | Status |
| --- | --- | --- | --- | --- | --- | --- |
| LAL 1% Purchasers | $3,200 | $38 | 4.2 | 2.1 | $12 | ✅ Scale |
| Interest: Fitness | $2,100 | $52 | 2.8 | 3.8 | $18 | ⚠️ Saturating |
| Broad US 25-45 | $4,500 | $44 | 3.5 | 1.4 | $8 | ✅ Scale |
| LAL 1% Email List | $1,800 | $41 | 3.9 | 4.2 | $22 | ❌ Maxed |
| Retargeting 7d | $900 | $28 | 5.1 | 5.5 | $35 | ⚠️ Cap frequency |

---

## Saturation Alerts

### LAL 1% Email List — MAXED OUT
- Frequency: 4.2 (above 3.0 threshold)
- CPM: $22 (up 40% from $16 two weeks ago)
- Performance declining: CPA up 15% week over week

**Recommendation:** 
- Pause this ad set
- Create LAL 2-3% Email List to expand pool
- Expected CPM drop to ~$14, CPA increase of ~10%

---

### Interest: Fitness — SATURATING
- Frequency: 3.8
- Still performing but declining

**Recommendation:**
- Reduce budget by 30% 
- Test related interests: "Gym," "Workout," "Health & Wellness"
- These have less overlap with current targeting

---

## Overlap Warning

**LAL 1% Purchasers** and **LAL 1% Email List** likely have 40-60% overlap

You're bidding against yourself in the same auctions

**Fix:**
- Consolidate into single ad set, OR
- Add exclusion: Exclude Email List LAL from Purchaser LAL

---

## Scaling Recommendations

### 1. Expand LAL 1% Purchasers → LAL 3%
- Current 1% performing well ($38 CPA)
- Room to scale before saturation
- Expected performance at 3%: $42-48 CPA
- Potential additional spend: $5,000/week

### 2. Scale Broad US 25-45
- Low frequency (1.4), low CPM ($8)
- Large audience pool
- Let algorithm optimize
- Can likely 2x budget without performance drop

### 3. Test new LAL source: High-LTV Customers
- If you have LTV data, create LAL from top 20% customers
- Usually outperforms all-purchaser LALs

---

## New Audiences to Test

Based on LAL Purchasers success, test:

1. **LAL 1% Add-to-Cart** (higher intent than visitors)
2. **LAL 1% Repeat Purchasers** (quality signal)
3. **Interest Stack: [Competitor] + [Product Category]**
4. **In-Market: [Your Category]** (Google)
5. **Custom Intent: [Competitor URLs]** (Google)
```
