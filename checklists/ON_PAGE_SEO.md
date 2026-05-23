# On-Page SEO Audit Checklist

## 🎯 1. Purpose & Business Context
On-page SEO ensures that search engines can easily parse your content and match it to specific search queries. It also directly impacts click-through rate (CTR) from Search Engine Result Pages (SERPs) and improves user dwell time.

For B2B SaaS sites, on-page optimization requires balancing search keyword requirements with product marketing copy. This checklist ensures your pages use clear structures, click-worthy metadata, and logical internal links to direct prospects toward conversion actions.

---

## 📋 2. On-Page SEO Checklist Items

### A. Title Tags (SEO Titles)
*   **Target Length:** **50 to 60 characters** (to avoid truncation in search results).
*   **Audit Rules:**
    *   Include primary target keyword near the beginning of the title.
    *   Add brand name at the end (e.g., `Keyword - Brand`).
    *   Keep title tags unique across all pages.
*   **Execution Steps:**
    1.  Extract current title tags from your Screaming Frog crawl.
    2.  Highlight title tags that are under 50 characters or over 60 characters.
    3.  Rewrite titles to include the primary keyword while maintaining click appeal.

### B. Meta Descriptions
*   **Target Length:** **150 to 160 characters** (to avoid truncation in search results).
*   **Audit Rules:**
    *   Include primary target keyword or secondary variations.
    *   End with a clear, benefit-driven Call-To-Action (CTA) (e.g., *Try it free!*, *Get a demo today.*).
    *   Avoid duplicate descriptions across different URLs.
*   **Execution Steps:**
    1.  Identify pages with missing, duplicate, or truncated meta descriptions in the crawl report.
    2.  Write unique, compelling meta descriptions tailored to the search user's intent.

### C. Heading Structure (H1, H2, H3)
*   **Audit Rules:**
    *   Ensure **exactly one H1** is present per page, representing the main topic.
    *   Ensure H2, H3, and H4 headings follow a logical hierarchy (no jumping from H1 to H3).
    *   Use secondary keywords and natural variants in H2/H3 subheadings.
*   **Execution Steps:**
    1.  Inspect the heading structure of audited pages (using Screaming Frog's H1/H2 tabs or browser developer tools).
    2.  Correct code templates where blog titles are H1s and site logos or sidebar items are also marked as H1s.

### D. Keyword Placement & Density
*   **Audit Rules:**
    *   Place primary keyword in the H1, the first 100 words of body copy, and at least one H2.
    *   Avoid keyword stuffing; target a natural keyword density of **1% to 2%** of total page word count.
    *   Include Latent Semantic Indexing (LSI) or conceptually related terms.
*   **Execution Steps:**
    1.  Read through the text to check for keyword stuffing (repetitive or unnatural sentence structures).
    2.  Adjust phrasing to read naturally for human visitors while retaining target search terms.

### E. Internal Links & Anchor Text
*   **Audit Rules:**
    *   Every page must have at least **3 to 5 incoming internal links** from other relevant pages.
    *   Use descriptive, keyword-rich anchor texts (e.g., `features of project management software`) instead of generic phrases (e.g., `click here` or `read more`).
    *   Link to high-converting transactional pages (Pricing, Features, Request Demo) from top-performing blog posts.
*   **Execution Steps:**
    1.  Use search queries like `site:yourdomain.com "related term"` in Google to find pages that could link to the page you are auditing.
    2.  Add contextual internal links to these pages using appropriate anchor text.

### F. Image Alt Text
*   **Audit Rules:**
    *   Every image must have an `alt` attribute.
    *   Alt text must describe the image contents for accessibility, incorporating keywords naturally where relevant.
    *   Avoid generic names like `image1.png` or `screenshot_final.jpg` in both alt text and file names.
*   **Execution Steps:**
    1.  Identify images with missing alt tags using Screaming Frog.
    2.  Update the image metadata in your CMS with helpful, descriptive alt text.

---

## 🖼️ 3. Example Screenshot Descriptions
*   **Screenshot 1: SERP Preview Tool in SEO Plugin**
    *   *Description:* A screen view of a CMS SEO optimization widget (e.g., Yoast SEO or Webflow SEO panel) showing real-time previews for mobile and desktop SERPs. Progress bars for "SEO Title" and "Meta Description" are green, showing the character counts are within the target ranges.
*   **Screenshot 2: Incorrect vs. Correct Heading Hierarchy**
    *   *Description:* A side-by-side comparison diagram. On the left is an "Incorrect" structure showing multiple H1s and headings skipping levels (H1 $\rightarrow$ H3). On the right is a "Correct" structure showing one H1 at the top followed by nested H2s and H3s.

---

## 🚫 4. Common Mistakes to Avoid
*   **Optimizing for Multiple Primary Keywords:** Trying to make a single page rank for "crm software" and "project management software". Focus each page on one primary search intent.
*   **Using Raw URLs as Anchor Text:** Creating links like `https://yoursite.com/blog/best-crm` rather than wrapping the link in descriptive anchor text.
*   **Writing Alt Text for Purely Decorative Elements:** Creating alt text for divider lines, icons, or background decorative graphics. Decorative images should have empty alt tags (`alt=""`) so screen readers skip them.

---

## 📅 5. Expected Outcomes & Timelines
*   **Day 1:** Extract on-page crawl metrics for all tier-1 landing pages.
*   **Days 2-4:** Write optimized metadata overrides and H-tag adjustments.
*   **Day 5:** Input modifications into CMS and submit updated URLs to Google Search Console for re-indexing.
*   **Expected Result:** 100% of target pages have search-compliant title lengths, unique meta descriptions with clear CTAs, proper heading hierarchies, and descriptive image alt tags, leading to a **10% to 30% increase in organic click-through rates**.
