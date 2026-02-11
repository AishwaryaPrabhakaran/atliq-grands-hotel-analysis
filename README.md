# 🏨 Atliq Grands Hotel Performance Analysis

##  Business Problem

Atliq Grands is a multi-city hotel chain operating across different property types and locations.  
The management team has observed uneven occupancy levels across cities and a noticeable revenue concentration in specific markets. Additionally, weekday performance appears weaker compared to weekends.

The business seeks to understand:

- Why revenue varies across cities  
- Whether performance gaps are demand-driven or pricing-driven  
- Which properties are underutilized  
- Where strategic intervention is required  

This project analyzes historical booking data to derive actionable insights that improve occupancy, pricing strategy, and asset utilization.

---

## Objectives & Hypothesis

### Primary Objective
To diagnose revenue performance across cities by decomposing it into:
- Pricing Driver → Average Daily Rate (ADR)
- Demand Driver → Occupancy Percentage

### Hypothesis
Revenue differences across cities are more influenced by pricing strategy (ADR) than occupancy variations.

### Supporting Analytical Goals
- Evaluate weekday vs weekend occupancy patterns
- Identify high-capacity underutilized properties
- Analyze revenue contribution by hotel category
- Assess relationship between customer ratings and occupancy

---

## Data Collection

The dataset consists of structured CSV files assumed to be extracted by a Data Engineer from the operational business database.

### Data Sources:

- `fact_bookings.csv`  
  Transaction-level booking data including revenue, guests, and ratings.

- `fact_aggregated_bookings.csv`  
  Property-level aggregated booking data including capacity and successful bookings.

- `dim_hotels.csv`  
  Property metadata including city, hotel name, and category.

The analysis integrates multiple fact tables using `property_id` as the primary key.

---

## Data Exploration

Exploratory analysis focused on understanding:

- Distribution of occupancy across cities
- Room-category performance
- Revenue contribution by property type
- Weekday vs weekend trends
- Property-level capacity utilization
- Customer rating patterns

Preliminary findings revealed:
- Consistent weekend outperformance across cities
- Significant revenue concentration in specific markets
- Variation in performance across hotel categories

---

## Data Cleaning

The following steps were performed to ensure data reliability:

- Removed records where successful bookings exceeded capacity
- Filtered invalid occupancy values
- Ensured no division-by-zero errors during metric computation
- Verified merge integrity between fact tables
- Avoided accidental aggregation of unrelated numeric columns

All aggregations were explicitly controlled using `.agg()` to prevent unintended summations.

---

## 🔄 Data Transformation & Feature Engineering

Several business-relevant metrics were derived:

### 1️⃣ Occupancy Percentage
Occupancy (%) = (Successful Bookings / Capacity) × 100

### 2️⃣ Average Daily Rate (ADR)
ADR = Total Revenue Realized / Total Successful Bookings
ADR was computed using aggregated totals to ensure correct weighted calculation.

### 3️⃣ Revenue Decomposition
City-level revenue was decomposed into:
- ADR (Pricing component)
- Occupancy (Demand component)

This enabled identification of the primary revenue driver.

---

## 📊 Key Insights

### 1️⃣ Revenue is Primarily Pricing-Driven (ADR-Led)

City-level decomposition shows that revenue differences align more closely with ADR than occupancy levels.

- Mumbai generates the highest revenue due to strong pricing power.
- Delhi exhibits the highest occupancy but comparatively lower revenue, indicating pricing optimization opportunity.

---

### 2️⃣ Weekday Underperformance is Structural

Weekend occupancy consistently exceeds weekday occupancy across all cities, indicating a portfolio-wide weekday demand gap.

---

### 3️⃣ Bangalore Requires Demand Stimulation

Bangalore demonstrates relatively high ADR but the lowest occupancy among major cities, suggesting demand-side intervention is required.

---

### 4️⃣ High-Capacity Properties Are Underutilized

Certain large-capacity properties operate below optimal occupancy levels, representing asset efficiency gaps.

---

### 5️⃣ Luxury Segment Drives Revenue

Luxury properties contribute significantly higher realized revenue than business-category hotels, primarily due to stronger pricing rather than higher occupancy.

---

### 6️⃣ Service Quality Influences Demand

Cities with stronger customer ratings tend to maintain healthier occupancy levels, indicating service quality impacts booking performance.

---

## 🏢 Business Recommendations

- Implement controlled ADR optimization in high-demand cities (e.g., Delhi)
- Stimulate weekday demand through corporate partnerships and midweek offers
- Maintain premium pricing strategy in Mumbai
- Launch demand-generation initiatives in Bangalore
- Improve service consistency in lower-rated properties
- Enhance utilization strategies for high-capacity hotels

---

## 🛠 Tools & Technologies Used

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

## 📈 Project Outcome

This analysis demonstrates how revenue performance can be systematically decomposed into pricing and demand components, enabling data-driven strategic decision-making across cities and property categories.

The findings provide actionable direction for pricing optimization, demand stimulation, and operational improvement initiatives.

