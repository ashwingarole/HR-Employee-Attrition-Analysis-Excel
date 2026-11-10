# HR Analytics: Employee Attrition & Retention Dashboard

## Executive Summary
This project analyzes employee attrition dynamics across a workforce of **99,990 employees**. Using Microsoft Excel, two transactional datasets (50,000 records each) were merged, cleansed, and modeled to identify core drivers of employee turnover, evaluate risk segments, and provide actionable retention strategies.

---

## Key Performance Indicators (KPIs)
* **Total Headcount:** 99,990
* **Active Workforce:** 84,046
* **Total Leavers:** 15,944
* **Overall Attrition Rate:** 15.95%

---

## Dashboard Architecture

### Report 1: Attrition Overview
Focuses on workforce demographics, departmental trends, job roles, and tenure distribution.
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
1. **Data Extraction & Appending:**
   * Ingested two distinct datasets containing 50,000 employee records each via **Power Query**.
   * Performed table append (`Append Queries`), deduplication, data type validation, and standard null handling.
2. **Feature Engineering:**
   * Created dynamic salary brackets (`<3k`, `3k-5k`, `5k-8k`, `8k-12k`, `12k-16k`, `16k+`).
   * Grouped age distributions into standardized bins (`18-25`, `26-35`, `36-45`, `46-55`, `55+`).
   * Standardized tenure bands and distance-to-work groupings.
3. **Data Modeling & Calculations:**
   * Leveraged Excel Data Model / Pivot Tables to calculate dynamic measures:
     * `Attrition Rate = [Total Leavers] / [Total Employees]`
     * Active headcount tracking and departmental distribution ratios.
4. **Interactive UI & Visualization:**
   * Configured cross-filtering using synchronized Slicers (`Department`, `Gender`, `JobRole`).
   * Designed layered combo charts (Bar + Line trends) with consistent theme palettes and custom navigation headers.

---

## Strategic Recommendations
1. **Targeted Overtime Management:** Restructure workload allocation for roles requiring persistent overtime to curb the 30.27% exit rate.
2. **Early-Tenure Onboarding:** Implement structured 30-60-90 day check-ins and mentorship programs to reduce first-year turnover (34.53%).
3. **Mid-Level Career Pathing:** Address promotion plateaus around years 6–7 with clear lateral or vertical growth milestones.
4. **Base Pay Benchmarking for Entry Roles:** Review minimum salary slabs (<3k) to align with industry standards and reduce entry-level flight risk.


\### Report 1: Attrition Overview

Focuses on workforce demographics, departmental trends, job roles, and tenure distribution.

!\[Attrition Overview](images/report1\_overview.png)



\* \*\*Departmental Split:\*\* Sales records the highest attrition rate at \*\*20.59%\*\*, followed by HR at \*\*17.72%\*\* and R\&D at \*\*13.65%\*\*.

\* \*\*Age Dynamics:\*\* Highest turnover is concentrated in early-career professionals aged \*\*18–25 (35.38%)\*\*, dropping significantly in the \*\*36–45 (9.32%)\*\* bracket.

\* \*\*Role Vulnerability:\*\* Sales Representatives experience the steepest attrition (\*\*39.01%\*\*), whereas Research Directors maintain high stability (\*\*2.30%\*\*).

\* \*\*Tenure Risk:\*\* Attrition peaks in the first year (\*\*34.53%\*\* for 0 years) and stabilizes significantly after 4+ years of service.



\---



\### Report 2: Attrition Drivers Analysis

Evaluates operational, compensation, and lifestyle factors influencing employee decisions to leave.

!\[Attrition Drivers Analysis](images/report2\_drivers.png)



\* \*\*OverTime Impact:\*\* Employees working overtime experience an attrition rate of \*\*30.27%\*\* versus \*\*10.34%\*\* for non-overtime staff (\~3x higher risk).

\* \*\*Marital Status:\*\* Single employees exhibit the highest attrition (\*\*25.53%\*\*) compared to married (\*\*12.25%\*\*) and divorced (\*\*9.59%\*\*) staff.

\* \*\*Travel Frequency:\*\* Frequent business travelers demonstrate a \*\*24.15%\*\* attrition rate compared to \*\*7.55%\*\* for non-traveling roles.

\* \*\*Equity \& Stock Options:\*\* Employees with Level 0 stock options leave at \*\*24.39%\*\*, whereas employees holding stock option levels 1 \& 2 exhibit lower turnover (6.99%–9.01%).



\---



\### Report 3: Correlation \& Cross-Tabulation Analysis

Cross-evaluates compensation slabs, age demographics, and promotion timelines.

!\[Correlation \& Cross Tabulation](images/report3\_correlation.png)



\* \*\*Salary Slab Sensitivity:\*\* Compensation below 3k/month shows a severe attrition rate of \*\*28.34%\*\*, dropping to \*\*10.90%\*\* for the 5k–8k bracket.

\* \*\*Age vs. Salary Interaction:\*\* In the 18–25 age segment, lower salary brackets account for \*\*43.02%\*\* of attrition share.

\* \*\*Promotion Lag:\*\* Sharp attrition spikes occur at years 6–7 (\*\*21.17%\*\*) and year 9 (\*\*22.47%\*\*) post-promotion, indicating retention dips when upward mobility stalls.



\---



\## Technical Workflow \& Excel Implementation

1\. \*\*Data Extraction \& Appending:\*\*

&#x20;  \* Ingested two distinct datasets containing 50,000 employee records each via \*\*Power Query\*\*.

&#x20;  \* Performed table append (`Append Queries`), deduplication, data type validation, and standard null handling.

2\. \*\*Feature Engineering:\*\*

&#x20;  \* Created dynamic salary brackets (`<3k`, `3k-5k`, `5k-8k`, `8k-12k`, `12k-16k`, `16k+`).

&#x20;  \* Grouped age distributions into standardized bins (`18-25`, `26-35`, `36-45`, `46-55`, `55+`).

&#x20;  \* Standardized tenure bands and distance-to-work groupings.

3\. \*\*Data Modeling \& Calculations:\*\*

&#x20;  \* Leveraged Excel Data Model / Pivot Tables to calculate dynamic measures:

&#x20;    \* `Attrition Rate = \[Total Leavers] / \[Total Employees]`

&#x20;    \* Active headcount tracking and departmental distribution ratios.

4\. \*\*Interactive UI \& Visualization:\*\*

&#x20;  \* Configured cross-filtering using synchronized Slicers (`Department`, `Gender`, `JobRole`).

&#x20;  \* Designed layered combo charts (Bar + Line trends) with consistent theme palettes and custom navigation headers.



\---



\## Strategic Recommendations

1\. \*\*Targeted Overtime Management:\*\* Restructure workload allocation for roles requiring persistent overtime to curb the 30.27% exit rate.

2\. \*\*Early-Tenure Onboarding:\*\* Implement structured 30-60-90 day check-ins and mentorship programs to reduce first-year turnover (34.53%).

3\. \*\*Mid-Level Career Pathing:\*\* Address promotion plateaus around years 6–7 with clear lateral or vertical growth milestones.

4\. \*\*Base Pay Benchmarking for Entry Roles:\*\* Review minimum salary slabs (<3k) to align with industry standards and reduce entry-level flight risk.

