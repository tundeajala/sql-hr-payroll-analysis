# Capstone HR & Global Payroll Analysis (SQL)

![header overview](header-image.png)
---

## Executive Summary
This project analyzes a global workforce database using SQL to uncover insights into payroll distribution, staffing structure, and talent segmentation.

Key findings include:
- Executive and senior management roles earn **average salaries above $12,000**
- Several job titles have **zero employees**, indicating structural gaps
- High earners represent a critical segment for **leadership development**

---

## Business Context
HR and Finance teams require a centralized, data-driven approach to:
- Monitor payroll costs  
- Evaluate departmental efficiency  
- Identify workforce gaps  

This project replaces manual reporting with SQL-driven analysis, enabling faster and more accurate decision-making.

---

## Objectives
This analysis answers the following business questions:

- Which departments have the highest and lowest headcount?
- What is the total and average salary by department and country?
- How are employees distributed across salary bands?
- Which job titles currently have zero employees?
- Which employees earn above the global average?

---

## Data Overview
- **Database Schema:** `capstone`
- **Core Tables:**
  - employees
  - departments
  - jobs
  - countries
- **Relationships:**
  - Linked via `department_id`, `job_id`, and `country_id`

---

## Key Metrics Snapshot
- Global Workforce: Multi-country dataset
- High Salary Threshold: $10,000+
- Executive Salary Benchmark: $12,000+
- Salary Bands: Low, Medium, High

---

## Key Findings
- **Payroll Concentration:**
  - Certain countries account for a disproportionate share of total salary expenditure

- **Salary Segmentation:**
  - Employees are clearly distributed into Low, Medium, and High salary bands

- **Vacant Roles:**
  - Multiple job titles have no assigned employees, indicating hiring gaps

- **Departmental Load:**
  - Headcount analysis highlights resource-heavy departments

---

## Data Cleaning and Transformation (SQL)

- **Aggregation:**
  - Used `GROUP BY` to summarize salary and headcount data

- **Rounding:**
  - Applied `ROUND(AVG(salary), 2)` for consistent financial reporting

- **Conditional Logic:**
  - Created salary bands using `CASE`:
    - Low (< $5,000)
    - Medium ($5,000–$10,000)
    - High (> $10,000)

- **Joins:**
  - Combined tables using `INNER JOIN` and `LEFT JOIN` for relational analysis

---

## Detailed Analysis

### Headcount Analysis
![workforce distribution](workforce-distribution.png)

### Salary Analysis
![(salary comparison](salary-comparison.png)

### Salary Segmentation
![salary bands for employees](salary-bands-for-employees.png)

### Organizational Structure
![country level analysis](country-level-analysis.png)

### High Earners Analysis
![high earners](high-earners.png)

###  High-Paying Job Roles (CTE)
![job role analysis](job-role-analysis.png)

###  Payroll Distribution
![salary growth trend](salary-growth-trend.png)

###  Structural Gaps
![workforce gaps](workforce-gaps.png)


## Key SQL Techniques Used
- INNER JOIN and LEFT JOIN
- GROUP BY and Aggregations
- Subqueries
- Common Table Expressions (CTEs)
- CASE statements for segmentation

  ## Conclusion
This project demonstrates how SQL can be used to transform relational HR data into actionable insights.
By analyzing payroll distribution, workforce structure, and salary segmentation, the organization can improve hiring strategy, optimize payroll costs, and identify high-value talent for leadership development.
