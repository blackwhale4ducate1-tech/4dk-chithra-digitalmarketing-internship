# Backlink Profile & Off-Page Audit Checklist

## 🎯 1. Purpose & Business Context
Backlinks (links from other sites to yours) function as votes of confidence in the eyes of search engine algorithms. A clean, high-authority backlink profile is essential for ranking competitive commercial terms in the B2B SaaS space.

However, unnatural links can trigger manual actions or algorithmic suppression. This checklist focuses on auditing your site's Domain Authority (DA/DR), locating toxic backlinks, analyzing anchor text distributions, monitoring link velocity, and reclaiming broken backlink equity.

---

## 📋 2. Backlink Audit Checklist Items

### A. Domain Authority (DA/DR) Benchmarking
*   **Assessment:** Check your site's Domain Rating (Ahrefs) or Authority Score (SEMrush) against your top 3-5 direct SaaS competitors.
*   **Execution Steps:**
    1.  Input your URL and competitor URLs into Ahrefs Site Explorer.
    2.  Record DA/DR values inside your [BASELINE_TEMPLATE.csv](file:///d:/4DK/Projects/Marketting/seo-content-audit-strategy/kpis/BASELINE_TEMPLATE.csv).
    3.  Identify the authority gap: if your DR is 45 and competitors are at 70, prioritize high-value content assets (infographics, research reports) to attract natural links.

### B. Toxic & Spam Link Detection
*   **Assessment:** Identify incoming links from spam networks, hacked sites, or low-quality directories.
*   **Execution Steps:**
    1.  Run a "Backlink Audit" inside SEMrush or Ahrefs.
    2.  Filter referring domains by "Toxic Score" (SEMrush) or inspect domains with low ratings and thousands of outgoing links.
    3.  Export toxic domains to a disavow text file *only* if you see an active warning in Google Search Console or a sudden drop in search traffic.

### C. Anchor Text Distribution
*   **Assessment:** Analyze the text clicked to visit your site. Unnatural profiles trigger spam filters.
*   **Target Profiles:**
    *   **Branded Anchors (50-70%):** e.g., `BrandName`, `yoursite.com`.
    *   **Generic Anchors (10-20%):** e.g., `website`, `click here`, `source`.
    *   **LSI / Partial Match Anchors (10-15%):** e.g., `features of our SaaS`, `team scheduling tool`.
    *   **Exact Match Anchors (<1-5%):** e.g., `best CRM software`.
*   **Execution Steps:**
    1.  Open Ahrefs Site Explorer > **Anchors**.
    2.  Identify any exact match terms that look over-optimized. If you see high percentages of spam keywords (e.g. unrelated products), your site may be a target of negative SEO.

### D. Link Velocity Mapping
*   **Assessment:** Monitor the rate at which your domain acquires new backlinks over time.
*   **Execution Steps:**
    1.  Review the "Referring Domains" growth chart in Ahrefs.
    2.  Look for abrupt, steep spikes in referring domains. 
    3.  Investigate spikes: if the spike is due to a successful PR campaign, it is healthy. If the spike consists of hundreds of automated forum profiles, monitor those domains for toxicity.

### E. Broken Link Reclamation (Link Juice Recovery)
*   **Assessment:** Find high-value external links pointing to 404 pages on your site.
*   **Execution Steps:**
    1.  Go to Ahrefs > **Best by Links** filter.
    2.  Set HTTP response filter to **404 Not Found**.
    3.  Identify pages with multiple referring domains that return 404 errors.
    4.  Implement 301 redirects inside your CMS to point those dead URLs to active, relevant pages to reclaim the link authority.

---

## 🖼️ 3. Example Screenshot Descriptions
*   **Screenshot 1: SEMrush Backlink Toxicity Dashboard**
    *   *Description:* A screenshot of the SEMrush Backlink Audit dashboard displaying an authority score, toxic score breakdown (Red for "Toxic", Orange for "Potentially Toxic", Green for "Healthy"), and a button to export toxic links to a disavow list.
*   **Screenshot 2: Referring Domains Growth Curve**
    *   *Description:* An Ahrefs line chart showing steady, upward growth in referring domains over 3 years. A second chart shows a comparison containing a sudden vertical spike, illustrating a spam attack or automated link building.

---

## 🚫 4. Common Mistakes to Avoid
*   **Over-disavowing Links:** Google's algorithms have evolved to ignore spam backlinks automatically. Disavowing links too aggressively can accidentally remove helpful links and lower your organic rankings. Disavow *only* when you have a manual action or clear evidence of search penalty.
*   **Buying Automated Link Packages:** Buying "Fiverr SEO packages" that promise 5,000 links in 24 hours. These links are low quality and will harm your site's rankings.
*   **Ignoring 404 Pages with Backlinks:** Letting valuable backlinks go to waste on 404 error pages. Reclaiming links via 301 redirects is one of the fastest ways to recover lost authority.

---

## 📅 5. Expected Outcomes & Timelines
*   **Day 1:** Benchmark DA/DR and competitor authority metrics.
*   **Day 2:** Run toxicity audits and flag domains for review.
*   **Day 3:** Run 404 link audits and set up 301 redirects.
*   **Timeline:**
    *   Setup 404 redirects: **Within 3 business days** (Quick Win).
    *   Disavow submission: **Only when necessary, reviews occur quarterly**.
    *   *Expected Result:* Zero wasted backlink equity (no backlinks pointing to 404s), a natural-looking anchor text profile, and a steady increase in Domain Authority over time.
