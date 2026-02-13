# 🏥 Healthcare Financial Performance & Cost Optimization Analytics
## 📌 Project Overview

This project analyzes hospital financial performance using real-world healthcare financial reporting data from the CMS Hospital Provider Cost Report dataset.

The objective is to transform complex regulatory financial reporting data into executive decision intelligence to support cost optimization, profitability improvement, and operational efficiency strategy.

## 🎯 Business Objectives

- Identify profit vs loss hospitals
- Detect high financial risk regions
- Evaluate operational efficiency using infrastructure utilization metrics
- Support data-driven healthcare financial strategy

## 📂 Real World Dataset

- Dataset: Hospital Provider Cost Report
- Source: Data.gov (US Government Open Data Portal)
- Publisher: Centers for Medicare & Medicaid Services (CMS)

Dataset Includes:

- Hospital Revenue
- Operating Costs
- Net Income
- Bed Capacity
- Fiscal Reporting Period

## 🧱 Project Architecture
Raw Data → Python Cleaning → SQL Analysis → Power BI Dashboard → Business Case Study

## 🛠 Tools & Technologies
Tool	Purpose
- Python (Pandas)	and Google Sheet for Data Cleaning
- SQL (MySQL)	Financial Analysis
- Power BI	Dashboard Visualization
  - DAX	KPI Calculations

Create KPI Metrics
<pre>
df_final["profit_margin"] = (
    df_final["net_income_from_service_to_patients"] /
    df_final["total_patient_revenue"]
) * 100
</pre>
<pre>
df_final["cost_to_revenue_ratio"] = (
    df_final["total_costs"] /
    df_final["total_patient_revenue"]
)
</pre>
<pre>
df_final["revenue_per_bed"] = (
    df_final["total_patient_revenue"] /
    df_final["number_of_beds"]
)
</pre>

## 📈 Power BI Dashboard Development
Core KPI Measures
- Total Revenue
  <pre>
  Total Revenue = SUM(Data[total_patient_revenue])
</pre>

- Total Cost
  <pre>
  Total Cost = SUM(Data[total_costs])
</pre>

- Total Profit
  <pre>
  Total Profit = SUM(Data[net_income])
</pre>

- Profit Margin %
  <pre>
  Profit Margin % = DIVIDE([Total Profit], [Total Revenue]) * 100
</pre>

## 📊 Dashboard Pages
Page 1 — Financial Overview

- KPI Cards
- Revenue vs Cost vs Profit
- Revenue by State
- Profit by State

Page 2 — Profitability & Efficiency

- Revenue Per Bed
- Cost Per Bed
- Efficiency Scatter Plot

Page 3 — Risk & Opportunity

- Loss vs Profit Hospital Counts
- Risk Distribution

Page 4 — Performance Deep Dive

- Waterfall Financial Flow
- Heatmap Matrix
- Geographic Map
- Profit Distribution

## 📊 Key Analytical Findings

- Revenue growth does not guarantee profitability
- Cost structure is primary profit driver
- Profitability varies significantly across regions
- Operational efficiency drives financial performance
- Healthcare operates on thin margins

## 🚀 Strategic Recommendations
- Cost Optimization
- Benchmark hospital operating costs
- Identify top cost drivers
- Regional Strategy
- State-level performance monitoring
- Region-specific cost programs
- Efficiency Optimization
- Monitor Revenue Per Bed KPI
- Optimize infrastructure utilization

## 📊 Business Value Delivered

✔ Financial visibility

✔ Risk monitoring capability

✔ Cost optimization opportunity identification

✔ Executive decision support
