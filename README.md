# Google-Ads-Analysis-Workflow

This project simulates a full marketing-analytics workflow using a raw Google Ads export, from SQL cleaning to Python statistical modeling to a Power BI dashboard designed for interactive performance exploration.

---

## 📊 Google Ads Data Pipeline & Analysis

### 📌 Project Overview

This project processes uncleaned Google Ads data through SQL, Python, and Power BI to identify efficiency patterns and build a transparent performance dashboard. That entails:

- SQL for cleaning, transforming, and creating rollups and efficiency metrics.  
- Python for statistical testing with regression models.  
- PowerBI for the creation of an interactive visual dashboard.  

The dataset itself was relatively uniform and low-variance, which meant most results were predictable. The value of this project lies in showing the workflow and tooling integration, taking messy data to the point of report readiness.  

---

## 🌐 Data Source

The raw Google Ads export used in this analysis is publicly available as the **Google Ads Sales Dataset** on Kaggle by **Ganesh Nayak**.  
[https://www.kaggle.com/datasets/nayakganesh007/google-ads-sales-dataset](https://www.kaggle.com/datasets/nayakganesh007/google-ads-sales-dataset)


--- 

## 🗂 Repository Structure


```plaintext
.
├── Data/
│   ├── raw_set.csv                    # Raw Google Ads export
│   ├── staging.csv                    # Cleaned and standardized data
│
├── Sql/
│   └── ads_project_code.sql           # Full SQL script: cleaning, rollups, metrics
│
├── Python/
│   ├── function_definitions.ipynb     # Clean notebook with only functions
│   └── full_workflow.ipynb            # Complete analysis workflow with outputs
│
├── PowerBI/
│   └── ads_project_dashboard.pbix     # Interactive dashboard for dynamic data visualization
│
├── findings_notes.md                  # Raw significance test notes
└── README.md                          # This file

---
```
## 🧹 SQL Code

The SQL script (`sql/google_ads_analysis.sql`) handles:  

- Cleaning & standardization: fixing device names, keyword inconsistencies, date formatting, type conversions, handling blanks/NULLs.  
- Rollups: daily, weekly, device-level, and keyword-level aggregations.  
- Efficiency metrics: ROI, CPC, CPA, profit per click, etc.  
- Iterative refinement: views are sometimes redefined to show the development process.  

---

## 🐍 Python Code

There are two Jupyter notebooks provided for different audiences:  

- [`function_definitions.ipynb`](python/function_definitions.ipynb)  
  A clean reference notebook containing only the function definitions for regression analysis, fully documented with inline comments.  

- [`full_workflow.ipynb`](python/full_workflow.ipynb)  
  The complete analysis workflow, including:  
  - Running OLS regressions across keyword–device combinations  
  - Filtering significant predictors (`p ≤ 0.002`) on regressions with large numbers of tests for  
    Bonferroni correction  
  - Subset regression testing on specific keywords  
  - Raw outputs and summaries  

---

## 📊 PowerBI Dashboard

The PowerBI dashboard (`PowerBI/ads_project_dashboard.pbix`) provides an interactive visualization layer for the cleaned and analyzed data.  

It includes drop-down menus and data slicers for **dynamic customization** of visuals, allowing the viewer to:  
- Adjust the level of granularity across keyword and device categories.
- Choose which measures each visual displays, such as impressions, clicks, cost, ROI, or profit per click.  

This interactivity allows users to explore patterns in performance data intuitively and tailor the visual presentation to specific analytical questions or reporting needs.  

---

## 📑 Findings Notes

The `findings_notes.md` file contains the raw significance test results generated from the regression analyses.  

The dataset itself was largely uniform and low-variance, yielding few meaningful trends. While the dataset showed limited variance — typical of synthetic campaign data — The tests serve to illustrate proper regression workflows and significance interpretation.

---


## 🙋 Author

**Nehir Rogers-Sirin**  
[LinkedIn](https://www.linkedin.com/in/nehirrs)
