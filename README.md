<h1 align="center">📊 HR Employee Attrition Analysis</h1>
<p align="center">
  <b>End-to-end HR Analytics project — from raw data to an interactive Excel dashboard</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Excel-Power%20Query%20%7C%20Pivot%20Tables%20%7C%20DAX-217346?logo=microsoftexcel&logoColor=white" />
  <img src="https://img.shields.io/badge/Dataset-1%2C480%20employees%20%C2%B7%2038%20features-blue" />
  <img src="https://img.shields.io/badge/Status-Completed-success" />
  <img src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey" />
</p>

---

## 📌 Overview

This project analyzes an HR dataset of **1,480 employees** to understand the key drivers behind **employee attrition** (turnover), and translates the findings into an **interactive Excel dashboard** that HR / management teams can filter and explore on their own.

The full workflow — cleaning, modeling, and visualization — was built entirely in **Excel** using **Power Query**, the **Data Model / Pivot Tables**, and **DAX measures**, following a structured **Define → Clean → Analyze → Decide** methodology.

> 📄 A full write-up of the methodology (in Arabic) is available in [`docs/HR_Attrition_Analysis_Documentation.docx`](docs/HR_Attrition_Analysis_Documentation.docx).

---

## 🎯 Business Question

> Which employee segments are most likely to leave the company, and what factors are driving that attrition?

---

## 🗂️ Dataset

| | |
|---|---|
| **Rows** | 1,480 employees |
| **Columns** | 38 features |
| **Target variable** | `Attrition` (Yes / No) |
| **Key dimensions** | Department, Job Role, Job Level, OverTime, Marital Status, Business Travel, Salary Slab, Stock Option Level, Satisfaction & Performance scores |

A complete data dictionary (column name → business meaning) is documented in the **Meta_Data** sheet of the workbook.

---

## 🛠️ Tools & Techniques

- **Power Query** — data type correction, missing value treatment
- **Excel Data Model / Pivot Tables** — data summarization
- **DAX** — custom measures for the dashboard KPIs
- **Excel Charts & Slicers** — interactive dashboard build

---

## 🧭 Methodology

**1. Define**
Understood the business context and explored the dataset structure, confirming `Attrition` as the focal metric around which the whole analysis is built.

**2. Clean / Transform (Power Query)**
- Corrected data types for all columns.
- Found missing values in `YearsWithCurrManager`.
- Instead of blindly imputing the **mean**, the distribution was checked first using a **Histogram** and **Box Plot** — which revealed significant outliers, making the mean unreliable.
- Imputed missing values with the **median (3)** instead of the mean (≈4.12), based on that evidence.

**3. Analyze (Pivot Table + DAX)**
Built a Pivot Table on the cleaned data and created DAX measures to power the dashboard dynamically:

| Measure | Value |
|---|---|
| Total Employees | 1,480 |
| Attrition Rate | 16.08% |
| OverTime Rate | 28.24% |
| Satisfaction Score | 2.73 |
| Average Monthly Income | 6,505 |
| Average Tenure (Years) | 7 |

**4. Decide (Dashboard)**
Built a 3-page interactive dashboard — **Overview**, **Department**, and **Employee** — with slicers for Department, Job Role, Job Level, and Salary Slab.

---

## 📈 Key Insights

- 🔴 **OverTime is the strongest attrition driver found**: employees who work overtime leave at **~3x** the rate of those who don't (**30.62%** vs **10.36%**).
- 🔴 **Sales** has the highest attrition rate among departments (**20.67%**), followed by HR (**19.05%**) and R&D (**13.75%**).
- 🟢 The overall company-wide attrition rate stands at **16.08%**.

**Recommendation:** Investigate workload and staffing levels in Sales, and review overtime policy — since overtime shows a much stronger relationship with attrition than department alone.

---

## 📊 Dashboard Preview

<p align="center">
  <img src="assets/dashboard_overview.png" width="800" alt="Dashboard Overview page" />
</p>

> *(Replace the image above with a screenshot of the `OverView` page — export it from Excel and place it in an `assets/` folder.)*

---

## 📁 Repository Structure

```
HR-Attrition-Analysis/
│
├── data/
│   └── HR_Analytics.csv                 # Raw dataset
│
├── dashboard/
│   └── Dashboard.xlsm                   # Excel file (Power Query + Pivot + DAX + Dashboard)
│
├── docs/
│   └── HR_Attrition_Analysis_Documentation.docx   # Full methodology write-up (Arabic)
│
├── assets/
│   └── dashboard_overview.png           # Dashboard screenshots
│
└── README.md
```

---

## 🚀 How to Explore

1. Download `dashboard/Dashboard.xlsm`.
2. Open it in Excel (macros/Power Query need to be enabled).
3. Use the slicers on each page (Department, Job Role, Job Level, Salary Slab) to filter the KPIs and charts interactively.

---

## 👤 Author

**Hozaifa Alzohare**
Freelance Data Analyst | AI & Data Science Student

- 🔗 LinkedIn: [linkedin.com/in/hozaifa-alzohare](https://linkedin.com/in/hozaifa-alzohare)
- 📧 Email: hozaifaalzohare@gmail.com

---

<p align="center"><i>If you found this project useful, consider giving it a ⭐ on GitHub!</i></p>
