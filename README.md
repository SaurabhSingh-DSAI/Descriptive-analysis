# Descriptive-analysis
# IBM Cognos Analytics – RetailPulse Practicals

A collection of six hands-on practicals completed in **IBM Cognos Analytics**, covering the full reporting workflow: list reports, grouping, filtering, crosstabs, prompt pages, and interactive dashboards.

> **Note:** The practical briefs reference a "RetailPulse" sales package. My submissions were built on the Cognos sample **automobile (Toyota) sales data** available in my environment, with fields such as `Region`, `Model`, `Profit_USD`, `Ex_Showroom_Cost_USD`, `On_Road_Price_USD`, `Discount_USD` and `Gender`. The report structure and techniques follow the practical instructions.

---

## Table of Contents

| # | Practical | Topic | Output |
|---|-----------|-------|--------|
| 1 | Generate a First Report | Intro to Cognos Reporting | [`Practical_1.pdf`](./Practical_1.pdf) |
| 2 | Grouped List Report | Create List Reports | _Add file/screenshot_ |
| 3 | Filter by Region and Date | Focus Reports Using Filters | _Add file/screenshot_ |
| 4 | Region × Product Crosstab | Create Crosstab Reports | [`Practical4.pdf`](./Practical4.pdf) |
| 5 | Sales Prompt Report | Design a Prompt Report | [`Practical_5.png`](./images/Practical_5.png), [`P_5.png`](./images/P_5.png) |
| 6 | Customer Insights Dashboard | Build a Dashboard | [`Dashboard.png`](./images/Dashboard.png) |

---

## Practical 1 – Generate a First Report

**Objective:** Navigate the Cognos Reporting environment and generate a running list report.

**Steps**
1. Open Cognos Analytics → **New > Report**.
2. Select the data package/module as the source.
3. Choose the **List** template.
4. Drag `Region`, and the relevant product and measure columns onto the canvas.
5. Click **Run** to preview live data.
6. Save the report to a personal folder.

**Result:** A list report showing live data by region and model, with the total `Ex_Showroom_Cost_USD` (8,737,397,010) displayed.

📄 Output: [`Practical_1.pdf`](./Practical_1.pdf)

---

## Practical 2 – Build a Grouped List Report

**Objective:** Build a list report, group it, format columns, and add a summarizing footer.

**Steps**
1. Create a new List report.
2. Add Region, Store/Model, Category, Quantity and Amount columns.
3. Group by Region, then by the second-level field (two-level hierarchy).
4. Format the amount as currency; right-align numeric columns.
5. Add a list footer using **Total (sum)**.
6. Insert a page header with the report title and run date; run and save.

**Expected outcome:** Nested group bands, currency formatting, correct group totals, and a page header on every page.

---

## Practical 3 – Filter Sales by Region and Date

**Objective:** Scope a report using a simple filter and an advanced detail filter, then generalise it with a prompt.

**Steps**
1. Open the grouped list report from Practical 2.
2. Add a simple filter: `Region = "North"` (or a region from my data).
3. Add an advanced detail filter for a date range (quarter start to end).
4. Combine both conditions with **AND**.
5. Run and confirm the row count drops.
6. Convert the Region filter into a **prompted filter** for reuse.

**Expected outcome:** Only rows matching both conditions remain; re-running with a different prompt value returns a different region.

---

## Practical 4 – Region × Product Crosstab

**Objective:** Summarise data across two dimensions with multiple measures and summary totals.

**Steps**
1. Start a new report using the **Crosstab** template.
2. Place `Region` on the rows and `Model` on the columns.
3. Drag `Profit_USD` into the crosstab body.
4. Add a second measure beside it.
5. Turn on row and column summary totals.
6. Format as currency, run and save.

**Result:** A crosstab with Region on rows and Model on columns, showing `Profit_USD` per cell, plus a singleton summary of `Discount_USD` (**$113,188,218.00**).

📄 Output: [`Practical4.pdf`](./Practical4.pdf)

---

## Practical 5 – Sales Prompt Report

**Objective:** Design a prompt page with value, date-range and cascading prompts linked to report filters.

**Steps**
1. Open the crosstab report from Practical 4.
2. Insert a new prompt page before the report page.
3. Add a **Value prompt** for Region and a **Date-range prompt** for the period.
4. Add a **cascading prompt** (Model) that depends on the selected Region.
5. Link every prompt to its matching filter.
6. Set default values, add a Finish/OK button, then run and test.

**Result:** A prompt page with three controls – `p Region` (e.g. India), `p_DateRange` (calendar picker) and `p Model` (e.g. Supra) – with OK / Cancel buttons. Submitting returns the crosstab filtered to the chosen values.

| Prompt page | Report output |
|---|---|
| ![Prompt page](./images/Practical_5.png) | ![Prompt report](./images/P_5.png) |

---

## Practical 6 – Customer Insights Dashboard

**Objective:** Assemble a dashboard with a summary card, trend chart, breakdown chart and a shared filter.

**Steps**
1. Create a new Dashboard and connect it to the data module.
2. Add a **summary card** (KPI) widget.
3. Add a **line chart** for a trend over time.
4. Add a **bar chart** for a category breakdown.
5. Add a **Region filter** widget that cross-filters all widgets.
6. Arrange widgets in a clear visual hierarchy and save.

**Result:** A dashboard filtered to **Region = India**, containing:
- **KPI card:** `Profit_USD` total (159M)
- **Bar chart:** `Profit_USD` by `Model`
- **Line chart:** `On_Road_Price_USD` (average) by date, coloured by `Gender`

![Dashboard](./images/Dashboard.png)

---

## Tools & Skills Demonstrated

- IBM Cognos Analytics (Reporting & Dashboards)
- List, grouped and crosstab report design
- Simple and advanced detail filters
- Value, date-range and cascading prompts
- KPI, line and bar chart widgets with cross-filtering
- Data formatting, summaries and page layout

## Repository Structure

```
.
├── README.md
├── Practical_1.pdf
├── Practical4.pdf
├── Practical2/        # add your files
├── Practical3/        # add your files
└── images/
    ├── Practical_5.png
    ├── P_5.png
    └── Dashboard.png
```

## How to View

1. Clone the repo: `git clone <your-repo-url>`
2. Open the PDFs and images directly, or import the reports into your own Cognos Analytics instance.

## Author

**Your Name** – _Course / Roll No. / Institution_
