# Notebooks – Analysis Workflow

This folder contains the Jupyter Notebook used to perform the end-to-end hospitality performance analysis for Atliq Grands.

---

## Contents

- `hotels_analysis.ipynb`  
  Main analysis notebook containing data exploration, cleaning, transformation, and business insight generation.

---

## Purpose of the Notebook

The notebook is designed to:

- Analyze occupancy performance across cities and hotel categories
- Identify weekday vs weekend demand gaps
- Evaluate capacity utilization at property level
- Decompose revenue into ADR (Average Daily Rate) and Occupancy drivers
- Assess customer ratings and their relationship to performance
- Generate actionable business insights

This notebook transforms raw operational data into decision-ready insights.

---

## 🧭 Notebook Structure

The analysis follows a structured workflow:

### 1️⃣ Problem Understanding
- Business context: Lower occupancy in certain cities and room categories
- Objective: Improve revenue realization and operational efficiency

### 2️⃣ Data Loading
- fact_bookings.csv
- fact_aggregated_bookings.csv
- dim_hotels.csv
- Other supporting datasets

### 3️⃣ Data Exploration (EDA)
- Unique property checks
- Booking distribution
- Capacity validation
- Occupancy computation
- Revenue aggregation

### 4️⃣ Data Cleaning
- Removed invalid bookings (successful bookings > capacity)
- Checked null values
- Ensured consistent column naming
- Validated merges between fact tables

### 5️⃣ Data Transformation
- Created occupancy percentage column
- Calculated ADR (Revenue / Successful Bookings)
- Merged revenue and occupancy data
- Created city-level and property-level summaries
- Aggregated monthly revenue trends
- Generated weekday vs weekend analysis

### 6️⃣ Visualization & Insights
The notebook generates:
- City-wise occupancy trends
- Room category heatmap
- ADR vs Occupancy decomposition
- Revenue contribution by property category
- Booking platform revenue share
- Underutilized property identification

---

## 📊 Key Analytical Outputs Generated

All final visuals and summary tables are exported to the `/outputs/` folder.

These include:
- ADR vs Occupancy bubble chart
- Capacity vs Utilization scatter
- Monthly revenue trends
- Occupancy heatmaps
- Revenue breakdown charts
- Weekday vs Weekend comparison

---

## ▶️ How to Run the Notebook

1. Install required dependencies:
pip install -r ../requirements.txt

2. Ensure raw CSV files are placed in the `/data/` folder.

3. Open Jupyter Notebook:

4. Run all cells sequentially.

---

## 📌 Assumptions

- Raw data is provided by a Data Engineering team.
- Data reflects real operational hotel booking transactions.
- Revenue is realized revenue (not potential revenue).
- Capacity values are accurate and validated.

---

## 💼 Business Value

This notebook demonstrates:

- Structured analytical thinking
- Correct fact table merging strategy
- Revenue decomposition logic (ADR vs Occupancy)
- Stakeholder-focused visualization
- Data-driven decision-making

The output supports strategic pricing, demand management, and operational optimization decisions.

---

