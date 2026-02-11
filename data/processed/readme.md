# 📂 Processed Data Overview

This folder contains curated analytical outputs derived from the raw transactional datasets.  

These files represent cleaned, aggregated, and business-ready datasets used for insight generation and visualization.

---

## Available Processed Files

### 1️⃣ avg_occupancy_by_city.csv

**Description:**  
City-level average occupancy percentage.

**Derived From:**  
`fact_aggregated_bookings.csv`

**Purpose:**  
Used to compare overall demand strength across cities and identify underperforming markets.

**Key Fields:**
- city  
- occ_pct  

---

### 2️⃣ avg_occupancy_by_room_class.csv

**Description:**  
Average occupancy percentage segmented by room category.

**Derived From:**  
`fact_aggregated_bookings.csv`

**Purpose:**  
Helps evaluate demand patterns across different room types (RT1, RT2, RT3, RT4).

**Key Fields:**
- room_class  
- occ_pct  

---

### 3️⃣ total_revenue_realized_by_city.csv

**Description:**  
Total realized revenue aggregated at the city level.

**Derived From:**  
`fact_bookings.csv`

**Purpose:**  
Used for revenue performance comparison and revenue decomposition analysis (ADR vs Occupancy).

**Key Fields:**
- city  
- revenue_realized  

---

### 4️⃣ underutilized_properties.csv

**Description:**  
List of high-capacity properties operating at comparatively lower occupancy levels.

**Derived From:**  
Merged dataset of revenue and aggregated booking tables.

**Purpose:**  
Identifies potential asset efficiency gaps and revenue optimization opportunities.

**Key Fields:**
- property_id  
- property_name  
- city  
- capacity  
- occ_pct  

---

## 🔄 Processing Logic Summary

The processed datasets were generated after:

- Removing invalid booking records
- Filtering occupancy values exceeding capacity
- Ensuring aggregation consistency using controlled `groupby` operations
- Avoiding unintended summation of unrelated numeric columns
- Recomputing derived metrics (e.g., ADR) using aggregated totals

---

## Important Notes

- These files are analytical outputs and should not be treated as raw operational data.
- All metrics are aggregated and cleaned for business insight purposes.
- Reproducibility is ensured via the main notebook located in the `notebooks/` folder.

---

## Usage

These processed files are intended for:

- Visualization generation  
- Business insight communication  
- Executive reporting  
- Further modeling or dashboard development  

For full reproducibility, refer to:

`notebooks/Atliq_Grands_Hotel_Performance_Analysis.ipynb`
