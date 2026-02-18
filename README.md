# YellowTrip-NYC-Taxi-Analysis

## Project Overview

This project analyses 898K Yellow Taxi trips in New York City during May–June 2020 to uncover operational patterns, revenue drivers, and optimisation opportunities. The analysis is built from two perspectives — **Vendor** (fleet operations) and **Employee** (driver earnings) — using Power BI dashboards connected to NYC TLC trip record data.

**Context:** May–June 2020 coincided with NYC's COVID-19 lockdown and early reopening phase. Trip volumes were significantly lower than pre-pandemic levels, making this a unique window into how taxi operations behave under constrained demand — and which patterns persist even during a downturn.

**Goal:** Identify the highest-value time slots, locations, and vehicle types to help vendors optimise fleet deployment and help drivers maximise earnings per shift.

**Tools & Technologies:** Power BI · NYC TLC Trip Record Data · Geographic Analysis (Bing Maps) · DAX

---

## Executive Summary

| Metric | Value |
|--------|-------|
| Total Trips | 898K |
| Total Income | $17M |
| Total Returns | $58K |
| Total Tips | $1.47M |
| Avg Income per Trip | $19.12 |
| Avg Tip | $1.63 |
| Avg Distance | 9.25 km |

### Top Findings

- **Friday dominates** trip volume across both vehicle types, while **Monday generates the highest avg income per trip ($21.59)** — volume and value peak on different days.
- **Afternoon rush (13:00–17:00)** accounts for the top 5 busiest hours, with 15:00 as the absolute peak. Morning rush is notably absent during the COVID period.
- **Manhattan generates 87%+ of all trips** (775K) and passengers (973K). Queens is a distant second at 54K trips. Staten Island and EWR are negligible.
- **EWR airport tips are 6x higher** ($9.90 avg) than Manhattan ($1.59), but with only 38 trips it's a niche opportunity, not a strategy.
- **Medium cars earn $0.38/km in tips** vs Private cars at $0.17/km — more than double the tip rate per kilometre despite Private being the dominant vehicle type.
- **Returns total $58K** against $17M income (0.34%), which is low but worth monitoring by vendor for quality issues.

---

## 1. Vendor Perspective — Fleet Operations

![Vendor Dashboard](dashboards/Vendor.png)

The vendor dashboard reveals where and when to deploy vehicles for maximum utilisation.

### Trip Volume by Day

| Day | Trip Volume | Rank |
|-----|-----------|------|
| Friday | ~175K | 1st |
| Tuesday | ~150K | 2nd |
| Monday | ~140K | 3rd |
| Thursday | ~130K | 4th |
| Wednesday | ~125K | 5th |
| Saturday | ~100K | 6th |
| Sunday | ~75K | 7th |

Private vehicles dominate every day of the week, with Medium Cars representing a small fraction of total trips. Weekend volumes drop significantly — Sunday is roughly 40% of Friday's volume.

### Top Rush Hours

The 5 busiest hours are all in the afternoon block:

| Rank | Hour | Avg Trips |
|------|------|----------|
| 1st | 15:00 | ~68K |
| 2nd | 14:00 | ~65K |
| 3rd | 16:00 | ~63K |
| 4th | 13:00 | ~60K |
| 5th | 17:00 | ~58K |

The traditional morning rush (7:00–9:00) does not appear in the top 5 — likely a COVID effect as commuter traffic was severely reduced during this period. This pattern may not hold in normal operating conditions.

### Geographic Concentration

Manhattan accounts for the overwhelming majority of pickup volume, visible as the sole concentration point on the map. The vendor filter shows three operators: Creative Mobile Technologies LLC, VeriFone Inc., and NewPlayer.

**Vendor actions:** Maximise Manhattan coverage during 13:00–17:00 weekdays. Ensure Friday fleet capacity is at maximum. Investigate the $58K in returns — is it concentrated in one vendor or spread evenly?

---

## 2. Employee Perspective — Driver Earnings

![Employee Dashboard](dashboards/Employee.png)

The employee dashboard focuses on what drivers can control: which days to work, where to position, and which vehicle to drive.

### Average Income by Day

| Day | Avg Income/Trip |
|-----|----------------|
| Monday | $21.59 |
| Sunday | $19.34 |
| Friday | $18.75 |
| Thursday | $18.59 |
| Saturday | $18.55 |
| Tuesday | $18.55 |
| Wednesday | $18.41 |

Monday pays $3.18 more per trip than Wednesday — a 17% premium. This is counterintuitive since Friday has the highest volume, but lower competition on Monday likely drives higher per-trip fares. Drivers should avoid taking Mondays off.

### Average Tip by Borough

| Borough | Avg Tip | Trips |
|---------|---------|-------|
| EWR Airport | $9.90 | 38 |
| Queens | $2.75 | 54,457 |
| Manhattan | $1.59 | 775,326 |
| Brooklyn | $1.20 | 37,116 |
| Staten Island | $1.10 | 884 |
| Bronx | $0.92 | 21,825 |

EWR's $9.90 avg tip is striking but based on only 38 trips — not a reliable strategy. Queens at $2.75 on 54K trips is the actionable finding: 73% higher tips than Manhattan with meaningful volume. Drivers finishing Manhattan trips heading toward Queens should consider repositioning rather than returning.

### Tip per Km by Vehicle Type

Medium Cars earn **$0.38/km** in tips vs Private vehicles at **$0.17/km** — more than double. Despite Private vehicles dominating trip volume, Medium Cars are significantly more profitable on a per-kilometre basis for tip income. Drivers with the option should evaluate whether the Medium Car tip premium offsets any volume differences.

### Passengers by Borough

Manhattan dominates with ~973K passengers, followed by Queens (~52K), Brooklyn (~14K), and the Bronx (~8K). Staten Island and EWR are negligible. The Unknown category (~10K passengers) suggests data quality issues with LocationIDs 264 and 265 that should be investigated.

---

## 3. Strategic Recommendations

### For Vendors / Fleet Operators

| Priority | Action | Rationale |
|----------|--------|-----------|
| 1 | **Max fleet in Manhattan, weekdays 13:00–17:00** | 87% of trips, top 5 rush hours all afternoon |
| 2 | **Scale up Friday capacity** | Highest volume day by ~15% over Tuesday |
| 3 | **Investigate $58K returns** | Identify if vendor-specific or systemic |
| 4 | **Evaluate Medium Car expansion** | Higher tip/km suggests underserved demand |
| 5 | **Resolve unknown LocationIDs 264/265** | ~10K passengers with no borough attribution |

### For Drivers

| Priority | Action | Rationale |
|----------|--------|-----------|
| 1 | **Don't take Mondays off** | $21.59 avg/trip — highest earning day |
| 2 | **Work the 13:00–17:00 block** | Peak demand, highest trip availability |
| 3 | **Position in Queens after Manhattan runs** | $2.75 avg tip vs $1.59 in Manhattan |
| 4 | **Consider Medium Car if available** | $0.38/km tip vs $0.17/km for Private |
| 5 | **Avoid Staten Island and Bronx** | Low volume, lowest tips ($0.92–$1.10) |

---

## COVID-19 Context

This dataset covers May–June 2020 — the tail end of NYC's initial lockdown and early Phase 1 reopening. Key implications:

- **Trip volumes are dramatically lower** than pre-pandemic baselines (NYC typically sees 300K+ yellow taxi trips per day vs ~15K/day in this dataset)
- **The absent morning rush** (no 7:00–9:00 peak) is almost certainly a COVID effect from reduced commuter traffic
- **Afternoon dominance** may partially normalise post-pandemic, but the 13:00–17:00 concentration is a useful signal even under normal conditions
- **Geographic concentration** in Manhattan may be even more pronounced than normal, as outer-borough demand collapsed further during lockdown

These findings should be validated against post-pandemic data before making long-term strategic decisions.

---

---

## Future Enhancements

- Compare with 2019 pre-COVID data to isolate pandemic effects
- Add seasonal analysis across a full 12-month period
- Build a predictive model for trip demand by hour/borough
- Correlate weather data with trip volume and tip behaviour
- Analyse route-level data for driver positioning optimisation

---

*Analysis Period: May–June 2020 · Last Updated: January 2026*
