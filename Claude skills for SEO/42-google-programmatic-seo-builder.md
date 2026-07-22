---
name: programmatic-seo-builder
description: Create scalable programmatic SEO page templates with title patterns, internal linking logic, schema markup, and thin content avoidance strategies. Use when given a niche and data source to build page templates, establishing programmatic SEO structure, or scaling content production with templates.
metadata:
  platform: Google
---

# Programmatic SEO Builder

Design scalable page templates that rank without appearing thin or auto-generated.

## Process

1. **Define page type** - Location, comparison, directory, definition, converter
2. **Create title pattern** - Keyword + modifier formula
3. **Design page template** - Sections, variable content, unique elements
4. **Plan internal linking** - Hub and spoke model
5. **Specify schema markup** - Appropriate JSON-LD
6. **Add uniqueness requirements** - Avoid thin content penalties

## Common Programmatic Page Types

| Type | URL Pattern | Example |
|------|-------------|---------|
| Location | /[service]-in-[city] | /plumber-in-austin |
| Comparison | /[product-a]-vs-[product-b] | /notion-vs-airtable |
| Directory | /best-[category]-for-[use-case] | /best-crm-for-startups |
| Definition | /what-is-[term] | /what-is-seo |
| Converter | /[x]-to-[y]-converter | /usd-to-eur-converter |

## Title Tag Formulas

| Pattern | Template | Example |
|---------|----------|---------|
| Local service | [Service] in [City] - [Brand] | "Personal Injury Lawyer in Phoenix - Smith Law" |
| Best + Year | Best [Category] [Year] - [Brand] | "Best CRM Software 2025 - TechReview" |
| Comparison | [Product A] vs [Product B]: [Year] Comparison | "Notion vs Airtable: 2025 Comparison" |
| How to | How to [Action] + [Modifier] | "How to Convert PDF to Word Free" |
| Definition | What is [Term]? Definition + [Examples/Guide] | "What is SEO? Definition + Complete Guide" |

## Internal Linking: Hub & Spoke Model

```
Hub Page: "Marketing Tools" (comprehensive guide)
    │
    ├── Spoke: "Email Marketing Tools" 
    │   └── Links to: Hub, SEO Tools, Social Tools
    │
    ├── Spoke: "SEO Tools"
    │   └── Links to: Hub, Email Tools, Analytics Tools
    │
    ├── Spoke: "Social Media Tools"
    │   └── Links to: Hub, Email Tools, Content Tools
    │
    └── Each spoke links to:
        • Parent hub (always)
        • 2-3 related spokes (contextually)
        • Relevant comparison pages
```

## Schema Markup Requirements

| Page Type | Schema | Required Properties |
|-----------|--------|---------------------|
| Location | LocalBusiness | name, address, telephone, openingHours |
| Comparison | Product (multiple) | name, description, review, aggregateRating |
| Directory | ItemList | itemListElement[], numberOfItems |
| Definition | FAQPage or Article | mainEntity (FAQ) or headline, author (Article) |
| Converter | WebApplication | name, applicationCategory, offers |

**Always include**: BreadcrumbList for navigation structure

## Thin Content Avoidance

### Minimum Requirements
- **Word count**: 300-500 words unique content per page
- **Unique sections**: 2-3 sections beyond templated structure
- **Intent match**: Specific answer to the search query
- **Variable depth**: Context added, not just name-swapping

### What Makes Pages Thin (Avoid)
- Only swapping city/product names in identical text
- No unique insights or local/specific information
- Template visible through multiple pages
- No added value beyond what database provides

### What Makes Pages Valuable (Do)
- Unique introductions per page variant
- Specific data points (local stats, product specs)
- Custom recommendations based on variant
- User-generated content where appropriate
- FAQ section with variant-specific questions

## Output Format

```
## Programmatic SEO Specification

### Page Type Overview
- **Type**: [Location/Comparison/Directory/etc.]
- **URL Pattern**: /[pattern]
- **Target Keywords**: [X] pages targeting [keyword pattern]
- **Data Source**: [Where variable data comes from]

### Title Tag Template
```
[Template with variables]
```
**Examples**:
- [Example 1]
- [Example 2]

### Meta Description Template
```
[Template with variables]
```

### Page Template Structure

#### Section 1: [Header]
- **Content type**: [Static/Variable/Mixed]
- **Requirements**: [Specifications]

#### Section 2: [Header]
...

### Internal Linking Rules
- **Hub page**: [URL]
- **Link to hub**: [Where in template]
- **Related spokes**: [Logic for selection]
- **Contextual links**: [Placement rules]

### Schema Markup (JSON-LD)
```json
{
  "@context": "https://schema.org",
  "@type": "[Type]",
  ...
}
```

### Uniqueness Requirements
- [ ] [Requirement 1]
- [ ] [Requirement 2]
- [ ] [Requirement 3]

### Thin Content Safeguards
- Minimum word count: [X]
- Required unique sections: [List]
- Variable content depth: [Specifications]

### Example Page
**URL**: [Example URL]
**Title**: [Example title]
**H1**: [Example H1]
[Brief content outline]
```

## Example

**Input**: "Build programmatic SEO template for 'best [software] for [industry]' pages. Data source is a database of 50 software tools and 20 industries."

**Output**:
```
## Programmatic SEO Specification

### Page Type Overview
- **Type**: Directory/Recommendation
- **URL Pattern**: /best-[software-category]-for-[industry]
- **Target Keywords**: 1,000 pages (50 tools × 20 industries)
- **Data Source**: Software database + industry requirements mapping

### Title Tag Template
```
Best [Software Category] for [Industry] ([Year]) | [Brand]
```
**Examples**:
- Best CRM Software for Real Estate (2025) | TechReview
- Best Project Management Tools for Agencies (2025) | TechReview

### Meta Description Template
```
Discover the best [software] for [industry] in [year]. Compare top [X] options with pricing, features, and expert recommendations for [industry] professionals.
```

### Page Template Structure

#### Section 1: Introduction (Variable)
- **Content type**: Variable - industry-specific
- **Requirements**: 100-150 words addressing why [industry] needs specialized [software], unique challenges

#### Section 2: Quick Picks Summary (Variable)
- **Content type**: Variable based on industry fit scores
- **Requirements**: Top 3 picks with one-line reasoning, links to full reviews

#### Section 3: Detailed Recommendations (Variable)
- **Content type**: Mixed - template structure, variable content
- **Requirements**: 
  - 5-7 tools per page
  - Each tool: 150-200 words
  - Industry-specific use case for each
  - Pricing with industry discount notes
  - Pros/cons relevant to industry workflow

#### Section 4: How We Evaluated (Static)
- **Content type**: Static
- **Requirements**: Methodology transparency, criteria list

#### Section 5: Industry-Specific Buying Guide (Variable)
- **Content type**: Variable
- **Requirements**: 200-300 words on considerations specific to [industry]

#### Section 6: FAQ (Variable)
- **Content type**: Variable - 5 questions per page
- **Requirements**: Industry + software specific questions

### Internal Linking Rules
- **Hub page**: /best-software-tools/
- **Link to hub**: In introduction and footer
- **Related spokes**: Link to same-industry different-software and same-software different-industry
- **Contextual links**: Individual tool review pages

### Schema Markup
```json
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "name": "Best [Software] for [Industry]",
  "numberOfItems": 7,
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "Product",
        "name": "[Tool Name]",
        "description": "[Industry-specific description]"
      }
    }
  ]
}
```

### Uniqueness Requirements
- [ ] Industry-specific introduction (not just name swap)
- [ ] Custom tool ordering based on industry fit algorithm
- [ ] Industry-specific pros/cons for each tool
- [ ] Unique FAQ questions per industry
- [ ] Buying guide section tailored to industry workflow

### Thin Content Safeguards
- Minimum word count: 1,500 words
- Required unique sections: Introduction, Buying Guide, FAQ
- Each tool must have industry-specific recommendation paragraph
```

## Guidelines

- Always include thin content safeguards
- Schema must match page type
- Internal linking logic must be systematic
- Provide actual template structure, not just concepts
- If data source unclear, ask before proceeding
- Flag if proposed scale risks quality issues
