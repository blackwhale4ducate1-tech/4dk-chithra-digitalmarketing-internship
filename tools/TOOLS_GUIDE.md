# SEO Tools Guide & Configuration SOP

## 🎯 1. Purpose & Business Context
Auditing a B2B SaaS website requires specialized SEO platforms to analyze crawl structures, backlink matrices, keyword positions, and technical speed. Different team members might use these tools inconsistently, leading to fragmented metrics.

This document acts as the **Standard Operating Procedure (SOP)** for our SEO tool stack. It ensures everyone on the team configures, runs, and interprets results from Screaming Frog, SEMrush, Ahrefs, Google Search Console, PageSpeed Insights, and GTmetrix in an identical manner.

---

## 📋 2. Step-by-Step Tool SOPs

### A. Screaming Frog SEO Spider (Crawl Engine)
*   **Purpose:** Map site structure, identify status codes, and export metadata.
*   **Step-by-Step Instructions:**
    1.  Open Screaming Frog. Go to **Configuration > Spider > Crawl**.
    2.  Check the boxes for: `Crawl All Subdomains`, `Check Canonical`, `Check Next/Prev`, and `Check HTTPS`.
    3.  Go to **Configuration > API Access** and connect **Google Search Console** and **PageSpeed Insights** using your team credentials to pull organic performance data directly into your crawl reports.
    4.  Enter your target domain (`https://example.saas.com/`) and click **Start**.
    5.  Once the crawl reaches 100%, export the data. Refer to [SCREAMING_FROG_EXPORT.md](file:///d:/4DK/Projects/Marketting/seo-content-audit-strategy/tools/SCREAMING_FROG_EXPORT.md) for columns to isolate.

### B. SEMrush & Ahrefs (Keywords & Competitors)
*   **Purpose:** Map keyword rankings, analyze competitor gaps, and audit backlink profiles.
*   **Step-by-Step Instructions:**
    1.  Open Ahrefs Site Explorer. Enter your SaaS domain and click Search.
    2.  Go to **Organic Keywords** to see your current ranking terms. Filter by **Position: 11-20** to find striking-distance content opportunities.
    3.  Go to **Content Gap** and input your top 3 competitors. Click **Show Keywords** to isolate keywords where competitors rank on page 1 but your site does not.
    4.  Export these keywords to compile your [KEYWORD_GAP_ANALYSIS.csv](file:///d:/4DK/Projects/Marketting/seo-content-audit-strategy/templates/KEYWORD_GAP_ANALYSIS.csv).

### C. Google Search Console (Organic Performance)
*   **Purpose:** Inspect index coverage, submit XML sitemaps, and evaluate mobile usability.
*   **Step-by-Step Instructions:**
    1.  Log in to [Google Search Console](https://search.google.com/search-console).
    2.  Navigate to **Performance > Search Results**. Filter date range to the last **3 months**.
    3.  Toggle on **Total Clicks**, **Total Impressions**, **Average CTR**, and **Average Position**.
    4.  Go to **Pages** tab and sort by impressions in descending order. Find pages with high impressions but low CTR (<1%) to target for title/meta tag optimizations.
    5.  Check **Indexing > Page Indexing** to ensure there are no spikes in "Crawl anomalies" or "Not indexed" pages.

### D. Google PageSpeed Insights & GTmetrix (Performance & Speed)
*   **Purpose:** Measure page load speeds and identify rendering bottlenecks.
*   **Step-by-Step Instructions:**
    1.  Navigate to [PageSpeed Insights](https://pagespeed.web.dev/).
    2.  Input your core conversion URLs (e.g., Homepage, Pricing, main product features).
    3.  Record the mobile speed performance score. Mobile performance is Google's primary indexing signal (Mobile-First Indexing).
    4.  For detailed waterfalls, paste the URL into [GTmetrix](https://gtmetrix.com/). Analyze the **Waterfall Chart** tab to identify heavy scripts or CSS files that block browser rendering.

---

## 🖼️ 3. Example Screenshot Descriptions
*   **Screenshot 1: Screaming Frog API Integration Panel**
    *   *Description:* A screen view of Screaming Frog's Configuration dropdown. The "API Access" setting is open, displaying checkbox ticks and green checkmarks indicating successful API connections to Google Search Console and PageSpeed Insights.
*   **Screenshot 2: Ahrefs Content Gap Setup**
    *   *Description:* The setup screen of Ahrefs Content Gap tool. Three competitor domain inputs are shown in the "Show keywords that the following targets rank for" fields, while the company's domain is in the "But the following target does not rank for" field.

---

## 🚫 4. Common Mistakes to Avoid
*   **Crawling and Testing the Wrong Protocol:** Running speed tests or crawls on `http://example.saas.com` instead of the secure `https://example.saas.com`. This creates crawl issues and skews speed results.
*   **Ignoring User-Agent Settings:** Forgetting that search engines crawl using mobile user agents. In Screaming Frog, ensure your User-Agent is set to **Googlebot Smartphone** inside `Configuration > User-Agent` to see what Googlebot actually sees.
*   **Exceeding API Query Limits:** Running massive batch speed tests in PageSpeed Insights without API key throttling, which can cause temporary IP blocks.

---

## 📅 5. Expected Outcomes & Timelines
*   **Setup Period (Days 1 - 2):** Connect all API integrations in Screaming Frog and configure access roles for GSC and Ahrefs.
*   **Auditing Cycles (Monthly):** Ensure every auditor runs tests according to these exact guidelines.
*   **Expected Outcome:** 100% uniformity in technical crawling and performance evaluations across the team, resulting in reliable tracking metrics.
