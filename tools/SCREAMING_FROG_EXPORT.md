# Screaming Frog Data Export & Filtering Playbook

## 🎯 1. Purpose & Business Context
Screaming Frog crawls yield hundreds of columns and thousands of data rows. Without clear instructions on what columns to isolate, team members can spend hours filtering noise instead of focusing on high-value data.

This document details the exact columns to export from Screaming Frog, what specific problems to look for in each column, and Excel/Google Sheets formulas to merge crawl data with Google Search Console performance reports.

---

## 📋 2. Step-by-Step Instructions: Exporting and Filtering

### Step A: Configure Columns Before Export
1.  Once the crawl is at 100%, navigate to the **Internal** tab in Screaming Frog.
2.  Set the filter dropdown to **HTML** (we only want to audit web pages, not images, CSS, or JS files).
3.  Click the **Export** button at the top left of the panel. Save the file as `screaming_frog_raw.csv`.

### Step B: Essential Columns to Keep
Open your exported CSV and delete all columns except the following:

| Column Header | What to Look For (Target Metrics) | Action If Out of Range |
| :--- | :--- | :--- |
| **Address** | Target URL. Look for staging protocols or uppercase characters. | Normalize to lowercase HTTPS. |
| **Status Code** | Target: **200 OK**. Watch for **301/302 redirects**, **404s**, or **500s**. | Replace or redirect broken links. |
| **Indexability** | Target: **Indexable**. Watch for **Non-Indexable**. | Review canonicals or remove `noindex` tags. |
| **Title 1** | Target length: **50 to 60 characters**. | Rewrite titles that are too long or short. |
| **Title 1 Length** | Numeric length of title. | Filter for values `< 50` or `> 60`. |
| **Meta Description 1** | Target length: **150 to 160 characters**. | Rewrite descriptions that are too long or short. |
| **Meta Desc 1 Length**| Numeric length of meta description. | Filter for values `< 150` or `> 160`. |
| **H1-1** | Target: **Exactly 1 H1 per page** that matches search intent. | Fix pages with multiple H1s or missing H1s. |
| **Word Count** | Target: **> 1,000 words** for blog posts, **> 300 words** for features. | Flag pages with low word count as "Thin Content". |

---

## 🧮 3. Useful Excel & Google Sheets Formulas

### Formula A: Find Character Lengths (If missing in export)
Use this to double-check title or meta lengths:
```excel
=LEN(C2)
```
*(Assuming cell C2 contains the Meta Description text)*

### Formula B: Merge Crawl Data with GSC Performance (VLOOKUP)
To bring GSC click data from another tab (named `GSC_Data`) into your master audit sheet:
```excel
=VLOOKUP(A2, 'GSC_Data'!A:B, 2, FALSE)
```
*(Assuming A2 is the URL in your crawl sheet, and GSC_Data has URLs in Column A and Clicks in Column B)*

### Formula C: Flag Thin Content Automatically
To mark thin pages in your sheet using a simple IF statement:
```excel
=IF(H2<300, "Thin Content - Expand", "Check Depth")
```
*(Assuming H2 contains the Word Count value)*

---

## 🖼️ 4. Example Screenshot Descriptions
*   **Screenshot 1: Screaming Frog Column Configuration Panel**
    *   *Description:* A screen view of Screaming Frog with a red circle highlighting the "Export" button on the top menu bar of the "Internal" tab, and a dropdown menu showing the filter set to "HTML".
*   **Screenshot 2: Filtered Pivot Table in Excel**
    *   *Description:* An Excel spreadsheet showing a pivot table. The rows are filtered by "Status Code" to display only 404 and 301 redirects, with columns showing the corresponding referral source URL to trace where the broken links are located.

---

## 🚫 5. Common Mistakes to Avoid
*   **Exporting Image and Resource URLs:** Forgetting to filter by "HTML" before exporting. This includes images, scripts, and CSS stylesheets in your sheet, cluttering the data.
*   **Assuming Canonical Target is Indexable:** Not checking if the canonical URL points to an active, indexable 200 OK page. If a canonical tag points to a redirected URL, it creates a redirect loop that confuses search engines.
*   **VLOOKUP Exact Match Error:** Forgetting to write `FALSE` at the end of your VLOOKUP formula. If you leave it blank or write `TRUE`, Excel will search for approximate matches, which results in incorrect data mapping.

---

## 📅 6. Expected Outcomes & Timelines
*   **Crawl Export:** Completed within 1 hour of crawl finalization.
*   **Data Cleaning:** Clean the data and isolate the core columns in under 2 hours.
*   **Master Sheet Setup:** Merge GSC performance metrics and crawl metrics together using formulas within the same business day, establishing a single source of truth for the audit.
