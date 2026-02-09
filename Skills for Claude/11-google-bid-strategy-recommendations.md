Google

# 11/ Bid Strategy Recommendations — Google

## What it does
Analyzes your campaign history, conversion volume, CPA targets, and auction dynamics, then recommends the right bid strategy for each campaign — manual CPC, target CPA, target ROAS, maximize conversions, or maximize conversion value. Not a blanket recommendation, but campaign-by-campaign based on the data.

## How it works
Claude evaluates each campaign's conversion volume (whether it has enough data for automated bidding to work), CPA consistency (high variance means automated strategies will struggle), budget headroom, and competitive landscape. It also looks at your current strategy's performance trend to determine if switching would likely improve or hurt results.

## Practical example
You have 8 search campaigns all running maximize conversions. Claude identifies that 3 of them have fewer than 15 conversions per month — not enough for the algorithm to optimize effectively. It recommends switching those to manual CPC with specific bid suggestions. For the 2 campaigns with 100+ monthly conversions, it recommends target CPA set at $42 (10% above current CPA to give the algorithm room). The remaining 3 are performing well on current strategy and should stay as-is.

## What you get back
- Campaign-by-campaign bid strategy recommendation with reasoning
- Minimum conversion thresholds each campaign needs for automated bidding
- Recommended target CPA or ROAS values based on historical data
- Risk assessment for each strategy change (expected short-term performance dip during learning)
- Transition plan with timing recommendations to avoid disrupting active campaigns

## When to use it
- When onboarding new accounts to set up strategies correctly from the start
- Quarterly bid strategy reviews to catch campaigns that have outgrown or underperform their current strategy
- When conversion volume changes significantly (up or down)
- Before scaling campaigns, because the right strategy at $5K/month might be wrong at $25K/month
