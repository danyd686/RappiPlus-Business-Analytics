![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
# 🛵 RappiPlus — From Data to Business Decisions
---

## 📌 Project Overview

This project analyzes RappiPlus transactional, customer activity, marketing, funnel, and experimentation data to evaluate business performance and identify opportunities for improvement.

The analysis covers data quality, financial performance, conversion funnels, customer retention, and A/B testing, combining SQL, Python, and Tableau to transform raw data into actionable business insights.

---

## 🎯 Business Problem

RappiPlus needs to understand how its business is performing across different stages of the customer journey.

The project addresses six key business questions:

1. Can we trust the available data?
2. Are we generating profit after costs and marketing investment?
3. Where are users dropping out of the conversion funnel?
4. Do users return after registration?
5. Did the checkout interface change produce a measurable impact?
6. How can these insights be communicated clearly to business stakeholders?

---
### 🚀 My Contribution to the Project

* Performed **data cleaning and validation** using Python and Pandas.
* Developed **SQL analyses** for profitability, customer funnels, and retention.
* Conducted **A/B testing** using statistical analysis.
* Built an interactive **Tableau dashboard** to communicate key business insights.
* Translated data into **actionable business recommendations**.
---
# 🔄 Analysis Process
# 1. 🧹 Data Cleaning & Quality Assurance

The first stage focused on validating and preparing the datasets for analysis.

### Keys and learning

- Identified and removed duplicate orders.
- Investigated missing values.
- Recovered missing product categories using the product catalog.
- Standardized category names and data types.
- Converted date fields to appropriate formats.
- Investigated negative quantities and transaction values.
- Recovered missing marketing channel information.
- Checked for sentinel values such as `-999` and `999`.
- Performed final data-quality checks.
- Learned to translate analytical findings into clear business recommendations.
- Improved data storytelling and dashboard design using Tableau.

### Final Orders Dataset

| Metric | Result |
|---|---:|
| Orders | 25,000 |
| Columns | 12 |
| Duplicate rows | 0 |
| Missing quantities | 50 |
| Missing unit prices | 50 |

The remaining missing quantity and price values could not be reliably recovered from the available data and were documented rather than artificially imputed.

---

## 2. 💰 Financial Performance & Profitability

Key financial metrics were calculated using transaction-level data and product costs.

### Main KPIs

| Metric | Result |
|---|---:|
| Revenue | **$51.99M** |
| Known Costs | **$43.12M** |
| Marketing Spend | **$2.87M** |
| Final Profit | **$5.99M** |
| Average Ticket | **$2,079.50** |
| Average Products per Order | **7.12** |

Profitability was also analyzed by:

- Product
- Category
- Country
- Device

This analysis helped distinguish between sales volume and actual profitability.

---

## 3. 📉 Conversion Funnel Analysis

A sequential funnel was created using user event timestamps to ensure that each stage occurred after the previous stage.

| Funnel Stage | Users | Conversion |
|---|---:|---:|
| First Visit | 7,796 | — |
| Select Item | 4,055 | 52.01% |
| Add to Cart | 1,267 | 31.25% |
| Begin Checkout | 342 | 26.99% |
| Add Payment Info | 82 | 23.98% |
| Purchase | 8 | 9.76% |

### Overall Conversion

**First Visit → Purchase: 0.10%**

The largest observed drop occurred between **Add Payment Info → Purchase**, with a **90.24% abandonment rate**.

---

## 4. 🔄 Customer Retention — Cohort Analysis

Users were grouped into monthly registration cohorts and analyzed according to weekly activity after registration.

Retention was measured at:

- Week 1
- Week 2
- Week 3

Weekly retention remained approximately within the **40%–44% range** during the first three weeks across the analyzed cohorts.

The analysis did not show a sustained decline from Week 1 to Week 3 across all cohorts.

---

## 5. 🧪 A/B Testing

The final stage evaluated whether a checkout UI modification produced a statistically significant difference in conversion.

### Hypotheses

**H₀:** There is no statistically significant difference in conversion between the control and treatment groups.

**H₁:** There is a statistically significant difference in conversion between the control and treatment groups.

A **two-proportion z-test** was used with a significance level of **α = 0.05**.

### Experiment Results

| Variant | Users | Conversions | Conversion Rate |
|---|---:|---:|---:|
| Control | 4,965 | 779 | 15.69% |
| Treatment | 5,035 | 820 | 16.29% |

### Statistical Test

- Observed difference: **+0.60 percentage points**
- z-statistic: **-0.8133**
- p-value: **0.4161**
- Significance level: **0.05**

The experiment did not provide sufficient statistical evidence of a difference in conversion between the two variants at the selected significance level.

---

# 🔑 Key Findings

### 💰 Financial Performance

- RappiPlus generated approximately **$51.99M in revenue**.
- Final profit after known costs and marketing spend was approximately **$5.99M**.
- Marketing investment totaled approximately **$2.87M**.
- Revenue volume and profitability differed considerably across categories and products.

### 📉 Conversion Funnel

- **7,796** users entered the analyzed funnel.
- **8** users completed a purchase through the sequential funnel.
- Overall first-visit-to-purchase conversion was approximately **0.10%**.
- The largest observed stage abandonment was between payment information and purchase.

### 🔄 Customer Retention

- Weekly retention remained relatively stable at approximately **40%–44%** during the first three weeks.
- Cohort behavior varied by registration month.

### 🧪 Experimentation

- Treatment conversion was **16.29%** compared with **15.69%** for control.
- The observed difference was **0.60 percentage points**.
- The statistical test did not provide sufficient evidence of a significant difference at α = 0.05.

---

# 📊 Tableau Dashboard

The final analysis was transformed into an interactive Tableau Public dashboard.

## Overview Ejecutivo

The executive dashboard includes:

- Revenue
- Final Profit
- Marketing Spend
- Average Ticket
- Average Products per Order
- Monthly Revenue
- Profit by Category
- Revenue by Product
- Category filter
- Country filter
- Device filter

## Detalle de Ventas

The detailed dashboard includes:

- Order-level detail
- Product
- Category
- Quantity
- Revenue
- Cost
- Profit
- Conditional Profit formatting
- Quantity sold by product
- Date filter
- Country filter
- Category filter
- Device filter
- Interactive product filtering

### 🔗 Interactive Dashboard

[View RappiPlus Dashboard on Tableau Public](https://public.tableau.com/app/profile/danilo.gallego/viz/dashboardrappi/overviewejecutivo?publish=yes)

---

### 🛠️ Tools & Technologies

* **Python & Pandas** — Data cleaning, transformation, exploratory analysis, and KPI calculations.
* **SQL** — Customer funnel, cohort retention, profitability, and business performance analysis.
* **Tableau** — Interactive dashboard development and business data visualization.
* **Excel** — Data preparation, validation, and supporting business analysis.
* **Jupyter Notebook** — Documentation and execution of the end-to-end analysis workflow.
* **Statistical Analysis** — A/B testing and evaluation of conversion rate differences.

---
Danilo Gallego López

Data Analyst | Reporting | Business Intelligence | Sales Analytics

📧 danyd686@gmail.com

🔗 LinkedIn: www.linkedin.com/in/danilogallego

---
# 📂 Repository Structure

```text
RappiPlus-Data-to-Business-Decisions/
│
├── README.md
│
├── notebooks/
│   └── RappiPlus_Analisis_Final.ipynb
│
├── data/
│   ├── orders_clean.csv
│   ├── catalog_clean.csv
│   ├── marketing_clean.csv
│   └── experiment_checkout_ui.csv
│
├── sql/
│   ├── funnel_analysis.sql
│   ├── cohort_analysis.sql
│   └── ab_testing.sql
│
└── images/
    ├── overview_ejecutivo.png
    └── detalle_ventas.png

--- 
