<div align="center">

# Public Transit Operations Optimization

### CT Transit · Operations Analytics · Demand Forecasting · Facility Location

[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)](https://microsoft.com/excel)
[![Operations](https://img.shields.io/badge/Operations_Analytics-2C3E50?style=flat-square)]()
[![Forecasting](https://img.shields.io/badge/Demand_Forecasting-FF6B35?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)]()

| | |
|---|---|
| **Domain** | Public Transit · Supply Chain & Operations · Quantitative Analysis |
| **Tools** | Excel, Operations Research Methods |
| **Methods** | Demand Forecasting, Little's Law, Centre of Gravity |
| **Corridor** | Downtown New Haven to West Haven, CT |

</div>

---

## The Business Problem

CT Transit's New Haven–West Haven bus corridor was running on static schedules with no quantitative basis for fleet sizing, frequency decisions, or maintenance hub placement. Service was inconsistent. Passengers waited longer than necessary. Maintenance crews were positioned by convention rather than by where breakdowns actually happened.

**The question:** What does the data say the right fleet size is, where should hubs be located, and what is the financial case for these changes?

---

## Challenge

Three operational problems were running simultaneously — and each required a different quantitative method.

Fleet frequency decisions had no mathematical grounding. Adding buses feels intuitive, but without a demand model and a queuing framework, there's no way to know how much wait time each additional bus actually buys, or when additional buses stop producing meaningful improvement (diminishing returns).

Maintenance hub placement had been decided historically, not analytically. The result was excess deadhead mileage — buses traveling empty to jobs rather than being positioned where the work is.

Budget planning was done to a single ridership projection with no scenario envelope. If demand varied by 15%, the plan had no answer.

---

## Action

**Demand Forecasting with Confidence Intervals**
Ridership projections were built at three scenarios — base, upper, and lower — with ±10-15% confidence intervals. This gave management a range to plan against rather than a single number that may or may not materialize. Fleet sizing decisions were validated against all three scenarios.

**Waiting Time Optimization via Little's Law**
Queuing theory, specifically Little's Law (L = lambda W), was applied to model the relationship between bus frequency and average passenger wait time precisely. This framework quantified exactly how much wait time each additional bus would eliminate — and identified the point of diminishing returns at 8 buses for this corridor's demand profile.

**Centre of Gravity Facility Location**
Weighted demand coordinates from breakdown incident data were used to solve for optimal maintenance hub locations. The Centre of Gravity method minimized total deadhead mileage across all service events simultaneously — producing a location recommendation grounded in actual operational patterns.

**KPI Framework Design**
Six operational KPIs were defined with baselines and improvement targets: passenger wait time, fleet utilization rate, breakdown response time, daily ridership, route revenue, and operating cost per passenger. These KPIs were designed for ongoing monitoring, not one-time reporting.

---

## Result

| Metric | Baseline | Result |
|---|---|---|
| Avg. passenger wait time | Unoptimized | **25-28% reduction** |
| Daily ridership | 320/day | **500/day (+56%)** |
| Daily route revenue | Baseline | **+$315/day** |
| Annualized route revenue impact | — | **$100,000+** |
| Operating cost (projected) | Baseline | **10-15% reduction** |
| Breakdown response time | Unoptimized | **15-20% faster** |
| Fleet utilization | Baseline | **12-18% improvement** |

**The result that drove the recommendation:** Adding buses from 6 to 8 on this corridor produced a 28% wait time reduction and a 56% ridership increase. The demand model showed the gains were real and not an artifact of the baseline conditions. The cost reduction from hub repositioning compounded the financial case.

---

## Technical Architecture

```
Transit Data: Ridership | Fleet Counts | Route Revenue | Breakdown Incidents
                    |
                    v
        Exploratory Analysis + KPI Baseline
                    |
          __________|__________
         |           |         |
         v           v         v
  Demand           Little's   Centre of
  Forecasting      Law Model  Gravity
  (3 scenarios,    (wait      (hub location
  +/-10-15% CI)    time vs.   optimization)
                   frequency)
         |           |         |
         |___________|_________|
                    |
                    v
        Operational Recommendations
        Fleet sizing | Hub placement | Budget scenarios
```

**Repository structure:**
```
Public_Transport_Supply_Chain_Operations/
├── CT_Transit_Operations_Model.xlsx
└── README.md
```

---

## Key Insights

The queuing model confirmed that the optimal intervention on this corridor is targeted frequency increases during high-demand windows — not wholesale fleet expansion. Adding the 9th bus produces significantly smaller wait time improvements than the 7th or 8th. Knowing the diminishing returns curve is what separates a capital allocation decision from a guess.

Hub repositioning via Centre of Gravity reduced theoretical deadhead mileage by 12%. Across a full route network, that 12% compounds — each route saves fuel, driver hours, and response time. The method scales directly to any multi-facility operations problem.

The confidence interval forecasting framework addresses a gap that appears in most transit planning: single-point projections that get treated as certainties. Stress-testing against the lower bound demand scenario is what keeps capital decisions defensible when actual ridership underperforms.

---

## Recommended Extensions

Real-time GPS fleet data would allow dynamic scheduling to replace static timetables. Advanced time series models (ARIMA, Prophet) on actual ridership data would sharpen forecast accuracy. A Power BI dashboard connected to live operational feeds would make these KPIs continuously visible to management without requiring periodic manual reporting.

---

<div align="center">

**[Balasurya Chandana](https://linkedin.com/in/balasurya-chandana)** · Business & Data Analyst · [linkedin.com/in/balasurya-chandana](https://linkedin.com/in/balasurya-chandana)

</div>
