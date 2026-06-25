# Capstone 3 — EmporiUm East Region Sales Analysis
**Author:** Mutize  
**Tool:** Microsoft Power BI  

---

## Project Overview

This project analyzes four years of sales data (2022–2025) for EmporiUm, a virtual student bookstore operating across in-store and online channels. The report was built for the East region sales team — covering Massachusetts, Maine, New Jersey, New York, and Connecticut — to support data-driven business decisions around inventory, category performance, and regional strategy.

---

## Report Link

> 📊 [View the published Power BI report](#) ← _Replace # with your Power BI Service URL_

---

## Video Walkthrough

> 🎥 [Watch the 10-minute project video](#) ← _Replace # with your video link (YouTube, Loom, etc.)_

---

## Key Insights

- **Technology is the top-selling category** in the East region by a significant margin, making it the most critical category for inventory planning.
- **New York drives the largest share of regional revenue**, followed by Massachusetts and New Jersey.
- **Sales peak in August–September** each year, consistent with back-to-school demand, with a secondary spike in January at the start of the spring semester.
- **Top-selling general books** reflect diverse customer interests across fiction, non-fiction, and self-development titles.

---

## Report Pages

| Page | Description |
|------|-------------|
| Page 1 — Sales Overview | Line chart (monthly trend), bar chart (sales by category), and KPI summary cards |
| Page 2 — Regional Highlights | Donut chart (sales by state), top 10 general books table with author names |

---

## Data Sources

| File | Description |
|------|-------------|
| `Capstone3_Sample_Sales.xlsx` | Main sales data — Store Sales, Online Sales, Products, Store Locations, Management Team |
| `book_list.txt` | General audience book titles and author names |

---

## Data Cleaning Summary

The following transformations were applied in Power Query before building the report:

- **Online Sales date columns** — combined three separate Year, Month, Day columns into a single `Transaction Date` column using `#date([Year], [Month], [Day])`
- **State abbreviations** — standardized all state abbreviations (NY, MA, ME, CT, NJ) to full state names in the Store Locations table
- **Trailing spaces** — trimmed the `Category` column in Store Sales to remove a trailing space on "Apparel and Merchandise"
- **Null values** — replaced null entries in the `Category` column with "Unknown"
- **Unified sales table** — appended Store Sales and Online Sales into a single `All Sales` table with a `Sale Type` column (In-Store / Online)
- **Book list parsing** — split book_list.txt into separate `Title` and `Author` columns and removed asterisk formatting; merged Author into the Products table

---

## Repository Contents

```
Capstone_3/
├── README.md
├── Mutize_capstone3.pbix
├── Capstone3_Sample_Sales.xlsx
└── book_list.txt
```

---

## Tools Used

- Microsoft Power BI Desktop
- Power Query (M language)
- DAX (Data Analysis Expressions)
- GitHub
