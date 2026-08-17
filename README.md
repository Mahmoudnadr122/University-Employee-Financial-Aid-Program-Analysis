# 🎓 University & Employee Financial Aid Program Analysis (Power BI)

## 📌 Project Overview
An interactive and end-to-end **Power BI Dashboard** developed to analyze the **County Tuition Assistance & Financial Aid Program**. The project investigates organizational spending, employee education demand, degree preferences, and institutional funding distributions across various public departments.

---

## 📊 Key Performance Indicators (KPIs)
* **Total Cost (Spend):** **$3.43M** allocated across tuition reimbursements.
* **Total Requests:** **4,368** course reimbursement requests submitted.
* **Unique Courses:** **3,291** distinct courses pursued.
* **Unique Schools / Institutions:** **370** partner colleges & universities.

---

## 📈 Key Insights & Analytical Findings

### 1. Education Demand & Cost per Request across Degree Types
* **Highest Demand:** **Bachelors (BA/BS)** degrees represent the highest volume (**1,393 requests**, Avg Cost: **$726**), followed by **Masters** programs (**918 requests**, Avg Cost: **$1,154**).
* **Cost Drivers:** Doctoral programs (**Ph.D. DCS** at **$1,352** avg cost; **Juris Doctor** at **$1,343** avg cost) represent the highest per-request expenditure despite lower applicant volumes (37 and 35 requests respectively).

### 2. Departmental Expenditure Breakdown
* **Police Department:** The largest consumer of tuition assistance, accounting for **$1.12M (39.24%)** of total funds.
* **Fire / Rescue Services:** The second highest spending department with **$0.68M (23.69%)**.
* **Health & Human Services:** Comprises **$0.62M** in financial aid assistance.
* **Other Major Departments:** Correction & Rehabilitation ($0.20M), Transportation ($0.17M), and General Services ($0.08M).

### 3. Academic Institutions & Funding Flow
* Top-funded universities lead institutional allocations, with the top-ranked university receiving over **$0.53M** in approved aid payments.

---

## 🧮 DAX Measures & Data Model

```dax
// 1. Total Spend
Total_Cost = SUM('Tuition_Assistance'[Cost])

// 2. Total Approved Requests
Total Requests = COUNTROWS('Tuition_Assistance')

// 3. Average Cost per Request
Average Cost = AVERAGE('Tuition_Assistance'[Cost])

// 4. Unique Courses
Unique Courses = DISTINCTCOUNT('Tuition_Assistance'[Course Title])

// 5. Unique Academic Institutions
Unique Schools = DISTINCTCOUNT('Tuition_Assistance'[School])
