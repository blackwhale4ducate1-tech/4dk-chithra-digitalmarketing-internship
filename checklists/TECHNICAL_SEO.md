# Technical SEO Audit Checklist

## 🎯 1. Purpose & Business Context
Technical SEO is the foundation of organic search visibility. If a search engine cannot discover, crawl, or index your pages, even the highest-quality content will fail to rank.

This checklist focuses on evaluating site health, Core Web Vitals, indexation pathways, security, and machine-readable structured schema markup. For a B2B SaaS platform, resolving technical issues improves search engine access and reduces user bounce rates caused by slow-loading product pages or secure-login errors.

---

## 📋 2. Technical SEO Checklist Items

### A. Page Speed & Core Web Vitals (CWV)
*   **Assessment:** Evaluate Largest Contentful Paint (LCP), First Input Delay (FID) / Interaction to Next Paint (INP), and Cumulative Layout Shift (CLS).
*   **Target Metrics:**
    *   **LCP:** $\le$ 2.5 seconds (Good)
    *   **INP:** $\le$ 200 milliseconds (Good)
    *   **CLS:** $\le$ 0.1 (Good)
*   **Execution Steps:**
    1.  Input target URL into [Google PageSpeed Insights](https://pagespeed.web.dev/).
    2.  Check the "Core Web Vitals Assessment" pass/fail status.
    3.  Analyze the "Diagnostics" section for resource-blocking Javascript, unoptimized images, or layout shifts.
    4.  Create developer tickets to enable modern image formats (WebP/AVIF), activate server compression (Gzip/Brotli), and delay non-essential script execution.

### B. robots.txt & Crawl Pathways
*   **Assessment:** Ensure robots.txt is present, valid, and contains links to the sitemap while excluding non-public pages.
*   **Execution Steps:**
    1.  Navigate to `https://yourdomain.com/robots.txt`.
    2.  Check for wildcard blocking rules like `Disallow: /` which block search engines from crawling the entire site.
    3.  Verify that your staging environment has a strict `Disallow: /` rule.
    4.  Verify that application dashboard paths (e.g., `/app/`, `/billing/`) are excluded for search engines.

### C. XML Sitemaps
*   **Assessment:** Confirm sitemap existence, cleanliness, and submission status.
*   **Execution Steps:**
    1.  Locate your sitemap index, usually at `https://yourdomain.com/sitemap.xml` or referenced in your robots.txt.
    2.  Verify the sitemap contains *only* 200 OK indexable marketing URLs. It must exclude redirects, broken pages, and pages with `noindex` tags.
    3.  Check the sitemap submission status inside Google Search Console under **Indexing > Sitemaps**. Ensure there are no parsing errors.

### D. HTTPS & Security Protocol
*   **Assessment:** Ensure all traffic redirects to secure HTTPS connections.
*   **Execution Steps:**
    1.  Test http version of your site (e.g., `http://yourdomain.com`). It must 301-redirect to `https://yourdomain.com`.
    2.  Ensure there are no "mixed content" warnings (HTTP resources loaded on an HTTPS page). Look for mixed content warnings in the browser developer tools console.

### E. Crawl Errors & HTTP Status Codes
*   **Assessment:** Minimize server errors (5xx) and page-not-found errors (4xx) on linked pages.
*   **Execution Steps:**
    1.  Run a Screaming Frog crawl of the site.
    2.  Filter the results by "Response Codes" column.
    3.  Identify any 404 (Not Found) or 500 (Internal Server Error) status codes.
    4.  Redirect broken 404 links to relevant live pages and consult developers on resolving 500 errors.

### F. Structured Data (Schema Markup)
*   **Assessment:** Ensure pages use JSON-LD Schema to help search engines understand page context and render rich snippets.
*   **Execution Steps:**
    1.  For product/feature pages, confirm `SoftwareApplication` or `Product` schema is present.
    2.  For blog posts, confirm `BlogPosting` or `Article` schema is active.
    3.  For FAQ sections, ensure `FAQPage` schema is implemented.
    4.  Verify all schemas using the [Schema Markup Validator](https://validator.schema.org/) or GSC's Rich Results Test tool.

---

## 🖼️ 3. Example Screenshot Descriptions
*   **Screenshot 1: Google Search Console Page Indexing Report**
    *   *Description:* The Indexing report in GSC displaying a line chart of "Indexed" vs. "Not Indexed" pages. A red highlighted box points to the reasons why pages are not indexed (e.g., "Excluded by 'noindex' tag", "Soft 404").
*   **Screenshot 2: PageSpeed Insights Core Web Vitals Diagnostic**
    *   *Description:* A PageSpeed Insights mobile report displaying three circular indicators for LCP, INP, and CLS. A highlighted warning states "Eliminate render-blocking resources", showing a breakdown of heavy JS files causing delays.

---

## 🚫 4. Common Mistakes to Avoid
*   **Leaving Staging Sitemaps Public:** Accidentally adding links to your staging site inside your production XML sitemap, causing crawl errors.
*   **Blocking CSS and JS Files in robots.txt:** Historically, SEOs blocked JS/CSS to save crawl budget. Today, Google needs to crawl CSS and JS to render the page and verify mobile compatibility. Keep them accessible.
*   **Using Multiple Canonical Tags on a Page:** Inserting multiple canonical tags via different plugins or hardcoded templates. This confuses search bots, leading them to ignore the canonical instructions completely.

---

## 📅 5. Expected Outcomes & Timelines
*   **Day 1:** Complete Screaming Frog crawl and export all status codes and crawl paths.
*   **Day 3:** Run PageSpeed evaluations on the top 20 transactional pages.
*   **Day 5:** Compile technical issues into Jira tickets and hand over to developers.
*   **Execution Timeline:** 
    *   Resolve 404/500 errors: **Within 5 business days**.
    *   Robots.txt & Sitemap corrections: **Within 3 business days**.
    *   Core Web Vitals optimizations: **1 to 2 developer sprints (15-30 days)**.
    *   *Expected Result:* 100% crawl accessibility, indexation of all strategic marketing pages, and Core Web Vitals scores in the "Good" range (Green) across all core landing pages.
