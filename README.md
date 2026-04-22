# **IBM HR Analytics Attrition Dashboard**


---

## Overview

A single-page Power BI dashboard analyzing employee attrition across the IBM HR dataset — built to help a Head of Talent Acquisition and Hiring Operations understand why employees leave, where attrition is concentrated, and which employees are most likely to exit next.

---

## Objective

Conduct a comprehensive analysis of IBM's employee attrition data using Power BI to surface key retention insights and identify optimization opportunities across departments, job roles, compensation bands, and risk profiles — enabling data-driven decisions that reduce turnover and lower rehiring costs.

---

## Key Performance Indicators (KPIs)

| KPI | Value |
|---|---|
| Total Employees | 1,470 |
| Active Employees | 1,233 |
| Attrition Total | 237 |
| Attrition Rate | 16.12% |
| Critical Risk Employees | 53 |

---

## Business Questions

**1. What drives attrition? (Overtime & Compensation)**
- 75% of all 237 departures came from employees working overtime — overtime is the single most controllable retention risk
- 113 of 237 departures came from the lowest salary band — nearly half of all attrition lives in one pay bracket
- Low and Mid earners combined drive 75% of total attrition

**2. Where is attrition highest? (Department & Role)**
- R&D leads in headcount loss with 133 of 237 total departures — more than every other department combined
- 62 Laboratory Technicians departed — the single biggest attrition problem by role
- Sales Executive and Sales Representative follow closely, signaling a Sales retention crisis

**3. Who is most likely to leave next? (Risk Profiles)**
- Critical Risk employees leave at a 58% rate vs 6% for Safe employees — the risk model predicts reality
- 53 employees are currently flagged as Critical Risk Employees across key roles
- Sales Executives lead the at-risk table at 57.14% attrition, followed by Human Resources at 50%

---

## Salary Band Model

A custom Salary Band column was built in Power Query grouping each employee into one of four compensation tiers based on their Monthly Income — Low (≤ 3,000), Mid (3,001 — 6,000), High (6,001 — 10,000), and Very High (10,000+). This eliminated the noise of raw salary figures and made it possible to compare attrition rates cleanly across pay levels. 

---

## Risk Scoring Model

A custom Risk Score was built in Power Query assigning each employee 0–6 points based on known attrition risk factors — Overtime, Low Salary, Low Job Satisfaction, Poor Work-Life Balance, No Stock Options, and Early Tenure. Employees scoring >=4 are flagged as Critical Risk, >=2 as Medium Risk.

---

## Interactivity & Filters

The dashboard includes a dynamic Department slicer enabling stakeholders to isolate any department instantly. Every visual is cross-filtered, clicking any data point automatically updates the entire report, allowing the Head of TA to drill into specific segments without navigating away from the single-page view.

---

## Tools & Technologies

- **Power BI Desktop** — Dashboard development and visualization
- **DAX** — Custom measures and KPI calculations
- **Power Query** — Data transformation and risk scoring model

---

## Dataset
The dataset used is the IBM HR Analytics Employee Attrition & Performance dataset published on Kaggle containing:

- 1,470 employee records across 35 features
- Attrition status, compensation, satisfaction scores, tenure, and role data
- 3 Departments: Research & Development, Sales, Human Resources
- 4 Salary Bands: Low, Mid, High, Very High — derived from MonthlyIncome as a calculated column
- **Source:** [Kaggle — IBM HR Analytics Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Note:** This is a fictional dataset created by IBM for analytics purposes

---

## Conclusion
Leveraging Power BI to analyze IBM HR data reveals that attrition is not random — it is predictable, concentrated, and addressable. Overtime policy, compensation structure, and early tenure engagement are the three most impactful levers available to reduce attrition. The risk scoring model transforms historical patterns into a forward-looking watchlist, giving the Head of Talent Acquisition a concrete starting point for retention intervention before employees decide to leave.

---
