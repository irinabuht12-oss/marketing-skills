Google

# 20/ Keyword Cannibalization Check — Google

## What it does
Identifies where your own keywords and campaigns are competing against each other in Google Ads auctions. Finds duplicate keywords across campaigns, overlapping match types that trigger the same queries, and ad groups stealing traffic from each other — all of which inflate your CPCs and mess up your data.

## How it works
Claude cross-references your keyword lists across all campaigns and ad groups, maps search term overlap, and identifies where multiple keywords or campaigns are entering the same auctions. It then looks at which one Google is choosing to serve (and whether it's the one you'd want), and calculates the CPC impact of the internal competition.

## Practical example
Your account has "project management software" as an exact match in Campaign A ($28 CPC, 4.2% CVR) and as a broad match in Campaign B ($41 CPC, 2.1% CVR). Campaign B's broad match is cannibalizing 35% of the exact match traffic at nearly double the CPC and half the conversion rate. Claude also finds 23 other keyword pairs with similar overlap issues. Total estimated waste from cannibalization: $2,800/month in inflated CPCs plus conversion data split across campaigns making optimization harder.

## What you get back
- Full list of cannibalizing keyword pairs with the campaigns and ad groups involved
- Which keyword Google is choosing to serve for shared queries and why
- CPC differential between the competing keywords
- Estimated cost of cannibalization in dollars per month
- Specific recommendations: which keywords to pause, which match types to adjust, which campaigns need negative keywords to prevent overlap

## When to use it
- When taking over accounts with years of accumulated keyword sprawl
- After adding new campaigns to ensure they're not stealing traffic from existing ones
- When CPCs rise without competitive explanation
- Quarterly cleanup as part of account hygiene
