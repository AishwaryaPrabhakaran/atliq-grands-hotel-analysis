## 📊 Dataset Metadata (Data Dictionary)

The raw dataset consists of fact and dimension tables extracted from the operational hotel database. Below is a summary of key fields available in each dataset.

---

### 1️⃣ fact_bookings.csv  
Transactional-level booking data.

| Column Name          | Description |
|----------------------|------------|
| booking_id           | Unique identifier for each booking transaction |
| property_id          | Unique identifier for hotel property |
| booking_date         | Date when booking was made |
| check_in_date        | Guest check-in date |
| check_out_date       | Guest check-out date |
| no_guests            | Number of guests in the booking |
| room_category        | Type of room booked (RT1, RT2, etc.) |
| revenue_generated    | Gross revenue generated from booking |
| revenue_realized     | Actual realized revenue after cancellations/refunds |
| ratings_given        | Customer rating provided for the stay |

---

### 2️⃣ fact_aggregated_bookings.csv  
Property-level aggregated booking data (daily granularity).

| Column Name          | Description |
|----------------------|------------|
| property_id          | Unique identifier for hotel property |
| check_in_date        | Date of occupancy |
| room_category        | Room type |
| successful_bookings  | Number of confirmed bookings |
| capacity             | Total available room capacity |

Derived Metric:
- **Occupancy (%) = (successful_bookings / capacity) × 100**

---

### 3️⃣ dim_hotels.csv  
Property metadata table.

| Column Name   | Description |
|---------------|------------|
| property_id   | Unique identifier for hotel property |
| property_name | Name of hotel |
| category      | Hotel category (Luxury / Business) |
| city          | City where property is located |

---

## 🔗 Data Relationships

- `property_id` serves as the primary key linking fact and dimension tables.
- Revenue metrics are derived from `fact_bookings`.
- Occupancy metrics are derived from `fact_aggregated_bookings`.
- City and category attributes are sourced from `dim_hotels`.

---

## 📌 Assumptions

- CSV files are assumed to be extracted by a Data Engineer from the operational business database.
- Data reflects historical booking activity across multiple cities.
- No personally identifiable customer data is included.
