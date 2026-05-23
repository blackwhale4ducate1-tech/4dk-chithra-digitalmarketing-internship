# Content Quality & Editorial Audit Checklist

## 🎯 1. Purpose & Business Context
Search engines increasingly prioritize helpful, reliable, and people-first content (Google's E-E-A-T guidelines: Experience, Expertise, Authoritativeness, Trustworthiness). In B2B SaaS, visitors search for content to solve specific workflow bottlenecks, evaluate products, or train their teams.

This checklist evaluates the editorial quality, depth, and clarity of your content. By auditing for thin content, duplicate pages, outdated facts, and complex reading levels, we ensure your site builds trust with visitors and maintains rankings during search engine core updates.

---

## 📋 2. Content Quality Checklist Items

### A. Thin Content Identification
*   **Definition:** Pages with **fewer than 300 words** of unique, valuable content.
*   **Audit Rules:**
    *   Find low word count pages using your Screaming Frog crawl.
    *   Exclude natural exceptions like `Contact Us` pages, log-in pages, and resource hubs.
    *   Evaluate if informational blog posts or feature pages under 1,000 words provide enough depth to satisfy the searcher's query.
*   **Execution Steps:**
    1.  Filter crawl data by `Word Count` in ascending order.
    2.  Review all pages with under 300 words.
    3.  Flag pages as: **Prune** (delete & 301 redirect), **Consolidate** (merge with a larger article), or **Expand** (rewrite with more details).

### B. Duplicate & Near-Duplicate Content
*   **Audit Rules:**
    *   Ensure no page contains substantial blocks of text identical to another internal page or external website.
    *   Watch for near-duplicate SaaS pages, such as regional pricing variants or template-based industry pages where only the industry name changes.
*   **Execution Steps:**
    1.  Scan the site using [Siteliner](https://www.siteliner.com/) (internal duplicates) or [Copyscape](https://www.copyscape.com/) (external duplicates).
    2.  If duplicate percentage exceeds **20%** for a page, adjust the copy to add unique perspectives, or implement canonical tags pointing to the primary version.

### C. Outdated Content Review
*   **Audit Rules:**
    *   SaaS products change fast. Review pages annually to ensure screenshots, product features, prices, and software interface guidelines match the current live product.
    *   Check for outdated years in titles (e.g., "Best Marketing Tools for 2023").
    *   Ensure external data references and statistics are not more than 2-3 years old.
*   **Execution Steps:**
    1.  Sort site inventory by "Last Modified Date" or publishing date.
    2.  Flag articles older than 12 months for a quality review.
    3.  Replace old statistics, update product UI screenshots, and adjust dated title tags.

### D. Readability Analysis (Flesch-Kincaid Scale)
*   **Target Score:** **7th to 10th-grade reading level** (Flesch-Kincaid).
*   **Audit Rules:**
    *   Avoid overly academic, passive, or jargon-heavy writing. Keep B2B explanations simple and clear.
    *   Use short paragraphs (2-3 sentences max) and bullet points to make content scannable.
*   **Execution Steps:**
    1.  Paste article body text into the [Hemingway Editor](https://hemingwayapp.com/) or run it through [Readable](https://readable.com/).
    2.  Identify and break down "very hard to read" sentences (highlighted in red in Hemingway).
    3.  Simplify passive voice constructions and replace industry jargon with plain language.

---

## 🖼️ 3. Example Screenshot Descriptions
*   **Screenshot 1: Siteliner Duplicate Content Scan Results**
    *   *Description:* A Siteliner report dashboard highlighting duplicate content matching across a B2B site. A pie chart shows the site split into "Duplicate Content" (28%), "Common Content" (42%), and "Unique Content" (30%). A table displays matched page pairs.
*   **Screenshot 2: Content Refresh Planning Table**
    *   *Description:* A Google Sheets spreadsheet showing columns: `URL`, `Publishing Date`, `Outdated Elements Found`, `Action (Expand/Redirect/Keep)`, and `Assigned Writer`. Cells flag old software screenshots in red.

---

## 🚫 4. Common Mistakes to Avoid
*   **Pruning Traffic-Generating Pages:** Deleting a short 250-word page because it's "thin," without checking if it currently ranks for key terms or drives conversions. Check traffic metrics *before* deleting any page.
*   **Over-reliance on Jargon:** Writing complex, buzzword-heavy copy (e.g., "synergistic paradigm-shifting enterprise solutions") that makes content difficult to read and alienates users.
*   **Changing URL Slugs on Content Refreshes:** Modifying the URL path (e.g., from `/blog/crm-guide` to `/blog/crm-guide-updated`) when updating an article. This breaks existing backlinks. Keep the URL identical and set up a redirect if changes are unavoidable.

---

## 📅 5. Expected Outcomes & Timelines
*   **Days 1-2:** Identify thin pages, duplicate page clusters, and outdated content articles using crawl data.
*   **Days 3-7:** Run Hemingway readability scans on the top 30 traffic-driving articles.
*   **Day 8 onwards:** Distribute writing briefs to copywriters for expansions or updates.
*   **Implementation Timeline:**
    *   Redirect thin/redundant pages: **Within 5 business days**.
    *   Update year tags in titles: **Within 2 days** (at the start of the year).
    *   High-priority content refreshes: **Completed in 2-week batches**.
    *   *Expected Result:* Lower site-wide duplicate content percentages (<15% average), improved reader engagement (lower bounce rate, higher dwell times), and stable rankings through search engine algorithm updates.
