# 📊 QA Metrics Dashboard — Power BI Project

> **Tracking defect trends, resolution performance, and test execution quality across 8 agile sprints for an e-commerce platform redesign.**

![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-%2307405e.svg?style=for-the-badge&logo=sql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Business Analysis](https://img.shields.io/badge/Business%20Analysis-Informational?style=for-the-badge&logo=datadog&logoColor=white)
![Agile](https://img.shields.io/badge/Agile-%23FF6F00?style=for-the-badge&logo=agile&logoColor=white)
![Lean Six Sigma](https://img.shields.io/badge/Lean%20Six%20Sigma-007CBA?style=for-the-badge)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)


## 🚀 Live Dashboard [![Open App](https://img.shields.io/badge/Open%20App-Streamlit-orange?logo=streamlit)](https://emp-demo-distt.streamlit.app/?embed_options=light_theme,show_colored_line,show_padding)


[![Watch the demo](ezgif.gif)](https://emp-demo-distt.streamlit.app/?embed_options=light_theme,show_colored_line,show_padding)
> Click the image above to open the live dashboard!

## 🧩 Problem Statement

Quality Assurance teams generate enormous amounts of test data — defect logs, sprint results, SLA timers — but this data often lives in spreadsheets with no visibility into patterns over time. Without clear metrics, QA leads and project managers struggle to answer questions like:

- Are we resolving defects fast enough to meet SLA targets?
- Which modules are producing the most critical bugs?
- Is our test pass rate trending up or down sprint over sprint?
- How many defects are sitting unresolved beyond their SLA window?

This project builds a **fully interactive Power BI dashboard** that transforms raw QA data into actionable insight across four key dimensions.

---

## 🎯 Dashboard Pages

### 1. 📌 Executive Summary
High-level KPIs at a glance:
- Total defects logged vs resolved
- Overall resolution rate
- SLA breach rate
- Average test pass rate across all sprints

### 2. 🐛 Defect Analysis
- Defect volume by sprint and severity (Critical / High / Medium / Low)
- Module-level defect density heatmap
- Defect status distribution (Open / In Progress / Resolved / Closed / Reopened)
- Resolution rate trend line across sprints

### 3. ⏱️ SLA & Aging Tracker
- Open defects bucketed by aging tier (Within SLA / At Risk / Breached)
- SLA breach count by severity and sprint
- Average days to resolve by priority
- Breach rate trend over time

### 4. ✅ Test Execution
- Test cases planned vs executed per sprint
- Pass / Fail / Blocked breakdown by module
- Sprint-over-sprint execution coverage
- Pass rate trend with target reference line

---

## 📁 Repository Structure

```
qa-metrics-dashboard/
│
├── data/
│   └── QA_Metrics_Dashboard.xlsx     # Source data (5 sheets, 8 sprints)
│
├── dashboard/
│   └── QA_Metrics_Dashboard.pbix     # Power BI report file
│
├── screenshots/
│   └── (add screenshots after publishing)
│
└── README.md
```

---

## 📂 Data Model

The Excel workbook contains five structured sheets:

| Sheet | Description | Rows |
|---|---|---|
| `Defects_Log` | Individual defect records with severity, status, dates | ~200 |
| `Sprint_Summary` | Aggregated KPIs per sprint with formulas | 8 |
| `Defect_Aging` | Open defects only, bucketed by SLA status | ~50 |
| `Test_Execution` | Test case results by sprint and module | 64 |
| `KPI_Summary` | Overall project KPIs with targets and status | 8 |

### Key Fields

- **Defect ID** — Unique identifier (DEF-XXXX)
- **Sprint** — Sprint 1 through Sprint 8
- **Severity** — Critical / High / Medium / Low
- **Status** — Open / In Progress / Resolved / Closed / Reopened
- **Days Open** — Calculated field for aging and SLA analysis
- **SLA Breach** — Yes/No based on severity-specific SLA thresholds
- **Pass Rate** — Test execution pass percentage per sprint/module

### SLA Thresholds Used

| Severity | SLA Target |
|---|---|
| Critical | 2 days |
| High | 5 days |
| Medium | 10 days |
| Low | 20 days |

---

## 🔧 How to Use

### Step 1 — Open the data
1. Download `QA_Metrics_Dashboard.xlsx` from the `/data` folder
2. Review the five sheets to understand the data structure

### Step 2 — Connect Power BI
1. Open `QA_Metrics_Dashboard.pbix` in Power BI Desktop
2. Go to **Transform Data → Data Source Settings**
3. Update the file path to point to your local copy of the Excel file
4. Click **Refresh** — all visuals will populate

### Step 3 — Explore
Use the sprint slicer and severity filters to drill into any combination of data across all four dashboard pages.

---

## 💡 Key Insights from the Data

- **Critical defects in the Payments module** showed the highest SLA breach rate — indicating a need for earlier detection or dedicated triage capacity
- **Pass rates improved from Sprint 1 to Sprint 6** before dipping slightly in Sprint 7-8, correlating with a module expansion into Notifications and Search
- **Defect reopening rate stayed below 5%** — suggesting good root cause resolution practices
- **SLA compliance exceeded 90%** for Medium and Low severity defects throughout the project

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Power BI Desktop | Dashboard design and publishing |
| Microsoft Excel | Data source and KPI calculations |
| Power Query | Data transformation and modelling |
| DAX | Calculated measures and KPIs |

---

## 👤 About

Built by **Swarleen Bhamra** as part of a QA analytics portfolio project, demonstrating the application of data visualisation skills to real-world quality engineering workflows.

📎 Portfolio: [swarleen.com](https://www.swarleen.com)
🔗 LinkedIn: [linkedin.com/in/swarleenbhamra](https://linkedin.com/in/swarleenbhamra)

---

## 📬 Feedback

Found this useful or have suggestions? Feel free to open an issue or connect on LinkedIn!
