# HR Analytics: Employee Attrition & Retention Dashboard

## Executive Summary
This project analyzes employee attrition dynamics across a workforce of **99,990 employees**. Using Microsoft Excel, two transactional datasets (50,000 records each) were appended, cleansed, and modeled to identify core drivers of employee turnover, evaluate high-risk segments, and establish actionable retention strategies.

---

## Key Performance Indicators (KPIs)
* **Total Headcount:** 99,990
* **Active Workforce:** 84,046
* **Total Leavers:** 15,944
* **Overall Attrition Rate:** 15.95%

---

## Dashboard Architecture

### Report 1: Attrition Overview
Focuses on workforce demographics, departmental trends, job roles, salary bands, and tenure distribution.

![Attrition Overview](images/report1_overview.png)

* **Departmental Split:** Sales records the highest attrition rate at **20.59%**, followed by HR at **17.72%** and R&D at **13.65%**.
* **Age Dynamics:** Highest turnover is concentrated in early-career professionals aged **18–25 (35.38%)**, dropping significantly in the **36–45 (9.32%)** bracket.
* **Role Vulnerability:** Sales Representatives experience the steepest attrition (**39.01%**), whereas Research Directors maintain high stability (**2.30%**).
* **Tenure Risk:** Attrition peaks in the first year (**34.53%** for 0 years) and stabilizes significantly after 4+ years of service.

---

### Report 2: Attrition Drivers Analysis
Evaluates operational, compensation, and lifestyle factors influencing employee decisions to leave.

![Attrition Drivers Analysis](images/report2_drivers.png)

* **OverTime Impact:** Employees working overtime experience an attrition rate of **30.27%** versus **10.34%** for non-overtime staff (~3x higher risk).
* **Marital Status:** Single employees exhibit the highest attrition (**25.53%**) compared to married (**12.25%**) and divorced (**9.59%**) staff.
* **Travel Frequency:** Frequent business travelers demonstrate a **24.15%** attrition rate compared to **7.55%** for non-traveling roles.
* **Equity & Stock Options:** Employees with Level 0 stock options leave at **24.39%**, whereas employees holding stock option levels 1 & 2 exhibit lower turnover (6.99%–9.01%).

---

### Report 3: Correlation & Cross-Tabulation Analysis
Cross-evaluates compensation slabs, age demographics, and promotion timelines.

![Correlation & Cross Tabulation](images/report3_correlation.png)

* **Salary Slab Sensitivity:** Compensation below 3k/month shows a severe attrition rate of **28.34%**, dropping to **10.90%** for the 5k–8k bracket.
* **Age vs. Salary Interaction:** In the 18–25 age segment, lower salary brackets account for **43.02%** of attrition share.
* **Promotion Lag:** Sharp attrition spikes occur at years 6–7 (**21.17%**) and year 9 (**22.47%**) post-promotion, indicating retention dips when upward mobility stalls.

---

## Technical Workflow & Excel Implementation
1. **Data Appending & ETL (Power Query):**
   * Imported two separate datasets containing 50,000 employee records each.
   * Merged datasets using `Append Queries` to create a unified 100K-row transactional base.
   * Standardized data formats, eliminated duplicates, and verified zero null attributes across critical IDs.
2. **Feature Engineering & Calculated Categorization:**
   * **Salary Slabs:** Grouped into `<3k`, `3k-5k`, `5k-8k`, `8k-12k`, `12k-16k`, and `16k+`.
   * **Age Demographics:** Categorized into `18-25`, `26-35`, `36-45`, `46-55`, and `55+`.
   * **Tenure Bands:** Binned into `upto 0 year`, `2 to 3`, `4 to 5`, `6 to 10`, and `10+ years`.
3. **Data Modeling & Pivot Calculations:**
   * Built Pivot Tables with custom calculated fields:
     $$\text{Attrition Rate} = \frac{\text{Total Leavers}}{\text{Total Employees}}$$
   * Synced cross-functional Slicers across all three dashboard reports (`Department`, `Gender`, `JobRole`) for synchronized dynamic filtering.

---

## How to Access the Dashboard
Because the complete 100K-row dataset and interactive dashboard exceed standard web preview limits, the full workbook is archived in the repository:
1. Download `HR_Attrition_Analysis.zip` from this repository.
2. Extract the archive to access the full interactive Excel workbook (`.xlsb` / `.xlsx`).
3. Enable macros/content if prompted to interact with the slicers and dynamic charts.

---

## Strategic Retention Recommendations
1. **Workload Restructuring:** Address mandatory overtime in high-exit teams to curb the 30.27% turnover rate.
2. **First-Year Onboarding Interventions:** Focus retention programs on entry-level employees (18–25 age bracket) where first-year attrition reaches 34.53%–35.38%.
3. **Promotion Review Windows:** Re-evaluate mid-tenure career ladders around years 6–7 post-promotion to mitigate mid-career stagnation exits.
