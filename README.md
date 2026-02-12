# Atliq Grands – Hotel Performance & Revenue Optimization Analysis

## Executive Summary

Atliq Grands operates multiple luxury and business hotels across major Indian cities.  
Management observed uneven occupancy levels, revenue concentration in select markets, and a consistent weekday performance gap.

This analysis evaluates hotel performance across cities, room categories, and time periods to determine:

- Whether revenue differences are driven by pricing (ADR) or demand (occupancy)
- Where asset utilization gaps exist
- Which cities require demand stimulation vs pricing optimization
- How service quality influences occupancy performance

---

## 🎥 Executive Presentation

The final business presentation and walkthrough are available below:

| Resource | Link |
|-----------|------|
| 📂 Slide Deck (PDF) | [Open Presentation Folder](presentation/) |
| 🎬 Video Walkthrough | https://youtu.be/W60ZW_lJUTc |

---


## Business Objectives

- Diagnose city-level revenue performance
- Decompose revenue into ADR (pricing power) and Occupancy (demand strength)
- Identify underutilized high-capacity properties
- Evaluate weekday vs weekend demand variation
- Assess revenue contribution by hotel category and booking platform
- Provide actionable, data-driven strategic recommendations

---

## 📂 Data Overview

The dataset consists of structured CSV files extracted from the operational hotel database:

- **fact_bookings.csv** – Transaction-level booking and revenue data  
- **fact_aggregated_bookings.csv** – Property-level booking summary and capacity data  
- **dim_hotels.csv** – Property metadata (city, category)

Data was merged using `property_id` as the primary key.

---

## 🔍 Key Analytical Insights

### 1️⃣ Revenue is Primarily Pricing-Driven (ADR-Led)

City-level decomposition shows that revenue variation aligns more closely with ADR than occupancy:

- **Mumbai** generates the highest revenue due to the strongest ADR, not highest occupancy.
- **Delhi** records the highest occupancy but comparatively lower revenue, indicating pricing optimization opportunity.

 **Conclusion:** Pricing strategy plays a stronger role in revenue performance than demand variation.

---

### 2️⃣ Weekday Demand Gap is Structural

Across all cities, weekend occupancy consistently exceeds weekday occupancy.

 **Implication:** Underutilized weekday capacity represents a portfolio-wide opportunity.

---

### 3️⃣ Bangalore Requires Demand-Side Intervention

- Relatively strong ADR
- Lowest occupancy among major cities

 **Implication:** Demand stimulation (not pricing reduction) should be prioritized.

---

### 4️⃣ Delhi Has Pricing Upside Potential

- Highest occupancy levels
- Moderate ADR compared to Mumbai

 **Implication:** Controlled ADR testing may unlock incremental revenue without harming occupancy.

---

### 5️⃣ Underutilized High-Capacity Properties Identified

Several high-capacity properties operate below optimal occupancy levels, indicating asset efficiency gaps.

 **Implication:** Targeted demand initiatives can significantly improve return on fixed assets.

---

### 6️⃣ Luxury Segment Drives Revenue Contribution

Luxury properties generate higher realized revenue primarily due to higher ADR rather than occupancy dominance.

---

### 7️⃣ Service Quality Shows Moderate Demand Influence

Cities with stronger customer ratings tend to maintain healthier occupancy levels, though pricing remains the primary revenue driver.

---

## 📈 Revenue Decomposition Framework

Revenue was decomposed using:
Revenue = ADR × Successful Bookings
Occupancy (%) = Successful Bookings / Capacity

City-level ADR was calculated using weighted totals:
ADR = Total Revenue / Total Successful Bookings
This ensured correct aggregation and avoided averaging distortions.

---

## Strategic Recommendations

### 1. Optimize Pricing in High-Demand Markets (Delhi)
Implement controlled ADR increases through:
- Segmented pricing experiments
- Premium upselling strategies
- Event-driven rate optimization

---

### 2. Stimulate Demand in Bangalore
Focus on:
- Corporate weekday partnerships
- Mid-week bundled offers
- Localized marketing initiatives

---

### 3. Address Weekday Underutilization (Portfolio-Wide)
Introduce:
- Long-stay weekday discounts
- Business travel incentives
- Dynamic pricing strategies

---

### 4. Improve Utilization of High-Capacity Properties
- Event & conference sales initiatives
- Strategic partnerships
- Property-level performance audits

---

### 5. Protect Premium Pricing in Mumbai
Maintain pricing power while preserving occupancy stability.

---

## 🛠 Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📁 Repository Structure

```
atliq-grands-hotel-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── outputs/
│   ├── adr_vs_occupancy.png
│   ├── weekday_vs_weekend.png
│   └── revenue_by_category.png
│
├── notebooks/
│   └── Atliq_Grands_Hotel_Performance_Analysis.ipynb
│
├── README.md
└── requirements.txt
```

---


---

## 💼 Project Outcome

This project demonstrates:

- Structured business problem framing
- Multi-table data integration
- Correct metric derivation (ADR & Occupancy)
- Revenue decomposition methodology
- Asset utilization analysis
- Executive-level insight communication

The analysis provides actionable guidance for pricing optimization, demand stimulation, and operational efficiency improvement.


