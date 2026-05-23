# KPI Dashboard & SEO Performance Tracking

## 🎯 1. Purpose & Business Context
For B2B SaaS platforms, reporting on "organic sessions" or "keyword ranks" alone is not enough to show business value. Executives need to see how organic search contributions impact the bottom line—such as trial sign-ups, demo requests, and customer acquisition.

This document defines the key performance indicators (KPIs) we track, explains how to structure an automated reporting dashboard (using Google Looker Studio), and connects search engine performance to SaaS business goals.

---

## 📋 2. Core SEO KPIs to Track

### A. Business & Conversion Metrics (Bottom-of-Funnel)
*   **Primary KPIs:** 
    *   **Organic Demo Submissions:** Number of demo requests originating from organic search sessions.
    *   **Organic Free Trial Starts:** Number of self-serve trial sign-ups originating from organic search.
*   **Measurement Tool:** Google Analytics 4 (GA4) with conversion tracking, or HubSpot/Marketo CRM tracking.

### B. Search Performance Metrics (Middle-of-Funnel)
*   **Primary KPIs:**
    *   **Organic Sessions:** Unique visits coming from non-paid search results.
    *   **Click-Through Rate (CTR):** Clicks divided by impressions (via Google Search Console).
    *   **Average Search Position:** The average rank of our pages across all search terms.
*   **Measurement Tool:** Google Search Console, Google Analytics 4.

### C. Technical Health & Quality Metrics (Top-of-Funnel)
*   **Primary KPIs:**
    *   **Indexed vs. Non-Indexed Pages:** The ratio of pages crawled and available in search results.
    *   **Crawl Error Rate:** Percentage of crawled pages returning 4xx or 5xx status codes.
    *   **Core Web Vitals Pass Rate:** Percentage of page views meeting the "Good" speed category.
*   **Measurement Tool:** Google Search Console, Screaming Frog, PageSpeed Insights.

---

## 🛠️ 3. Step-by-Step Instructions: Setting up Looker Studio

Follow these steps to build an automated SEO reporting dashboard:

### Step 1: Connect Your Data Sources
1.  Open [Google Looker Studio](https://lookerstudio.google.com/). Click **Create > Report**.
2.  Add a data source for **Google Analytics 4** (select your target property).
3.  Add a second data source for **Search Console** (select your domain property and choose **Site Impression** and **Web** parameters).

### Step 2: Build the Performance Scorecards
1.  Create a scorecard widget for **Organic Users** from GA4. Set comparison period to **Previous Period** (to track month-over-month change).
2.  Add scorecards for Search Console **Clicks**, **Impressions**, and **Average CTR**.

### Step 3: Add Conversion Trend Lines
1.  Insert a time-series line chart.
2.  Set the dimension to **Date** and the metric to your GA4 conversion events (e.g., `sign_up_completed`, `demo_requested`).
3.  Filter the chart by `Default Channel Grouping` equals **Organic Search** to isolate search conversions.

### Step 4: Add the Page Audit Tracker
1.  Insert a table widget displaying top pages.
2.  Set dimensions to **Landing Page** and metrics to **Sessions**, **Bounce Rate**, and **Conversions**. Use this to identify which blog pages are bringing traffic but not generating leads.

---

## 🖼️ 4. Example Screenshot Descriptions
*   **Screenshot 1: Looker Studio SEO Executive Dashboard**
    *   *Description:* A Looker Studio dashboard showing key performance indicators at the top (Clicks, Impressions, CTR, average position) in blue cards. Below are two charts: a line graph displaying organic conversions MoM and a bar chart showing top organic landing pages.
*   **Screenshot 2: GA4 Custom Report Builder**
    *   *Description:* The GA4 Exploration interface showing a customized table segmenting users by "First user default channel group" equals "Organic Search", displaying detailed metrics like engagement rate and event counts.

---

## 🚫 5. Common Mistakes to Avoid
*   **Including Internal Traffic in Reports:** Not filtering out employee traffic. Internal team visits will skew bounce rates and session lengths. Ensure your office IP addresses and remote VPN IPs are filtered out in GA4 settings.
*   **Focusing on Vanity Metrics:** Reporting a 50% increase in traffic without tracking conversions. Traffic is only valuable if it brings target customers who convert.
*   **Reporting Global Traffic for Local SaaS:** If your software only sells in North America, tracking global traffic increases from regions you do not serve can mislead stakeholders. Use GA4 geography filters to isolate core markets.

---

## 📅 6. Expected Outcomes & Timelines
*   **Looker Studio Setup:** Complete the dashboard within 2 business days.
*   **Monthly Updates:** Log monthly metrics inside the `BASELINE_TEMPLATE.csv` on the last business day of every month.
*   **Target Performance Goals (90-Day Outlook):**
    *   **Organic Sessions:** Maintain a steady **5% to 8% month-over-month growth rate**.
    *   **Organic Conversion Rate:** Average a **1.5% to 3.0% conversion rate** from organic traffic.
    *   **Crawl Errors:** Maintain crawl errors under **1% of total site pages**.
