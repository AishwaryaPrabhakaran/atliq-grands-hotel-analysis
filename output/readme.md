#  Outputs Interpretation Guide

This folder contains finalized visualizations generated from the analysis notebook.  
Each visual addresses a specific business question and supports data-driven decision-making.

---

## 1️⃣ ADR vs Occupancy (City-Level Decomposition)

**File:** `adr_vs_occupancy_by_city.png`

**Business Question:**  
Are revenue differences across cities driven by pricing (ADR) or demand (Occupancy)?

**How to Interpret:**
- X-axis → Average Daily Rate (Pricing Power)
- Y-axis → Occupancy (%) (Demand Strength)
- Bubble Size → Total Revenue

If larger bubbles align more strongly with ADR than occupancy, revenue is pricing-driven.

**Key Insight:**  
Revenue variation across cities aligns more closely with ADR than occupancy, indicating pricing strategy is the primary revenue driver.

---

## 2️⃣ Weekday vs Weekend Occupancy by City

**File:** `weekday_vs_weekend_occupancy_by_city.png`

**Business Question:**  
Is there a structural demand gap between weekdays and weekends?

**How to Interpret:**
- Compare weekday and weekend bars for each city.
- A consistent weekend premium indicates weekday underutilization.

**Key Insight:**  
Weekend occupancy consistently outperforms weekday occupancy across all cities, indicating a portfolio-wide weekday demand gap.

---

## 3️⃣ Monthly Revenue Trend by City

**File:** `monthly_revenue_by_city.png`

**Business Question:**  
How stable is revenue performance across time periods?

**How to Interpret:**
- Compare revenue trend lines across cities.
- Identify seasonal dips or volatility.

**Key Insight:**  
Revenue patterns show relative stability, with differences largely influenced by pricing strategy rather than sudden demand shifts.

---

## 4️⃣ Revenue by Property Category

**File:** `revenue_by_property_category.png`

**Business Question:**  
Which hotel category contributes more to total revenue?

**How to Interpret:**
- Compare total revenue between Luxury and Business segments.

**Key Insight:**  
Luxury properties generate significantly higher realized revenue, primarily driven by higher ADR rather than higher occupancy.

---

## 5️⃣ Average Occupancy by City

**File:** `avg_occupancy_by_city.png`

**Business Question:**  
Which cities demonstrate stronger demand performance?

**How to Interpret:**
- Higher occupancy indicates stronger demand.
- Compare city ranking.

**Key Insight:**  
Delhi shows the highest occupancy levels, suggesting strong demand and potential pricing optimization opportunity.

---

## 6️⃣ Capacity vs Occupancy (Property-Level Utilization)

**File:** `high_capacity_vs_low_occupancy.png`

**Business Question:**  
Are high-capacity properties being effectively utilized?

**How to Interpret:**
- X-axis → Property Capacity
- Y-axis → Occupancy (%)
- Identify properties with high capacity but low occupancy.

**Key Insight:**  
Certain high-capacity properties operate below optimal occupancy, indicating asset efficiency gaps.

---

## 7️⃣ Occupancy Heatmap (City × Room Category)

**File:** `occupancy_heatmap_city_room_category.png`

**Business Question:**  
How does room-type demand vary across cities?

**How to Interpret:**
- Darker shades indicate higher occupancy.
- Compare performance across RT1, RT2, RT3, RT4 categories.

**Key Insight:**  
Demand patterns vary across room categories, enabling targeted pricing and promotional strategies.

---

## 8️⃣ Revenue by Booking Platform

**File:** `revenue_by_booking_platform.png`

**Business Question:**  
Is revenue concentrated across specific booking channels?

**How to Interpret:**
- Compare contribution share across platforms.
- Identify potential channel concentration risk.

**Key Insight:**  
Revenue dependence on specific platforms highlights potential risk and opportunity for channel diversification.

---

#  How to Use This Folder

These visuals are intended for:

- Executive presentations  
- Stakeholder discussions  
- Strategic pricing decisions  
- Operational performance reviews  

For reproducibility, refer to the main analysis notebook in the `notebooks/` directory.

---

# 🔍 Analytical Integrity

All metrics shown in these outputs are derived from:

- Cleaned datasets
- Controlled aggregations
- Properly weighted ADR calculations
- Validated occupancy formulas

The visuals reflect business-level summaries rather than raw transactional data.
