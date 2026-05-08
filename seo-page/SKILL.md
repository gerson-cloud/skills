---
name: seo-page
description: >
  Deep single-page SEO analysis covering on-page elements, content quality,
  technical meta tags, schema, images, and performance. Use when user says
  "analyze this page", "check page SEO", "single URL", "check this page",
  "page analysis", or provides a single URL for review.
user-invokable: true
argument-hint: "[url]"
license: MIT
metadata:
  author: AgriciDaniel
  version: "1.9.6"
  category: seo
---

# Single Page Analysis

## Audit Behavior Rules
- Base findings on actual observed page elements whenever possible
- Analyze the actual live page content before generating recommendations
- NEVER provide short summary-style SEO audits
- ALWAYS analyze every section listed in this skill
- NEVER skip sections even if issues are not found
- Provide detailed findings, not short summaries
- Include both strengths and weaknesses
- Use structured formatting exactly as defined below
- When possible, provide examples from the page
- Prioritize actionable SEO recommendations
- If target keyword is provided, optimize analysis around that keyword
- If keyword is not provided, infer the primary keyword from title, headings, URL, and body content
- If a keyword is provided, compare optimization against ranking intent for that keyword
- Avoid generic recommendations unless supported by findings from the analyzed page

## Analysis Priority

Prioritize findings in this order:
1. Indexation & crawlability
2. Search intent alignment
3. Content quality & topical coverage
4. Internal linking
5. Technical SEO
6. Structured data
7. Media optimization
8. Conversion optimization

## What to Analyze

### On-Page SEO
- Title tag: 50-60 characters, includes primary keyword, unique
- Meta description: 150-160 characters, compelling, includes keyword
- H1: exactly one, matches page intent, includes keyword
- H2-H6: logical hierarchy (no skipped levels), descriptive
- URL: short, descriptive, hyphenated, no parameters
- Internal links: sufficient, relevant anchor text, no orphan pages
- External links: to authoritative sources, reasonable count
- Anchor text distribution: branded / exact match / generic balance
- Internal link depth: estimated crawl distance from homepage
- Internal link equity flow: distribution of authority across pages

### Content Quality
- Word count vs page type minimums (see quality-gates.md)
- Readability: Flesch Reading Ease score, grade level
- Keyword density: natural (1-3%), semantic variations present
- Primary keyword: detected or provided input
- Secondary keywords: supporting terms identified
- Semantic keyword clusters: related topic groupings
- Keyword cannibalization: detect competing pages targeting same term
- E-E-A-T signals: author bio, credentials, first-hand experience markers
- Content freshness: publication date, last updated date
- Topical depth vs SERP average: coverage compared to top-ranking pages
- Missing subtopics: topics competitors cover but page does not include
- AI content risk signals: generic or low-depth pattern detection

### Technical Elements
- Canonical tag: present, self-referencing or correct
- Meta robots: index/follow unless intentionally blocked
- Open Graph: og:title, og:description, og:image, og:url
- Twitter Card: twitter:card, twitter:title, twitter:description
- Hreflang: if multi-language, correct implementation

### Schema Markup
- Detect all types (JSON-LD preferred)
- Validate required properties
- Identify missing opportunities
- NEVER recommend HowTo (deprecated) or FAQ (restricted to gov/health)

### Images
- Alt text: present, descriptive, includes keywords where natural
- File size: flag >200KB (warning), >500KB (critical)
- Format: recommend WebP/AVIF over JPEG/PNG
- Dimensions: width/height set for CLS prevention
- Lazy loading: loading="lazy" on below-fold images

### Core Web Vitals (reference only, not measurable from HTML alone)
- Flag potential LCP issues (huge hero images, render-blocking resources)
- Flag potential INP issues (heavy JS, no async/defer)
- Flag potential CLS issues (missing image dimensions, injected content)

### Internal Linking Intelligence (NEW)
- Link depth from homepage (crawl accessibility)
- Contextual vs navigational link ratio
- Anchor text quality distribution
- Internal link equity flow (authority distribution analysis)
- Orphan page risk detection

### Competitor & SERP Gap Analysis (NEW)
- Top 3 SERP competitor comparison
- Content gap summary vs competitors
- Missing sections vs ranking pages
- SERP feature opportunities (snippets, rich results, etc.)
- Differentiation opportunities for ranking improvement

## Response Depth Requirements
- ALWAYS provide optimized Title Tag, Meta Description, and H1 recommendations
- Every scoring category MUST include a numeric score
- Scores should reflect severity and quantity of issues found
- Minimum audit depth: medium-detail
- Include explanations for why each issue matters
- Include recommended fixes for every major issue
- Include SEO impact estimation when possible
- Avoid generic SEO advice unless directly relevant to the page
- Include direct examples from the page when possible
- Quote titles, headings, or metadata when relevant
- Prioritize issues based on estimated SEO impact and crawl/indexation importance

### Conversion SEO
- CTA visibility and clarity
- Above-the-fold messaging alignment
- Trust signals (reviews, guarantees, proof elements)
- UX friction impacting conversions
- Search intent to conversion alignment

## Required Output Format

### Page Score Card

Overall Score: XX/100

- On-Page SEO: XX/100
- Content Quality: XX/100
- Technical: XX/100
- Schema: XX/100
- Images: XX/100
- SERP Alignment: XX/100
- Conversion SEO: XX/100

---

### Strengths
- List what the page already does well

---

### Critical Issues
- Highest priority SEO problems

---

### High Priority Improvements
- Important ranking improvements

---

### Medium Priority Improvements
- Secondary optimizations

---

### Low Priority Improvements
- Minor enhancements

---

### SERP & Competitor Analysis
- Compare page structure vs top-ranking competitors
- Identify missing sections or content gaps
- Identify SERP differentiation opportunities

---

### Recommended Metadata

Title Tag:
[optimized version]

Meta Description:
[optimized version]

H1:
[optimized version]

---

### Schema Recommendations
- Recommended structured data opportunities
- Include JSON-LD examples when applicable

---

### Internal Linking Recommendations
- Suggested parent collections
- Suggested related collections
- Suggested anchor text opportunities

---

### Final SEO Summary
- Summarize biggest opportunities for ranking improvements |
