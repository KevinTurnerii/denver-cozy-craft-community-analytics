# Denver Cozy Craft Collective — Attendance Analytics & Capacity Forecasting System

## Business Problem
Despite increasing registrations, events consistently failed to reach full capacity due to low attendance conversion, limiting operational efficiency and growth potential.

Key challenges included:
- High no-show rates reducing actual attendance  
- Inefficient ticket release strategies  
- Limited visibility into retention and repeat engagement  
- Lack of forecasting for future event planning  

---

## Solution
Designed and implemented a full-stack analytics and forecasting system to model attendance behavior, optimize ticket release strategy, and support scalable event operations.

---

## Key Outcomes
- Identified **~54% no-show rate as the primary operational constraint**  
- Developed **~2.2× ticket release strategy** to consistently reach attendance targets  
- Analyzed attendance and retention across **6 events and 300+ participants**  
- Built end-to-end pipeline (**SQL → Python → Power BI**) for structured analytics and reporting  
- Delivered forecasting model to support capacity planning and growth strategy  

---

Built for a real community organization (**Denver Cozy Craft Collective**), supporting operational decision-making, attendance optimization, and long-term scaling.

This system transforms raw event data (orders, attendees, check-ins) into structured KPIs and forecasting models that enable data-driven planning and performance optimization.

---

## 📑 Table of Contents

- [Executive Overview](#executive-overview)
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

## Executive Overview

I designed and implemented an attendance analytics and forecasting system to evaluate event performance, participant engagement, and capacity utilization.

The system converts raw operational event data into structured, decision-ready insights that support attendance optimization, ticket release strategy, and long-term growth planning.

---

## Business Objectives

- Improve attendance conversion from registrations to verified attendees  
- Identify patterns in retention and repeat participation  
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
- Designed for SQL-based querying and scalable BI reporting  
- All Power BI visuals sourced from validated analytical outputs  

---

## Methodology

The system follows a structured analytics pipeline:

1. Raw data ingestion (orders, attendees, check-ins)  
2. Data cleaning and normalization (SQL + Python)  
3. Event-level KPI generation  
4. Attendance and conversion modeling  
5. Retention and repeat participation analysis  
6. Scenario-based forecasting (ticket release → attendance target)  

All KPIs were programmatically validated against raw check-in data to ensure full reconciliation and accuracy.

---

## End-to-End Pipeline Execution

### Data Engineering Layer (SQL — PostgreSQL)
- Ingested raw CSV exports into structured relational tables  
- Built dimensional model (fact + dimension tables)  
- Performed joins, transformations, and cleaning logic  
- Created analysis-ready datasets for downstream use  

### Analytical Layer (Python — Jupyter Notebook)
- Performed exploratory data analysis (EDA)  
- Engineered KPIs (attendance rate, conversion rate, retention)  
- Built forecasting logic using historical patterns  
- Validated outputs against source data  

### Business Intelligence Layer (Power BI)
- Developed executive dashboard for decision-making  
- Implemented DAX measures for KPI tracking  
- Visualized growth, utilization, engagement, and forecasting  
- Ensured full alignment with validated outputs  

---

## Analytical Framework

The analysis separates:

- **Registrations (Demand Layer)**  
- **Verified Attendance (Utilization Layer)**  

This enables:
- Accurate conversion modeling  
- Identification of no-show driven inefficiencies  
- Reliable forecasting based on actual behavior  

This mirrors real-world event analytics where demand ≠ utilization.

---

## Key Insights

### Attendance Efficiency
- Only **~46% of registrants attend events**  
- No-shows (~54%) are the primary constraint  

---

### Capacity Optimization
- To achieve ~70 attendees:  
  - **~152–175 registrations required**  
  - (~2.2× overbooking strategy)

---

### Growth Trend
- Registrations growing at **~22% per event**  
- Full capacity projected within **3–4 future events**

---

### Community Retention
- **~80% first-time participants**  
- **~20% repeat attendees**  
- Indicates early-stage community with retention opportunity  

---

## Power BI Dashboard

Power BI serves as the executive decision layer.

### Page 1 — Growth
- Seats Reserved by Event  
- Growth Rate Over Time  
- Capacity Trend  

### Page 2 — Utilization
- Verified Attendance vs Registrations  
- Attendance Rate %  
- Capacity Gap Analysis  

### Page 3 — Engagement
- Conversion (Buyer → Attendee)  
- Repeat Participation Breakdown  
- Community Depth Metrics  

### Page 4 — Forecasting
- Ticket Release Scenarios  
- Attendance Target Planning  
- Capacity Optimization  

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

- Identified no-show rate as the primary constraint impacting event performance  
- Enabled data-driven ticket release strategies to improve attendance consistency  
- Established baseline KPIs for attendance, conversion, and retention  
- Delivered forecasting framework to support event scaling and planning  
- Provided stakeholder-ready dashboards for monitoring and decision-making  

---

## Repository Structure

~~~
cozycraft-attendance-analytics-forecasting/
│
├── data/
│   ├── raw/                # Original source files
│   └── processed/          # Cleaned datasets used for analysis
│
├── sql/                    # Data warehouse schema and transformations
│
├── notebooks/              # Python analysis and forecasting models
│
├── powerbi/                # Dashboard files (.pbix)
│
├── images/                 # Dashboard screenshots and visuals
│
└── README.md
~~~

---

## Data Validation

- All KPIs computed programmatically  
- Fully reconciled with raw check-in data  
- No manual adjustments applied  
- Fully reproducible pipeline  

---

## Conclusion

This project demonstrates a full-stack analytics workflow, transforming raw operational event data into structured, decision-ready insights.

By integrating data engineering, analytical modeling, and business intelligence, the system enables optimized attendance planning, improved capacity utilization, and scalable community growth.
