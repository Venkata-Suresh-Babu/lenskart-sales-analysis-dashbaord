# Retail Sales Analytics Dashboard — Lenskart-Themed Dataset

**Power BI | DAX | Power Query | KPI reporting | Sales analysis**

An independent portfolio project using a Lenskart-themed retail dataset. **This is a practice/portfolio analysis, not an official Lenskart report or a claim about the company's actual performance.**

## Business question

How can a retail analyst monitor revenue, products, channels, locations, discounts, and customer mix in one report, then drill down to identify patterns worth investigating?

## What I built

- A **four-page Power BI report**: Overview, Finance, Category, and Insights.
- KPI cards for order/sales metrics, quantity, revenue, average customer age, average discount, and average unit price.
- Revenue views by state, year, sales channel, product category, customer gender, and payment method.
- Product-category analysis of sales, quantity mix, discounts, and month-to-month patterns.
- Interactive filters for year, state, product category, customer gender, store type, sales channel, and payment method.
- A written Insights page that summarizes descriptive findings.

The included `.pbix` file contains the report. Its model diagram shows a **single-table model** (`Lenskart India`), rather than a star schema. It demonstrates dashboard development and DAX reporting; I do **not** present this particular report as proof of a star-schema implementation.

## Data and tools

| Item | Details |
| --- | --- |
| Dataset | `Lenskart India.csv`, included in this repository |
| Reporting tool | Power BI Desktop |
| Transformations | Power Query |
| Calculations | DAX measures |
| Output | Four-page report, PDF exports, and screenshots |

The original provenance and representativeness of the dataset have not been independently established. Findings below refer only to the **supplied dataset**, not the retailer's real business.

## Report pages

1. **Overview:** High-level KPIs and revenue comparisons by geography, year, and channel.
2. **Finance:** Sales and revenue measures, gross/discount views, product and payment breakdowns.
3. **Category:** Product-level mix, discounts, and monthly patterns.
4. **Insights:** A concise interpretation of the report's descriptive results.

### Preview

![Overview dashboard](https://github.com/user-attachments/assets/02d68841-5e90-4097-ae28-9fe4bf04078a)

![Finance dashboard](https://github.com/user-attachments/assets/39f345b4-c8f3-47f9-aa0d-b7ec113dfdc5)

![Category dashboard](https://github.com/user-attachments/assets/3bea8102-7310-4d64-9950-db1405cafc72)

![Insights page](https://github.com/user-attachments/assets/2e216222-d9ab-4755-b86b-b34b84902ad1)

## Findings shown in the current report

The dashboard currently displays **₹784.36 million (approximately ₹78.44 crore)** as its revenue KPI. This is a displayed report value, not an independently audited financial figure.

The project's existing visualizations and notes indicate:

- Online is the leading sales channel **within the sample dataset** by reported revenue.
- Kerala, Madhya Pradesh, and Odisha appear among the leading states.
- The reported yearly sales distribution is strongest in 2023 and 2024.
- Eyeglasses contribute the largest **share of units/sales shown in the dataset**. This must not be described as actual company-wide *market share*.

These are descriptive findings, not proof of causation, growth produced by the dashboard, or business actions taken by a real organization.

## What this project demonstrates

- Translating business questions into dashboard KPIs and comparisons.
- Developing and using DAX measures in a Power BI report.
- Presenting measures using cards, bar/column/line charts, maps, tables, and interactive slicers.
- Explaining visual patterns with appropriate qualifications.

## Reproduction and technical checks

1. Open `lenskart sales analysis dashboard.pbix` in Power BI Desktop.
2. If prompted for a source file, repoint the query to `Lenskart India.csv` from this repository and refresh.
3. Check that measures respond correctly to slicers and that record counts match the source after cleaning.
4. Review the specific DAX definitions for **Total orders**, **Total sales**, **Total revenue**, **Total Gross Sales**, **Total Net Sales**, **Total Discount**, and **Avg. Discount %** before reusing the KPIs in another report.
5. When comparing discount rates, use a clearly defined **rate** (with numerator and denominator), rather than inferring rates from absolute discount totals.
6. Check whether the reporting grain represents orders, order lines, or another unit, and use the corresponding label on KPI cards.

The DAX expressions stored inside the report model have **not yet been independently audited** in this portfolio review. I will avoid claims of optimized performance or verified financial accuracy until those checks are completed.

## Next planned improvements

- Document the key DAX expressions and their units/denominators in a small measures table.
- Document the Power Query applied steps and row-count checks.
- Resolve any ambiguous KPI labels (especially total sales versus total orders).
- Optionally redesign a separate version using fact and dimension tables to demonstrate star-schema modeling.
