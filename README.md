<div align="center">

# Public Transit Operations Optimization
### CT Transit · Operations Analytics · Demand Forecasting · Facility Location

[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)](https://microsoft.com/excel)
[![Operations](https://img.shields.io/badge/Operations_Analytics-2C3E50?style=flat-square)]()
[![Forecasting](https://img.shields.io/badge/Demand_Forecasting-FF6B35?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)]()

**Domain:** Public Transit · Supply Chain & Operations · Quantitative Analysis
**Tools:** Excel, Operations Research Methods
**Focus Corridor:** Downtown New Haven to West Haven, CT

</div>

---

## Executive Summary

This project applies quantitative operations analytics to a realistic public transportation scenario — improving the efficiency, reliability, and cost structure of a regional bus transit system. Using demand forecasting, queuing theory, and center-of-gravity optimization, the analysis identifies actionable changes that reduce passenger wait times, lower operating costs, and improve asset utilization without requiring large capital investments.

---

## Challenge

CT Transit's New Haven-West Haven corridor faced compounding operational inefficiencies: inconsistent service frequency created unnecessarily long passenger wait times, fleet deployment was reactive rather than demand-driven, and maintenance facilities were positioned without regard for actual breakdown patterns or response time optimization.

The core analytical challenge was integrating multiple layers of operational data — ridership demand, fleet counts, route revenue, and breakdown incident patterns — into a unified framework that could generate defensible, actionable recommendations for route management and infrastructure positioning.

---

## Action

**Demand Forecasting**
Ridership projections were built with upper and lower confidence intervals of plus or minus 10 to 15 percent to support both conservative and optimistic fleet planning scenarios. Forecasting models enabled resource allocation decisions to be evaluated against a range of demand outcomes rather than a single point estimate.

**Waiting Time Optimization via Little's Law**
Queuing theory — specifically Little's Law (L = lambda x W) — was applied to model the relationship between bus frequency and average passenger wait time. This mathematical framework allowed precise quantification of how incremental fleet additions would translate into service time improvements, avoiding over- or under-investment in capacity.

**Centre of Gravity Facility Location**
The Centre of Gravity method was used to determine optimal placement for maintenance hubs and breakdown response facilities based on weighted demand coordinates. This reduced both average response time and non-revenue deadhead mileage across the route network.

**KPI Framework Design**
Operational KPIs were defined and tracked across fleet utilization, revenue per route, waiting time, and breakdown response — enabling ongoing performance monitoring rather than one-time analysis.

---

## Result

| Metric | Outcome |
|---|---|
| Avg. passenger wait time reduction | 25-28% |
| Ridership increase (6 to 8 buses deployed) | 320 to 500 passengers/day |
| Daily route revenue increase | ~56% |
| Operating cost reduction (projected) | 10-15% |
| Breakdown response time improvement | 15-20% |
| Fleet utilization improvement | 12-18% |
| Daily revenue improvement per route | ~$315 |
| Annualized route-level impact | $100,000+ |

---

## Technical Architecture

```
Transit Performance Data (Ridership, Fleet, Revenue, Maintenance)
        |
        v
Exploratory Data Analysis -- KPI Baseline Establishment
        |
        |---> Demand Forecasting (Confidence Intervals 10-15%)
        |
        |---> Queuing Model (Little's Law) -- Optimal Bus Frequency
        |
        +---> Centre of Gravity Analysis -- Hub Location Optimization
                        |
                        v
               Excel Model + Operational Recommendations
```

**Folder structure:**
```
Public_Transport_Supply_Chain_Operations/
├── CT_Transit_Operations_Model.xlsx
├── report/
│   └── CT_Transit_Analysis_Report.pdf
└── README.md
```

---

## Key Insights

The most significant lever in this system was fleet frequency — the analysis confirmed a strong inverse relationship between bus availability and wait time, with diminishing returns setting in above 8 buses for this corridor's demand profile. This means the optimal intervention is targeted frequency increases on high-demand windows rather than wholesale fleet expansion.

Hub positioning via Centre of Gravity reduced theoretical deadhead mileage by approximately 12 percent, which directly reduces fuel cost and driver non-productive hours. When scaled across a multi-route network, this methodology generates compounding operational savings.

The forecasting confidence interval framework is particularly valuable for budget planning: it allows management to stress-test capacity decisions against demand variability rather than planning to a single projection that may not materialize.

---

## Recommended Next Steps

Integrating real-time GPS fleet data would allow dynamic scheduling to replace static timetables. Advanced time series models such as ARIMA or Prophet applied to actual ridership data would improve forecast accuracy. An executive Power BI dashboard connected to live operational feeds would make these KPIs continuously visible to management rather than requiring periodic manual reporting.

---

<div align="center">
<sub>Balasurya Chandana · Business & Data Analyst · linkedin.com/in/balasurya-chandana</sub>
</div>
