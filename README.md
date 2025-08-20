# 🚌 Bus Transportation Analytics Dashboard (Excel)
[![GitHub last commit](https://img.shields.io/github/last-commit/aispai9995/bus-transportation-analytics-Excel?color=green&logo=github&style=for-the-badge)](https://github.com/aispai9995/bus-transportation-analytics-Excel) 
[![Excel](https://img.shields.io/badge/Microsoft%20Excel-F37626?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://github.com/aispai9995/bus-transportation-analytics-Excel)
[![GitHub repo size](https://img.shields.io/github/repo-size/aispai9995/bus-transportation-analytics-Excel?style=for-the-badge&color=blue)](https://github.com/aispai9995/bus-transportation-analytics-Excel)

## 🎯Objective
Excel is often overlooked. Yet it’s one of the most powerful tools for analysis, modeling, and storytelling when used well. This project analyzes the city bus operations to uncover usage patterns, inefficiencies in public transport, answer key operational questions, identify business development opportunities and thereby guide strategic decisions. Two interactive Dashboards are built in Excel to analyze and optimize city bus operations and to present those insights to the decision-makers.

## 🧰 Tools & Techniques

<li> Power Query (M Code): Data ingestion, cleaning, column normalization, time bucketing (hour-of-day, weekday, month). </li>

<li> Power Pivot (DAX): Time intelligece for dynamic reporting, build KPIs, relationships and custom measures (YoY %, utilization rate, peak-hour riders, route share). </li>

<li> Dashboards: Pivot charts, slicers for interactivity, KPI cards, abnd a clear layout for real-time business storytelling. </li>

<li> ChatGPT: Assisted in Drafting M Code / DAX snippets. </li>

## ❓ Key Business Questions

<li> Which routes are over- or under-utilized? </li>

<li> How does ridership vary by time, age, gender, and occupation? </li>

<li> What frequency changes or marketing can improve off-peak usage? </li>

<li> Which KPIs should transit managers track to drive ROI? </li>

## 💡 Insights (from this dataset)

📉 83.5% YoY drop in total ridership → urgent intervention needed.

🚌 East–West & Central lines: consistently high traffic; South line: underutilized.

⏰ Peak times differ by occupation → opportunity for schedule realignment and dynamic pricing.

👥 Target segment: males 30–39 → scope for targeted campaigns and gender diversity initiatives.

These insights are surfaced through interactive filters, making it easy for non-technical stakeholders to explore scenarios.

## 📌 KPIs (with example DAX)

| KPI                  | What it tells you            | Example DAX (Power Pivot)                                                                                                                                    |
| -------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Total Riders**     | Overall demand               | `Total Riders := SUM(FactRidership[Riders])`                                                                                                                 |
| **YoY % Change**     | Growth/decline vs. last year | `YoY % := DIVIDE([Total Riders] - CALCULATE([Total Riders], SAMEPERIODLASTYEAR('Date'[Date])), CALCULATE([Total Riders], SAMEPERIODLASTYEAR('Date'[Date])))` |
| **Utilization Rate** | Load factor by route/time    | `Utilization % := DIVIDE([Total Riders],[Total Capacity])`                                                                                                   |
| **Route Share %**    | Share of riders by route     | `Route Share % := DIVIDE([Total Riders], CALCULATE([Total Riders], ALL('DimRoute'))) `                                                                       |
| **Peak Hour Riders** | Demand during peaks          | `Peak Hour Riders := MAXX(VALUES('Date'[Hour]), CALCULATE([Total Riders]))`                                                                                  |

## 🧱 Data Model

<img width="1530" height="762" alt="DataModel" src="https://github.com/user-attachments/assets/06bf21da-9b37-47f9-9206-3dc5358d2e46" />


## 📊 Dashboard Features

<li> KPI Cards: Total Riders, YoY %, Utilization %, Route Share </li> 

<li> Time-Based View: Hourly/weekday/monthly patterns with slicers for route & demographics. </li> 

<li> Route Deep-Dive: Utilization vs. capacity, trend lines, and route comparisons. </li> 

<li> Demographics Panel: Age, gender, occupation breakdowns with cross-filtering. </li> 

<li> Recommendations Panel: Data-driven actions (frequency, pricing, marketing). </li> 

## 📊 Dashboard 1 - Time Series Dashboard
<img width="1207" height="621" alt="Dashboard1" src="https://github.com/user-attachments/assets/23b0e1db-30be-4f89-89d1-c8a5686c887e" />

## 📊 Dashboard 2 - Deep Dive Dashboard
<img width="1207" height="621" alt="Dashboard2" src="https://github.com/user-attachments/assets/db5c176b-a1f0-4c4a-b103-844b9c664733" />
<img width="1207" height="621" alt="Insights" src="https://github.com/user-attachments/assets/66c59b40-ac4e-469b-b177-d0877380179b" />

## 🧭 Decisions this Dashboard Supports

<li> Schedule optimization: Match frequency to actual demand across hours and occupations. </li> 

<li> Capacity planning: Align vehicle size/number with corridor-level utilization. </li> 

<li> Targeted campaigns: Reach segments (e.g., 30–39 males) and improve gender diversity.</li> 

<li> ROI tracking: Monitor the impact of interventions via KPIs (YoY %, off-peak uplift).</li> 

## 🛠️ What I Learned

✔️ Effective data visualization drives strategy by making insights accessible to business users, enabling informed decisions.<br>
✔️ KPIs aren’t just numbers, they’re decision enablers. Understanding what to measure and why is as important as knowing how.<br>
✔️ Targeted marketing and dynamic pricing are powerful business strategies that can significantly influence user behavior.<br>
✔️ When used creatively, Excel can be a powerful tool for building robust models and clear stories for data-driven decision-making.<br>
✔️ Design matters. Layout, contrast, and annotation accelerate comprehension.<br>

## 🔗 Related Links
📌 [LinkedIn Post](https://www.linkedin.com/feed/update/urn:li:activity:7346556819433046017/)

#### ✨ If you like this project, don’t forget to ⭐ star the repo!
