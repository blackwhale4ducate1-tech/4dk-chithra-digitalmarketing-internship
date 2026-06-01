# 📈 B2B SaaS SEO Content Audit Strategy & Playbook

<div align="center">

![SEO Audit](https://img.shields.io/badge/SEO-Audit_&_Strategy-4285F4?style=for-the-badge&logo=google-search-console&logoColor=white)
![Ahrefs](https://img.shields.io/badge/Ahrefs-Backlinks-orange?style=for-the-badge&logo=brandfolder&logoColor=white)
![SEMrush](https://img.shields.io/badge/SEMrush-Keywords-red?style=for-the-badge&logo=semrush&logoColor=white)
![Screaming Frog](https://img.shields.io/badge/Screaming_Frog-Crawler-3ECF8E?style=for-the-badge&logo=deno&logoColor=white)

**A comprehensive, production-grade SEO Content Audit playbook for B2B SaaS companies. Bridges technical SEO, on-page optimization, backlink authority, and content quality with a weighted 0-100 scoring system and a 30-day execution framework.**

[Overview](#1-purpose--business-context) • [Scoring Rubric](#3-mathematical-0-100-page-scoring-rubric) • [Checklists](#4-audit-checklists) • [SOPs](#5-screaming-frog-crawl-configurations) • [Setup](#6-monthly-audit-process-30-day-timeline)

</div>

---

## 📋 Table of Contents

1. [Purpose & Business Context](#1-purpose--business-context)
2. [Folder Structure & Deliverables](#2-folder-structure--deliverables)
3. [Mathematical 0-100 Page Scoring Rubric](#3-mathematical-0-100-page-scoring-rubric)
4. [Audit Checklists](#4-audit-checklists)
5. [Screaming Frog Crawl Configurations](#5-screaming-frog-crawl-configurations)
6. [Monthly Audit Process (30-Day Timeline)](#6-monthly-audit-process-30-day-timeline)
7. [Quick Win Playbook (Optimizations in Under 1 Hour)](#7-quick-win-playbook-optimizations-in-under-1-hour)
8. [Recommended Tool Stack & Budgeting](#8-recommended-tool-stack--budgeting)
9. [RACI Matrix & Team Responsibilities](#9-raci-matrix--team-responsibilities)
10. [Page Audit Tracking Sheet Structure](#10-page-audit-tracking-sheet-structure)
11. [Keyword Gap Analysis Framework](#11-keyword-gap-analysis-framework)
12. [KPIs, Dashboards & GA4 Reporting Models](#12-kpis-dashboards--ga4-reporting-models)
13. [Prioritization Matrix (Impact vs Effort)](#13-prioritization-matrix-impact-vs-effort)
14. [Competitor Comparison Strategy](#14-competitor-comparison-strategy)
15. [Verification Plan](#15-verification-plan)
16. [Project Changelog](#16-project-changelog)
17. [Contributing Guidelines](#17-contributing-guidelines)

---

## 1. Purpose & Business Context

This playbook details the SEO content auditing framework designed to optimize organic acquisition funnels for **B2B SaaS companies**. In B2B SaaS, driving organic traffic is only the first step. The primary goal of this framework is to convert organic searchers into qualified leads (e.g. product signups, trial starts, and demo requests).

This framework bridges the gaps between four critical SEO pillars:
- **Technical Site Health:** Enforcing crawler access, resolving redirect loops, and optimizing Core Web Vitals (CWVs).
- **On-Page Optimization:** Structuring HTML markup, optimizing headings, and targeting search intent.
- **Content Quality:** Improving readability, resolving duplicate content issues, and ensuring thin content is updated.
- **Backlink Authority:** Analyzing domain authority (DA) and maintaining a healthy internal link profile.

---

## 2. Folder Structure & Deliverables

The workspace is organized into folders that correspond to each phase of the audit process:

```text
seo-content-audit-strategy/
├── README.md                           # Main playbook operations manual
├── checklists/
│   ├── TECHNICAL_SEO.md                # Crawlability, indexing, and speed criteria
│   ├── ON_PAGE_SEO.md                  # Title tags, meta descriptions, and heading hierarchies
│   ├── CONTENT_QUALITY.md              # Duplicate checks, thin content, and readability
│   └── BACKLINK_PROFILE.md             # Anchor texts, broken links, and toxic backlink checks
├── kpis/
│   ├── KPI_DASHBOARD.md                # Reporting templates for organic dashboards
│   └── BASELINE_TEMPLATE.csv           # Baseline logs to record performance before and after audits
├── process/
│   ├── MONTHLY_AUDIT_PROCESS.md        # 30-day step-by-step auditing workflows
│   └── QUICK_WIN_PLAYBOOK.md           # 15 easy optimizations completed in under 1 hour
├── strategy/
│   ├── AUDIT_OVERVIEW.md               # Scope and business alignment briefs
│   ├── SEO_SCORING_RUBRIC.md           # Weighted 0-100 scoring formulas
│   └── PRIORITY_MATRIX.md              # Effort vs Impact scoring maps
├── templates/
│   ├── AUDIT_REPORT_TEMPLATE.md        # Presentable executive summaries template
│   ├── PAGE_AUDIT_SHEET.csv            # Page-level audit tracker spreadsheet
│   └── KEYWORD_GAP_ANALYSIS.csv        # Competitor keyword ranking spreadsheet
└── tools/
    ├── TOOLS_GUIDE.md                  # Settings and SOPs for auditing tools
    └── SCREAMING_FROG_EXPORT.md        # Configuration files for Screaming Frog crawls
```

---

## 3. Mathematical 0-100 Page Scoring Rubric

To evaluate page performance objectively, the audit uses a weighted scoring formula:

$$\text{Page Score} = (T \times 0.25) + (O \times 0.25) + (Q \times 0.30) + (A \times 0.20)$$

### Weights Breakdown

| Variable | Audit Category | Metric Target | Weight |
|---|---|---|---|
| **$T$** | Technical Health | Core Web Vitals passed, indexing validated, no crawl errors | **25%** |
| **$O$** | On-Page Structure | Title tag, meta description, and heading hierarchy optimized | **25%** |
| **$Q$** | Content Quality | Search intent matched, clear formatting, high readability score | **30%** |
| **$A$** | Authority & Links | 3+ high-quality internal links, healthy external backlinks | **20%** |

### Score Ranges and Actions

- **90–100 (Excellent):** No action required. Perform an annual review to keep content fresh.
- **75–89 (Good):** Apply minor optimizations: add alt text to images, improve internal linking.
- **60–74 (Fair):** Address minor issues: improve readability, update outdated stats.
- **40–59 (Poor):** Fix critical errors: fix broken links, improve slow page load speeds, refine thin content.
- **0–39 (Critical):** Immediate action needed: rewrite the page entirely, redirect it, or remove it from the index.

---

## 4. Audit Checklists

Our check sheets establish rules to ensure page quality:

### 1. Technical SEO Checklist
- [ ] **Index Status:** Verify page is indexed correctly in Google Search Console (GSC).
- [ ] **Canonical Tags:** Confirm canonical URLs match the page URL to prevent duplicates.
- [ ] **Page Speed:** Ensure Mobile Core Web Vitals score **Good** (LCP < 2.5s, FID < 100ms, CLS < 0.1).
- [ ] **Schema Markup:** Validate structured data (e.g. Article, FAQ Schema) using Google's schema test tool.

### 2. On-Page SEO Checklist
- [ ] **Title Tags:** Keep titles between **50 and 60 characters**, including primary target keywords.
- [ ] **Meta Descriptions:** Keep descriptions under **155 characters**, including target keywords and clear CTAs.
- [ ] **Heading Structure:** Ensure only one `<h1>` tag is used, followed by a logical hierarchy (`<h2>`, `<h3>`).
- [ ] **Image Alt Text:** Confirm all images use descriptive alt text that includes keywords naturally.

### 3. Content Quality Checklist
- [ ] **Search Intent:** Verify the content matches search intent (Informational, Transactional, Navigational).
- [ ] **Readability:** Aim for a Grade 8 reading level or lower on the Hemingway Editor scale.
- [ ] **Outdated Stats:** Update outdated statistics and links to keep the article current.
- [ ] **Conversion Focus:** Place relevant call-to-actions (CTAs) within the content flow to drive leads.

### 4. Backlink Profile Checklist
- [ ] **Internal Inlinks:** Confirm the page has at least **3 to 5 internal links** from other relevant pages.
- [ ] **Broken Links:** Run audits to locate and fix broken links (404 errors) on the page.
- [ ] **Anchor Text:** Ensure anchor text uses descriptive, natural phrasing rather than generic terms like "click here."

---

## 5. Screaming Frog Crawl Configurations

Configure **Screaming Frog SEO Spider** to extract on-page metrics efficiently:

- **Step 1:** Go to `Configuration > Spider > Crawl` and enable `Canonical`, `Pagination`, `H1`, `H2`, `Structured Data`, and `Core Web Vitals`.
- **Step 2:** Go to `Configuration > API > Google Search Console` and link your GSC account to pull organic click data.
- **Step 3:** Go to `Configuration > API > PageSpeed Insights` and enter your API key to fetch Core Web Vitals metrics directly.
- **Step 4:** Run the site crawl and export the **Internal All** spreadsheet to seed the page audit tracker.

---

## 6. Monthly Audit Process (30-Day Timeline)

We audit content on a 30-day recurring cycle:

```
┌────────────────────────────────────────────────────────┐
│               MONTHLY AUDIT TIMELINE                   │
├────────────────────────────────────────────────────────┤
│  DAYS 1 - 7: Site Crawling & Setup                     │
│  - Run Screaming Frog site crawls.                      │
│  - Export baseline metrics to tracking sheets.         │
├────────────────────────────────────────────────────────┤
│  DAYS 8 - 15: Evaluation & Scoring                     │
│  - Apply the weighted scoring formula to each page.    │
│  - Identify pages with critical errors.                │
├────────────────────────────────────────────────────────┤
│  DAYS 16 - 20: Prioritization                          │
│  - Map pages to the Effort vs Impact matrix.           │
│  - Plan the content optimization roadmap.              │
├────────────────────────────────────────────────────────┤
│  DAYS 21 - 30: Implementation & Reporting               │
│  - Fix technical errors and update content.            │
│  - Deliver executive reports to stakeholders.          │
└────────────────────────────────────────────────────────┘
```

---

## 7. Quick Win Playbook (Optimizations in Under 1 Hour)

When beginning an audit, focus on quick wins that drive traffic improvements with minimal effort:

1. **Title Tag Optimization:** Update titles to target keywords with high search volume but low click-through rates (CTR) in GSC.
2. **Featured Snippet Optimization:** Add clear, 50-word answer blocks under `<h2>` target questions to target featured snippets.
3. **Internal Linking:** Add links from high-authority pages to new or low-performing content.
4. **Fix 404 Redirects:** Redirect broken links to relevant active pages.
5. **Add Schema:** Add FAQ or Article schema markup to improve search appearance.

---

## 8. Recommended Tool Stack & Budgeting

We recommend the following tool stack to manage and run audits:

| Tool Name | Tool Category | Monthly Cost | Primary Purpose |
|---|---|---|---|
| **Screaming Frog** | Technical Crawler | Free / \$259/year | Running site crawls and exporting bulk metadata |
| **Ahrefs / SEMrush** | Keyword/Backlink | \$129 - \$299/mo | Analyzing competitor keyword gaps and backlinks |
| **Google Console** | Organic Performance | Free | Auditing search impressions, positions, and indexing |
| **PageSpeed Insights** | Performance / Core Web Vitals | Free | Tracking mobile page load times and diagnostics |
| **Hemingway Editor** | Readability | Free | Improving writing clarity and readability scores |

---

## 9. RACI Matrix & Team Responsibilities

Define roles for each task to keep the auditing process on track:

| Task / Deliverable | SEO Specialist | Content Writer | Web Developer | Marketing Director |
|---|---|---|---|---|
| Site Crawling | **Accountable/Responsible**| Consulted | Informed | Informed |
| Content Rewrites | Consulted | **Responsible** | Informed | Accountable/Approved |
| Schema & Speed | Consulted | Informed | **Responsible** | Accountable |
| Executive Summary | **Accountable/Responsible**| Consulted | Informed | Approved |

---

## 10. Page Audit Tracking Sheet Structure

The file `templates/PAGE_AUDIT_SHEET.csv` outlines the template structure used to track page-level audits:

```csv
URL,Title,Page Score,Organic Clicks,Search Intent,Word Count,Status,Next Action
https://saas-example.com/blog/best-analytics,Best Analytics Tools,74.5,1240,Informational,1850,Fair,Add internal links and update stats
https://saas-example.com/blog/crm-setup,CRM Integration Guide,48.0,150,Informational,650,Poor,Rewrite content and check schema
https://saas-example.com/pricing,Pricing Plans,92.0,5400,Transactional,320,Excellent,No action required
```

---

## 11. Keyword Gap Analysis Framework

Analyze competitor keyword gaps to identify content opportunities:

- **Step 1:** Add your domain and three competitor domains to Ahrefs or SEMrush.
- **Step 2:** Filter results to show keywords where competitors rank in positions 1 to 10, but your site does not rank.
- **Step 3:** Prioritize high-intent keywords that match your product offerings.
- **Step 4:** Plan and write targeted content to capture these search terms.

---

## 12. KPIs, Dashboards & GA4 Reporting Models

Track SEO success metrics on a monthly basis:

- **Organic Pipeline conversions:** Strategy Call bookings, product signups, and trial starts originating from organic search.
- **CTR by Query:** Monitor search impressions and click-through rates (CTR) in GSC.
- **Keyword Rankings:** Track improvements in keyword positions for target queries.
- **Organic Sessions:** Monitor organic search traffic trends in GA4.

---

## 13. Prioritization Matrix (Impact vs Effort)

Prioritize optimizations based on a simple matrix to get the best results for your effort:

- **Quick Wins (High Impact, Low Effort):** Title tag updates, fixing broken links, adding internal links.
- **Major Projects (High Impact, High Effort):** Rewrite thin content, optimize page load speeds, update product landing pages.
- **Fill-ins (Low Impact, Low Effort):** Update image alt text, fix minor formatting issues.
- **Low Priority (Low Impact, High Effort):** Redesigning old blog layouts.

---

## 14. Verification Plan

### Technical Audits
1. Run follow-up crawls in Screaming Frog to confirm redirects and page speed issues are resolved.
2. Check schema deployments using the Rich Results Test tool.

### Content Performance Checks
1. Monitor GSC to verify organic impressions and click-through rates (CTR) improve for optimized keywords.
2. Check GA4 conversions to track lead registrations from updated landing pages.

---

## 15. Project Changelog

### v1.0.0
- Launch of the initial auditing playbook.
- 0-100 page scoring rubric formulas.
- Auditing checklists: technical, on-page, quality, and backlinks.
- Screaming Frog configuration guides.
- 30-day auditing timeline configurations.

---

## 16. Contributing Guidelines

1. Proposed checklist updates must focus on B2B SaaS conversion goals and ranking signals.
2. Changes to templates should follow the standard layouts of our existing spreadsheets.

---
#   4 d k - c h i t h r a - d i g i t a l m a r k e t i n g - i n t e r n s h i p