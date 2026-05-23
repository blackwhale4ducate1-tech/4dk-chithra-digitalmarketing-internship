# SEO Scoring Rubric & Page Grading System

## 🎯 1. Purpose & Business Context
To manage and optimize a large B2B SaaS website, subjective feedback like "this page feels thin" or "that page is slow" is not enough. We need a standardized, quantitative, and repeatable grading framework.

This scoring rubric converts qualitative checklists into an objective **Weighted SEO Score (0-100)** for every indexable URL. This system allows the SEO team to easily identify underperforming pages, justify optimization resources to product leadership, and track site improvements over time.

---

## 📐 2. The Weighting Formula
Each audited URL receives scores from 0 to 100 across four distinct categories. The overall **Page Score** is calculated using the following weights:

$$\text{Final Page Score} = (T \times 0.20) + (O \times 0.30) + (Q \times 0.35) + (B \times 0.15)$$

Where:
*   **$T$ = Technical SEO Score (20%):** Site speed, crawlability, HTTP status, and mobile friendliness.
*   **$O$ = On-Page SEO Score (30%):** Metadata compliance, structure of headers, keyword targeting, and image optimizations.
*   **$Q$ = Content Quality Score (35%):** Word count, search intent match, readability scores, and freshness.
*   **$B$ = Backlink Profile Score (15%):** Page-level backlink quantity, domain authority, and toxic link ratios.

---

## 📝 3. Detailed Scoring Criteria

### A. Technical SEO (Weight: 20%)
| Score Range | Criteria |
| :--- | :--- |
| **90 - 100** | HTTPS active, PageSpeed score > 85 (Mobile), no crawl errors, structured Schema markup present and valid, canonical tag points to self. |
| **70 - 89** | Valid SSL, PageSpeed score 65-84, minor CSS blocking issues, valid Schema but minor warnings in Search Console, self-canonicalized. |
| **40 - 69** | Site is crawlable but slow (PageSpeed < 65), missing structured data, contains redirects (301 chain), or has minor mobile rendering bugs. |
| **0 - 39** | HTTP status error (404, 500), blocked by robots.txt or has noindex tags, contains broken canonicals, or fails mobile-friendly tests completely. |

### B. On-Page SEO (Weight: 30%)
| Score Range | Criteria |
| :--- | :--- |
| **90 - 100** | Title tag (50-60 chars) and meta description (150-160 chars) match target keyword; clear H1-H3 hierarchy; primary keyword in first 100 words; all images have descriptive alt texts; optimized internal linking (3+ inbound links). |
| **70 - 89** | Metadata is present but slightly long/short (e.g., Title 65 chars, Meta 170 chars); H-structure has small inconsistencies (e.g., missing H2); partial keyword matches; minor image alt tags missing. |
| **40 - 69** | Missing meta descriptions or title tags; no clear H1 hierarchy (multiple H1s or missing H1); keyword stuffing; poor or missing internal link anchors. |
| **0 - 39** | No title tag; duplicate metadata shared across multiple pages; zero search intent optimization; no internal linking pointing to the page. |

### C. Content Quality (Weight: 35%)
| Score Range | Criteria |
| :--- | :--- |
| **90 - 100** | In-depth coverage (e.g., > 1,500 words for long-form, or highly optimized product page); Flesch-Kincaid grade level between 7th and 10th grade; zero duplicate text; updated in the last 6 months; clear CTA. |
| **70 - 89** | Word count 800 - 1,500; readable language but slightly passive; minor duplicate text blocks (<10%); updated in last 12 months; clear CTA present. |
| **40 - 69** | Thin content (300-800 words for informational pages); reading level too complex (14th grade+); outdated statistics (2+ years old); no clear conversion path or CTAs. |
| **0 - 39** | Critically thin content (<300 words); auto-generated or scraped copy; duplicate content (>30%); outdated/inaccurate product features; missing or broken links. |

### D. Backlink Profile (Weight: 15%)
| Score Range | Criteria |
| :--- | :--- |
| **90 - 100** | Page has high-quality backlinks from high domain authority sites (DR/DA > 50); low toxicity scores (<5%); natural anchor text distribution. |
| **70 - 89** | Moderate backlink numbers; authority sites DR/DA 30-50; toxicity scores under 15%; standard anchor profile. |
| **40 - 69** | Few or no backlinks; toxic links representing 15-30% of backlink profile; anchor text looks slightly optimized (keyword stuffed). |
| **0 - 39** | High toxicity backlinks (>30% spam links); manual backlink action warnings; high velocity of spam links; manipulative/unnatural anchor texts. |

---

## 🛠️ 4. Step-by-Step Instructions: Scoring a Page

1.  **Open your page audit sheet:** Go to your central shared sheet (derived from [PAGE_AUDIT_SHEET.csv](file:///d:/4DK/Projects/Marketting/seo-content-audit-strategy/templates/PAGE_AUDIT_SHEET.csv)).
2.  **Evaluate Technical:** Check Google Search Console, Screaming Frog, and PageSpeed Insights for the URL. Grade it 0-100.
3.  **Evaluate On-Page:** Inspect page source or use an SEO browser extension (e.g., Detailed SEO Extension) to check meta tags, H-tags, alt texts, and internal links. Grade it 0-100.
4.  **Evaluate Quality:** Copy page copy into Hemingway Editor to check readability grade level. Perform a word count check and look for outdated product specs. Grade it 0-100.
5.  **Evaluate Backlinks:** Pull up the page URL in Ahrefs Site Explorer or SEMrush Backlink Audit. Check page-level referring domains and toxicity levels. Grade it 0-100.
6.  **Calculate Final Score:** Use the weighted Excel/Google Sheets formula to automatically output the final score:
    `=(B2*0.2) + (C2*0.3) + (D2*0.35) + (E2*0.15)` *(assuming B=Tech, C=On-Page, D=Quality, E=Backlinks)*

---

## 🖼️ 5. Example Screenshot Descriptions
*   **Screenshot 1: Page Grading Dashboard in Google Sheets**
    *   *Description:* An Excel sheet showing columns for `URL`, `Tech Score`, `On-Page Score`, `Quality Score`, `Backlink Score`, and a calculated `Final Score` column. Cells in the `Final Score` column are color-coded (Red for scores below 50, Yellow for 50-74, and Green for 75-100) using conditional formatting.
*   **Screenshot 2: Readability Scoring Example**
    *   *Description:* A screenshot of the Hemingway Editor interface evaluating a SaaS blog article. It shows a readability grade of "Grade 9 (Good)" on the right side and highlights passive voice, hard-to-read sentences, and complex words.

---

## 🚫 6. Common Mistakes to Avoid
*   **Overweighting Page Speed:** While site speed is a ranking factor, scoring a page at 0 overall because it has a mobile speed score of 50 is a mistake. Keep the categories weighted according to the formula.
*   **Using Complex Decimals:** Round your category scores to the nearest whole integer (e.g., 78 instead of 77.62) to keep the tracking sheet simple and readable.
*   **Inconsistent Evaluators:** Different team members grading pages differently. To avoid this, ensure the auditor references the criteria tables above to maintain objective grading.

---

## 📅 7. Expected Outcomes & Timelines
*   **Initial Rollout (Week 1):** Train the SEO and Content teams on the grading criteria. Score 5 test pages together to align on grading standards.
*   **Ongoing Audits (Monthly):** Score all audited pages inside the `PAGE_AUDIT_SHEET.csv`. 
*   **Remediation Goal:** Any page scoring below **60** must have optimization tickets created within 48 hours of audit completion. Target an average site-wide page score of **80+** within 90 days.
