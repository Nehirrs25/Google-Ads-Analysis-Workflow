# Google-Ads-Analysis-Workflow
Analysis of a month's worth of Google Ads data including cleaning, organization and exploratory work in SQL, full Python workflow including in depth statistical analysis and testing, and an interactive PowerBI dashboard allowing for dynamic visualization of the data on the reader side.

\# Google Ads Data Pipeline \& Analysis



\## 📌 Project Overview

This project demonstrates my ability to take raw marketing data through a complete workflow:  

\- SQL for cleaning, transforming, and creating rollups and efficiency metrics.  

\- Python for statistical testing with regression models.  

\- Tableau for interactive visualization.  



The dataset itself was relatively uniform and low-variance, which meant most results were predictable. The value of this project lies in showing the workflow and tooling integration, taking messy data to the point of report readiness.  





---



\## 🗂 Repository Structure



.

&nbsp;├── Data/

&nbsp;│ ├── raw\_set.csv # Raw Google Ads export

&nbsp;│ ├── staging.csv # Cleaned and standardized data

&nbsp;├── Sql/

&nbsp;│ └── ads\_project\_code.sql # Full SQL script: cleaning, rollups, metrics

&nbsp;│

&nbsp;├── Python/

&nbsp;│ ├── function\_definitions.ipynb # Clean notebook with only functions

&nbsp;│ └── full\_workflow.ipynb # Complete analysis workflow with outputs

&nbsp;│

&nbsp;├── PowerBI/

&nbsp;│ └── ads\_project\_dashboard.pbix # Interactive dashboard for dynamic data visualization

&nbsp;│

&nbsp;├── findings\_notes.md # Raw significance test notes

&nbsp;└── README.md # This file



---



\## 🧹 SQL Code

The SQL script (`sql/google\_ads\_analysis.sql`) handles:  

\- \*\*Cleaning \& standardization\*\*: fixing device names, keyword inconsistencies, date formatting, type conversions, handling blanks/NULLs.  

\- \*\*Rollups\*\*: daily, weekly, device-level, and keyword-level aggregations.  

\- \*\*Efficiency metrics\*\*: ROI, CPC, CPA, profit per click, etc.  

\- \*\*Iterative refinement\*\*: views are sometimes redefined to show the development process.  



The output of this stage is a set of clean tables and views stored in `/data/views/`.  



---



\## 🐍 Python Code

There are two Jupyter notebooks provided for different audiences:  



\- \[`function\_definitions.ipynb`](python/function\_definitions.ipynb)  

&nbsp; A clean reference notebook containing only the function definitions for regression analysis, fully documented with inline comments.  



\- \[`full\_workflow.ipynb`](python/full\_workflow.ipynb)  

&nbsp; The complete analysis workflow, including:  

&nbsp; - Running OLS regressions across keyword–device combinations  

&nbsp; - Filtering significant predictors (`p ≤ 0.002`) on regressions with large numbers of tests for     

&nbsp;   Bonferroni correction

&nbsp; - Subset regression testing on specific keywords  

&nbsp; - Raw outputs and summaries  






\## 🙋 Author

\*Nehir Rogers-Sirin\*  

\[LinkedIn](#) | \[Portfolio](#)  







