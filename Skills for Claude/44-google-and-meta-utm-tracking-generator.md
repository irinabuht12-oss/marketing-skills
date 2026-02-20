---
name: utm-tracking-generator
description: Generate consistent UTM parameters, GA4 event naming, and conversion tracking specs following taxonomy best practices. Use when describing campaign structure, requesting UTM links, needing GA4 event names, or wanting to standardize tracking nomenclature across marketing channels.
platform: Google and Meta
---

# UTM & Tracking Generator

Create standardized tracking parameters for consistent marketing attribution.

## Process

1. **Understand campaign context** - Channels, goals, audience, offers
2. **Apply naming taxonomy** - Consistent, lowercase, documented
3. **Generate UTM strings** - Complete parameter sets
4. **Create GA4 event specs** - Compliant naming
5. **Provide implementation guidance** - Platform-specific instructions

## UTM Parameter Taxonomy

| Parameter | Purpose | Example Values |
|-----------|---------|----------------|
| utm_source | Traffic source platform | google, facebook, linkedin, newsletter |
| utm_medium | Marketing channel type | cpc, paid-social, email, display, organic |
| utm_campaign | Campaign identifier | spring_sale-us-2024-prospecting |
| utm_term | Paid keywords (optional) | running_shoes, [brand_name] |
| utm_content | Content variant (optional) | hero_cta, sidebar_banner, email_v2 |

## Naming Convention Rules

1. **Always lowercase** - UTMs are case-sensitive (google ≠ Google)
2. **No spaces** - Use hyphens (-) or underscores (_)
3. **Consistent separators** - Pick one style for organization
4. **Descriptive but concise** - Balance clarity with length
5. **Document everything** - Maintain shared naming guide

## Campaign Naming Structure

```
[product/goal]-[geography]-[date]-[audience]-[offer]

Examples:
- shoes-us-q1_2024-running_enthusiasts-20off
- saas-global-jan2024-smb_trial-free_demo
- ebook-uk-2024_q2-marketers-lead_magnet
```

## Platform-Specific Templates

### Google Ads
```
utm_source=google&utm_medium=cpc&utm_campaign={campaign_name}&utm_term={keyword}&utm_content={creative}
```

### Meta Ads (Dynamic Parameters)
```
utm_source={{site_source_name}}&utm_medium=paid-social&utm_campaign={{campaign.name}}&utm_content={{adset.name}}&utm_term={{ad.name}}
```

### LinkedIn Ads
```
utm_source=linkedin&utm_medium=paid-social&utm_campaign=[campaign_name]&utm_content=[ad_name]
```

### Email Marketing
```
utm_source=klaviyo&utm_medium=email&utm_campaign=[flow_name]-[email_position]&utm_content=[variant]
```

## GA4 Event Naming Rules

| Rule | Requirement | Example |
|------|-------------|---------|
| Start with letter | No numbers or symbols first | ✅ page_view ❌ 1st_click |
| Allowed characters | Letters, numbers, underscores only | ✅ add_to_cart ❌ add-to-cart |
| Max length | 40 characters | Keep concise |
| No reserved prefixes | Avoid ga_, google_, firebase_ | Use custom prefix |
| Case | Use snake_case | form_submit, button_click |

### Standard Event Names (Use These)
```
page_view
scroll_depth
form_submit
button_click
video_play
video_complete
file_download
outbound_click
add_to_cart
begin_checkout
purchase
sign_up
login
search
```

## Output Format

```
## Tracking Specification

### Campaign Overview
- **Campaign Name**: [Name]
- **Channels**: [List]
- **Goal**: [Conversion objective]

### UTM Parameters

#### [Channel 1]
| Parameter | Value |
|-----------|-------|
| utm_source | |
| utm_medium | |
| utm_campaign | |
| utm_term | |
| utm_content | |

**Full URL**: `https://example.com?utm_source=...`

#### [Channel 2]
...

### GA4 Event Specifications

| Event | Trigger | Parameters |
|-------|---------|------------|
| [event_name] | [When fired] | [Key params] |

### Implementation Notes
- [Platform-specific guidance]
- [Testing recommendations]

### Naming Convention Reference
- Separator: [hyphen/underscore]
- Date format: [YYYY_QN or MMYYYY]
- Geography codes: [us, uk, global]
```

## Example

**Input**: "I need UTM tracking for a spring sale campaign running on Google Ads, Facebook, and email for US customers, promoting 20% off shoes."

**Output**:
```
## Tracking Specification

### Campaign Overview
- **Campaign Name**: shoes-us-spring2024-allcust-20off
- **Channels**: Google Ads, Meta Ads, Email
- **Goal**: Purchase conversions

### UTM Parameters

#### Google Ads
| Parameter | Value |
|-----------|-------|
| utm_source | google |
| utm_medium | cpc |
| utm_campaign | shoes-us-spring2024-allcust-20off |
| utm_term | {keyword} |
| utm_content | {creative} |

**Full URL**: 
`https://yoursite.com/shoes?utm_source=google&utm_medium=cpc&utm_campaign=shoes-us-spring2024-allcust-20off&utm_term={keyword}&utm_content={creative}`

#### Meta Ads
| Parameter | Value |
|-----------|-------|
| utm_source | facebook |
| utm_medium | paid-social |
| utm_campaign | shoes-us-spring2024-allcust-20off |
| utm_content | {{adset.name}} |
| utm_term | {{ad.name}} |

**Full URL**:
`https://yoursite.com/shoes?utm_source=facebook&utm_medium=paid-social&utm_campaign=shoes-us-spring2024-allcust-20off&utm_content={{adset.name}}&utm_term={{ad.name}}`

#### Email (Klaviyo)
| Parameter | Value |
|-----------|-------|
| utm_source | klaviyo |
| utm_medium | email |
| utm_campaign | shoes-us-spring2024-allcust-20off |
| utm_content | promo_blast_1 |

**Full URL**:
`https://yoursite.com/shoes?utm_source=klaviyo&utm_medium=email&utm_campaign=shoes-us-spring2024-allcust-20off&utm_content=promo_blast_1`

### GA4 Events to Track
| Event | Trigger | Parameters |
|-------|---------|------------|
| view_promotion | Promo banner viewed | promotion_id, promotion_name |
| select_promotion | Promo clicked | promotion_id, promotion_name |
| add_to_cart | Shoe added | item_id, item_name, price, discount |
| purchase | Order completed | transaction_id, value, items[] |

### Implementation Notes
- Test all UTMs with Google's Campaign URL Builder before launch
- Verify events in GA4 DebugView
- Document naming convention in shared spreadsheet
```

## Guidelines

- Always use lowercase for all UTM values
- Never include PII in tracking parameters
- Test URLs before distributing
- Provide platform-specific dynamic parameter syntax
- Include testing/validation recommendations
