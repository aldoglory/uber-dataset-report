# 🚕 Uber Fares Dataset Analysis – Comprehensive Report

## 📂 Dataset Description and Sources

**Dataset Name:** Uber Fares Dataset  
**Source:** [Kaggle – Uber Fares Dataset by Yasser Hatim](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)

This dataset contains historical Uber trip records from New York City. Each entry includes:
- Fare paid
- Pickup and dropoff locations (latitude & longitude)
- Pickup timestamp
- Number of passengers

**Features in the Dataset:**
- `fare_amount`: Total fare charged (USD)
- `pickup_datetime`: Date and time of pickup
- `pickup_longitude`, `pickup_latitude`: Pickup GPS coordinates
- `dropoff_longitude`, `dropoff_latitude`: Dropoff GPS coordinates
- `passenger_count`: Number of passengers per trip
- `key`: Unique ride identifier

---

## 🧹 Data Cleaning Methodology

Cleaning steps were conducted in **Python (Pandas)**:

1. **Missing Values**
   - Dropped rows where `dropoff_longitude` or `dropoff_latitude` were null.

2. **Invalid Values**
   - Removed entries where:
     - `fare_amount` was negative or zero
     - `passenger_count` was zero or above six
     - Coordinates were outside the realistic NYC bounds

3. **Datetime Conversion**
   - Converted `pickup_datetime` to datetime format
   - Extracted additional fields: `hour`, `day`, `month`, `day_of_week`

4. **Export**
   - Cleaned data saved as `cleaned_uber.csv`
   - Enhanced data (with new features) saved as `enhanced_uber.csv`

---

## 📊 Key Visualizations (Power BI)

Data visualized in **Power BI Desktop**, highlighting:

### 1. Fare Distribution
- **Histogram** and **boxplot** of fare values
- Skewed distribution with several outliers

### 2. Fare vs Hour of Day
- Line chart showing higher fares during evening rush hours

### 3. Passenger Count Breakdown
- Bar chart showing majority of rides had 1 or 2 passengers

### 4. Geographic Mapping
- Pickup and dropoff points visualized on an NYC map
- High concentration in Manhattan

### 5. Temporal Trends
- Ride frequency by hour, day of the week, and month
- Interactive slicers for exploration

---

## Insights and Outcomes

### Temporal Patterns
- **Peak hours:** 5–8 PM on weekdays
- **Busy days:** Fridays and weekends

### Fare Patterns
- Higher fares observed during peak hours and weekends
- Majority of fares ranged between $5 and $15

### Spatial Insights
- Most common ride origin and destination: **Manhattan**
- Less activity in boroughs like Staten Island

### Passenger Trends
- Over 60% of rides had 1 passenger
- Group rides (4–6 passengers) were rare

### Recommendations
- Introduce **surge pricing** during peak evening hours
- Offer **discounts during off-peak** to increase usage
- Expand service coverage in **low-traffic areas**
