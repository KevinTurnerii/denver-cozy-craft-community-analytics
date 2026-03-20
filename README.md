# Denver Cozy Craft Collective — Event Analytics & Forecasting

## 🚀 Business Impact Snapshot

- Analyzed attendance and retention across 6 events and 300+ participants  
- Identified **~54% no-show rate as the primary capacity constraint**  
- Developed **~2.2x ticket release strategy** to reach target attendance  
- Built full ETL → analytics → dashboard pipeline (SQL → Python → Power BI)  
- Delivered forecasting model for capacity planning and community growth  

---

Built a full-stack analytics and forecasting system to evaluate attendance behavior, retention patterns, and capacity utilization across a growing event-based business.

The system transforms raw event data (orders, attendees, check-ins) into structured KPIs and forecasting models that support ticket release optimization, attendance planning, and long-term community growth strategy.

**Pipeline:** PostgreSQL (ETL & Data Warehouse) → Python (EDA & Modeling) → Power BI (Visualization & Insights)

---

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Business Objectives](#business-objectives)
- [Data Architecture](#data-architecture)
- [Methodology](#methodology)
- [End-to-End Pipeline Execution](#end-to-end-pipeline-execution)
- [Analytical Framework](#analytical-framework)
- [Key Insights](#key-insights)
- [Power BI Dashboard](#power-bi-dashboard)
- [Dashboard Preview](#dashboard-preview)
- [Tools & Technologies](#tools--technologies)
- [Business Impact](#business-impact)
- [Repository Structure](#repository-structure)
- [Data Validation](#data-validation)
- [Conclusion](#conclusion)

---

## Project Overview

This project analyzes Cozy Craft’s transition from three 2025 pilot events to scaled 2026 operations, measuring attendance efficiency, repeat engagement, and growth sustainability across six total events.

---

## Business Problem

Despite increasing registrations, events consistently failed to reach full capacity due to low attendance conversion.

Key challenges:
- High no-show rates reducing actual attendance  
- Inefficient ticket release strategies  
- Limited visibility into retention and repeat engagement  
- Lack of forecasting for future event planning  

---

## Business Objectives

- Improve attendance conversion from registrations to verified attendees  
- Identify patterns in customer retention and repeat participation  
- Develop a forecasting model for event capacity planning  
- Build a scalable analytics pipeline for ongoing operational use  

---

## Data Architecture

Dimensional modeling approach using a star schema:

**Fact Table**
- `fact_event_performance`

**Dimension Tables**
- `dim_event`  
- `dim_attendees`

Design principles:

- Event-grain modeling for accurate KPI aggregation  
- Separation of registrations vs verified attendance  
- Participant-level tracking for retention analysis  
- All Power BI visuals sourced from validated analytical outputs  

---

## Methodology

The project followed a structured analytics pipeline:

1. Raw data ingestion (orders, attendees, check-ins)  
2. Data cleaning and normalization (SQL + Python)  
3. Event-level KPI generation  
4. Attendance and conversion modeling  
5. Retention and repeat participation analysis  
6. Scenario-based forecasting (ticket release → attendance target)  

All KPIs were programmatically validated against raw check-in data to ensure full reconciliation and metric integrity.

---

## End-to-End Pipeline Execution

This project was executed as a complete analytics pipeline across three layers:

### Data Engineering Layer (SQL — PostgreSQL)
- Ingested raw CSV exports into structured relational tables  
- Built dimensional model (fact + dimension tables)  
- Performed data cleaning, joins, and transformation logic  
- Created analysis-ready datasets for downstream modeling  

### Analytical Layer (Python — Jupyter Notebook)
- Performed exploratory data analysis (EDA)  
- Engineered KPIs (attendance rate, conversion rate, retention)  
- Built forecasting logic using historical growth and conversion patterns  
- Validated all outputs against raw data for accuracy  

### Business Intelligence Layer (Power BI)
- Developed executive dashboard for decision-making  
- Implemented DAX measures for KPI tracking  
- Visualized growth, utilization, engagement, and forecasting scenarios  
- Ensured full alignment with validated analytical outputs  

---

## Analytical Framework

To ensure accurate modeling of event performance, the analysis separates:

- **Registrations (Demand Layer)**  
- **Verified Attendance (Utilization Layer)**  

This distinction enables:
- Accurate conversion rate modeling  
- Identification of no-show driven inefficiencies  
- Reliable forecasting based on actual attendance behavior  

This mirrors real-world event analytics where demand does not equal utilization.

---

## Key Insights

### Attendance Efficiency
- Only **~46% of registrants attend events**  
- No-shows (~54%) are the primary constraint on capacity utilization  

---

### Capacity Optimization
- To achieve **~70 attendees**, approximately:  
  - **~152–175 registrations are required**  
  - (~2.2x overbooking strategy)

---

### Growth Trend
- Registrations growing at **~22% per event**  
- Full capacity projected within **3–4 future events**

---

### Community Retention
- **~80% of attendees are first-time participants**  
- Only **~20% return**  
- Indicates early-stage community with retention opportunity  

---

## Power BI Dashboard

Power BI serves as the executive reporting and decision layer.

### Page 1 — Growth
- Seats Reserved by Event  
- Growth Rate Over Time  
- Capacity Trend  

### Page 2 — Utilization
- Verified Attendance vs Registrations  
- Attendance Rate %  
- Capacity Gap Analysis  

### Page 3 — Engagement
- Buyer → Attendee Conversion  
- Repeat Participation Breakdown  
- Community Depth Metrics  

### Page 4 — Forecasting
- Ticket Release Scenarios  
- Attendance Target Planning  
- Capacity Optimization Strategy  

All measures implemented in DAX and trace directly to validated modeling outputs.

---

## Dashboard Preview

### Executive Overview
![Overview](images/overview.png)

### Event Performance
![Performance](images/performance.png)

### Retention Analysis
![Retention](images/retention.png)

### Forecasting & Capacity Planning
![Forecast](images/forecast.png)

---

## Tools & Technologies

- **SQL (PostgreSQL)** — ETL, data modeling, warehousing  
- **Python (pandas, Jupyter Notebook)** — EDA, KPI engineering, forecasting  
- **Power BI** — dashboards, visualization, reporting  

---

## Business Impact

This project delivers a scalable analytics framework that enables:

- Data-driven ticket release strategy  
- Improved attendance utilization  
- Identification of retention gaps  
- Forecast-based capacity planning  

Applicable to:
- Event-based businesses  
- Membership communities  
- Subscription platforms  
- Conference and venue planning  

---

## Repository Structure

~~~
cozy-craft-community-analytics/
│
├── data/
│ ├── raw/
│ └── processed/
├── notebooks/
├── powerbi/
├── images/
├── sql/
└── README.md
~~~


---

## Data Validation

- All KPIs computed programmatically  
- Validated against raw check-in data  
- No manual manipulation of results  
- Fully reproducible pipeline  

---

## Conclusion

This project demonstrates a full-stack analytics workflow, transforming raw operational event data into actionable business insights.

By integrating data engineering, analytical modeling, and business intelligence, the system enables optimized attendance planning, improved capacity utilization, and sustainable community growth.
