# 🚕 YellowTrip NYC Taxi Activity Analysis

## 📋 Project Overview

This project presents a comprehensive Power BI data analysis of **YellowTrip taxi operations** in New York City during **May-June 2020**. The analysis provides actionable insights from both **vendor** (company) and **employee** (driver) perspectives, examining trip patterns, vehicle utilization, rush hour trends, income distribution, tipping behavior, and passenger demographics across NYC's five boroughs.

### 📅 Time Period
- **May - June 2020**
- **Location:** New York City (Manhattan, Brooklyn, Queens, Bronx, Staten Island, EWR Airport)

### 🎯 Dual Perspective Analysis
This analysis serves two key stakeholder groups:
1. **Vendors/Companies:** Performance metrics, fleet optimization, location strategies
2. **Employees/Drivers:** Income optimization, best working days/locations, tipping insights

## 📊 Data Sources

The analysis incorporates multiple data dimensions:

### Vendor Perspective Data:
- Income and Returns
- Vehicle Types
- Pickup Locations (by borough)
- Rush Hours and Peak Times
- Vendor Performance (VeriFone Inc. and others)

### Employee Perspective Data:
- Trip Income and Tips
- Borough-level Trip Distribution
- Vehicle Types and Performance
- Distance Traveled
- Number of Passengers
- Average Income per Trip

## 🎯 Objectives

### Overall Goals:
1. **Analyze Performance Trends** - Identify patterns in taxi operations over time
2. **Understand Trip Patterns** - Examine trip volume and distance variations
3. **Evaluate Income & Tips** - Assess earning potential across different factors
4. **Optimize Operations** - Provide data-driven recommendations for vendors and drivers
5. **Statistical Analysis** - Apply comprehensive analytical approaches to uncover insights

## 🔍 Business Questions Analyzed

### 💼 Vendor Perspective Questions:

1. **What is the distribution of vehicle types by day of the week?**
   - **Finding:** Friday has the most trips on average
   - **Finding:** Private vehicles are the most chosen vehicle type
   - **Recommendation:** Focus on acquiring private service vehicles; investigate lower demand for other vehicle types

2. **Which five hours a day, on average, have the most starting times for rides?**
   - **Top 3 Rush Hours:**
     - 1st: 15:00 (3:00 PM)
     - 2nd: 14:00 (2:00 PM)
     - 3rd: 16:00 (4:00 PM)
   - **Recommendation:** These afternoon hours (1 PM - 5 PM) are priority times for vehicle availability

3. **Where are the most trips generated? (Pickup borough perspective)**
   - **Manhattan:** 775,326 trips (highest)
   - **Queens:** 54,457 trips
   - **Brooklyn:** 37,116 trips
   - **Bronx:** 21,825 trips
   - **Unknown:** 8,417 trips
   - **Staten Island:** 884 trips
   - **EWR International Airport (Newark):** 38 trips
   - **Recommendation:** Maximize vehicle presence in Manhattan, especially during peak times; consider investigating unknown borough LocationIDs 264 and 265

### 👥 Employee Perspective Questions:

1. **What are the two days a week when the average income per trip is the highest?**
   - **Average Income per Trip:** $19.12
   - **Recommendation:** Drivers should prioritize working these high-income days and avoid taking days off or scheduling maintenance during peak earning periods

2. **What is the type of vehicle with the highest tip per kilometer?**
   - **Finding:** Medium vehicles show higher tips per kilometer compared to private vehicles
   - **Recommendation:** Driving a medium vehicle may be more profitable, though further analysis of trip length is needed

3. **What are the best tipping boroughs?**
   - **Top Boroughs for Tips:** Manhattan and Queens
   - **Recommendation:** Drivers should focus on these boroughs for higher take-home earnings

4. **Which boroughs have the highest number of passengers?**
   - **Manhattan:** 973,316 passengers (highest)
   - **Queens:** 51,956 passengers
   - **Brooklyn:** 13,920 passengers
   - **Unknown:** 9,670 passengers
   - **Bronx:** 8,025 passengers
   - **Staten Island:** 206 passengers
   - **EWR International Airport (Newark):** 64 passengers

## 📈 Key Findings

### Trip Patterns:
- **Busiest Day:** Friday has the highest average number of trips
- **Peak Hours:** Rush hours occur between 13:00 and 17:00, with 15:00 as the peak hour
- **Vehicle Preference:** Private vehicles are the most preferred vehicle type

### Geographic Insights:
- **Top 3 Boroughs:** Manhattan (dominant), Queens, and Brooklyn account for the vast majority of trips and passengers
- **Manhattan Dominance:** Manhattan generates over 87% of total trips and passengers
- **Low Activity:** Staten Island and EWR Airport show minimal taxi activity

### Vendor Performance:
- **Top Vendor:** VeriFone Inc. has the highest trip numbers
- **Concern:** VeriFone Inc. shows high number of returns - requires review and investigation

### Income & Tips:
- Average income per trip: **$19.12**
- Manhattan and Queens offer the best tipping opportunities
- Medium vehicles may generate higher tips per kilometer than private vehicles

## 💡 Conclusions

### Key Takeaways:

1. **High Trip Volume:** Friday is the busiest day for taxi operations
2. **Afternoon Rush:** Peak activity occurs between 13:00 and 17:00 hours
3. **Manhattan Dominance:** Manhattan is the primary market, generating the overwhelming majority of trips and passenger volume
4. **Vehicle Preference:** Private vehicles are the most popular choice among customers
5. **Vendor Leader:** VeriFone Inc. leads in trip numbers but needs to address high return rates

## 🛠️ Recommendations

### For Vendors/Companies:

1. **Geographic Focus:**
   - Concentrate resources on **Manhattan, Queens, and Brooklyn**
   - Maintain high vehicle availability in Manhattan during all hours
   - Consider limited operations in Staten Island and Bronx

2. **Data Quality:**
   - **Investigate unknown boroughs** with LocationID 264 and 265
   - Improve data collection and location tracking

3. **Market Opportunity:**
   - **New players** should consider focusing on:
     - Night shift operations (less competition)
     - Markets without medium car saturation

4. **Performance Review:**
   - **VeriFone Inc.** should review and reduce high return numbers
   - Investigate causes of returns and implement corrective measures

5. **Fleet Management:**
   - Prioritize private vehicle acquisition
   - Ensure peak hour coverage (13:00-17:00)
   - Plan Friday operations with maximum capacity

### For Employees/Drivers:

1. **Maximize Earnings:**
   - Work during **high-income days** (avoid taking these days off)
   - Focus operations in **Manhattan and Queens** for better tips
   - Consider operating during **afternoon rush hours (13:00-17:00)**

2. **Vehicle Choice:**
   - Evaluate profitability of **medium vehicles** vs. private vehicles
   - Consider trip length patterns when selecting vehicle type

3. **Strategic Positioning:**
   - Position vehicles in high-passenger boroughs
   - Avoid low-activity areas like Staten Island unless specific demand exists

## 📁 Repository Structure

```
yellowtrip-nyc-taxi-analysis/
├── data/
│   └── [Raw data files - to be uploaded]
├── reports/
│   └── Power-Bi-Presentation_Final.pptx    # Final presentation deck
├── README.md                               # Project documentation
└── .gitignore                              # Git ignore file
```

## 📊 Technologies & Tools Used

- **Power BI:** Data visualization and dashboard creation
- **Data Analysis:** Statistical analysis and pattern recognition
- **Geographic Analysis:** Borough-level insights across NYC
- **Time Series Analysis:** Temporal patterns and trends
- **Comparative Analysis:** Vendor vs. employee perspectives

## 📄 Dataset Information

### Coverage:
- **Time Period:** May-June 2020
- **Location:** New York City (5 boroughs + EWR Airport)
- **Metrics:** Trips, income, tips, passengers, vehicle types, pickup locations

### Borough Coverage:
1. Manhattan (primary market)
2. Queens
3. Brooklyn
4. Bronx
5. Staten Island
6. EWR International Airport (Newark)
7. Unknown locations (requires investigation)

## 🚀 How to Use This Analysis

### For Vendors:
1. Review geographic insights to optimize fleet distribution
2. Analyze peak hour data to ensure adequate vehicle coverage
3. Examine vehicle type preferences for fleet planning
4. Assess vendor performance metrics for competitive positioning

### For Drivers:
1. Identify high-income days and hours
2. Determine optimal operating locations
3. Evaluate vehicle type options for profitability
4. Plan work schedules around peak earning opportunities

### For Stakeholders:
1. Use insights for strategic planning
2. Reference data for market entry decisions
3. Apply findings to resource allocation
4. Leverage recommendations for operational improvements

## 📝 Future Analysis Opportunities

1. **Extended Time Period:** Analyze full year to identify seasonal patterns
2. **Pre/Post COVID-19:** Compare operations before and after pandemic impact
3. **Weather Correlation:** Examine impact of weather on trip patterns
4. **Special Events:** Analyze effect of NYC events on taxi demand
5. **Predictive Modeling:** Build models to forecast demand and optimize operations
6. **Customer Segmentation:** Deep dive into passenger behavior patterns
7. **Route Optimization:** Analyze common routes for efficiency improvements

## 👤 Author

**dcardosomr-cmd**

Data Analyst specializing in business intelligence and operational analytics.

For questions or collaboration opportunities, please reach out through GitHub.

## 💬 Q&A and Feedback

This analysis is open for discussion and refinement. If you have:
- Questions about the methodology
- Suggestions for additional analysis
- Feedback on the findings
- Requests for specific insights

Please feel free to open an issue or reach out!

---

*Analysis Period: May-June 2020*  
*Last Updated: January 2026*  
*Created with Power BI*
