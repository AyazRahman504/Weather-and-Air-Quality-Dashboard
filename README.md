# 🌦️ Weather & Air Quality Monitoring Dashboard

### *One glance. Six cities. Every condition that matters.*


🔗 **[🌤 Bangladesh Weather & Air Quality Dashboard](https://app.powerbi.com/links/nqrilG-n5C?ctid=72a00c12-baf3-47eb-963b-273fb99e18ae&pbi_source=linkShare)**

---


## 📌 The Story Behind This Dashboard

Every morning, millions of people ask the same three questions: *Will it rain today? Is the air safe to breathe? Should I carry an umbrella or sunscreen?* Usually, answering that means bouncing between a weather app, a pollution tracker, and a news alert — three tabs for one decision.

This project set out to close that gap. Built in **Power BI**, the dashboard brings together **live weather conditions, a 7-day forecast, air quality readings, and rain probability** into a single, story-driven view — for **six major cities across Bangladesh**: Dhaka, Chittagong, Rajshahi, Barisal, Khulna, and Rangpur. Here real-time data is used from [WeatherAPI](https://www.weatherapi.com/) to deliver actionable insights into:  
- **Current weather metrics**: temperature, humidity, wind speed, UV index, visibility, and atmospheric pressure.  
- **7-day forecast trends**: dynamically displayed starting from the next day relative to the current date.  
- **Sun cycle information**: sunrise and sunset timings for local planning.  
- **Precipitation probabilities**: rain forecast across cities.  
- **Air Quality Index (AQI)**: includes PM2.5, PM10, CO, NO₂, SO₂, and O₃ with dynamic color coding.  

The goal wasn't just to display numbers. It was to turn raw meteorological and pollutant data into a narrative anyone can read in seconds — a forecast that tells you not just *what* the weather will be, but *what to do about it*.

---

## 🛠 Methodology

### 1. Data Acquisition
- Connected to WeatherAPI endpoints for **current weather**, **7-day forecast**, and **air quality metrics**.  
- Retrieved **JSON-formatted live data**, compatible with Power BI and other programming environments.

### 2. Data Transformation
- Flattened nested JSON structures using Power Query Editor.  
- Standardized column types for numeric, date/time, and textual values.  
- Removed duplicates and redundant columns to optimize data structure.  
- Generated separate tables for **Current Data**, **Forecast Data**, **Forecast Hours**, and **Air Quality**.  
- Created a **master table** to consolidate city-wise data, allowing easy expansion for future cities.

### 3. Data Modeling
- Created **Locations** dimension table and established relationships with all weather and forecast tables.  
- Configured filter propagation so selecting a city dynamically updates **current, forecast, and air quality data**.  
- Hidden intermediate tables to reduce clutter while retaining proper model functionality.

### 4. Dashboard Design & Visualization
- Applied a **dark, glossy theme** for modern aesthetics.  
- Implemented **KPI cards** for temperature, wind speed, humidity, visibility, UV index, and AQI.  
- Created **line charts** for 7-day temperature forecasts with smooth gradients.  
- Designed **gauge and donut charts** for pollutant AQI components with dynamic color indicators.  
- Constructed **horizontal bar charts** for rain probability visualization.  
- Integrated icons for weather conditions, rain, visibility, sunrise, and sunset.

### 5. Dynamic Measures & DAX Implementation
- Created **DAX measures** for conditional formatting, e.g., AQI color coding for CO, PM2.5, PM10.  
- Generated **current and forecast temperature measures** with unit formatting (°C).  
- Built **left/right rain probability measures** to visualize the chance of precipitation out of 100%.  
- Configured **dynamic indicators** for pollutant thresholds (red for high, green for safe) to enhance visual comprehension.

### 6. Interactivity & Usability
- Added **city selection slicers** for user-friendly filtering.  
- Configured **day-of-week labels** for forecast visualization to update automatically with live data.  
- Implemented **auto-refresh** through Power BI Service to maintain real-time weather accuracy across all cities.


---

## 📷 Dashboard Snapshot

![Dashboard Overview](Assets/Dashboard_Final.png)

---

## 🔗 Tools Used
`Power BI Desktop` • `Power Query` • `DAX` • Weather & Air Quality Data Sources
