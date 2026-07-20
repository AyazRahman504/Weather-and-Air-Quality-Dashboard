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

## 🛠 Development Process

### 1. Data Acquisition
- Integrated **WeatherAPI** to retrieve real-time weather information, 7-day forecasts, and air quality data for selected cities in Bangladesh.
- Extracted live data in **JSON format** and connected it directly to Power BI for automated data visualization and analysis.
- Collected key parameters including temperature, humidity, wind conditions, precipitation probability, sunrise/sunset timings, and air pollutant levels.

---

### 2. Data Transformation
- Processed and cleaned raw API responses using **Power Query Editor**.
- Expanded nested JSON structures into structured tables suitable for analysis.
- Standardized data formats for numerical values, timestamps, and categorical fields to ensure consistency.
- Removed unnecessary columns and duplicate records to improve data quality and model efficiency.
- Organized the dataset into separate tables:
  - **Current Weather Data** – real-time weather conditions
  - **Forecast Data** – daily weather predictions
  - **Hourly Forecast Data** – detailed hourly conditions
  - **Air Quality Data** – pollutant measurements
- Developed a consolidated master structure to simplify city-wise analysis and allow future expansion to additional locations.

---

### 3. Data Modeling
- Created a dedicated **Locations dimension table** to manage city selections across the dashboard.
- Established relationships between location, weather, forecast, and air quality tables to ensure accurate data filtering.
- Designed the data model so that selecting a city automatically updates all related visuals, including current conditions, forecasts, and pollution levels.
- Hidden supporting tables and intermediate queries to maintain a cleaner and more user-friendly Power BI model.

---

### 4. Dashboard Design & Visualization
- Developed a modern **dark-themed dashboard interface** to improve readability and create a visually engaging user experience.
- Designed KPI cards to display key weather indicators:
  - Temperature
  - Humidity
  - Wind speed
  - Visibility
  - UV index
  - Air Quality Index
- Created interactive visualizations including:
  - **Line chart:** 7-day temperature forecast trends
  - **Bar chart:** Rain probability forecast
  - **Gauge/indicator charts:** Air quality monitoring
  - **Cards:** Sunrise and sunset information
- Added weather-related icons and visual elements to improve user understanding and make the dashboard more intuitive.

---

### 5. Dynamic Measures & DAX Implementation
- Developed custom **DAX measures** to enhance dashboard functionality and automate calculations.
- Implemented dynamic color indicators to classify pollutant levels based on air quality thresholds:
  - Green → Good air quality
  - Yellow → Moderate
  - Orange/Red → Higher pollution levels
- Created calculated measures for:
  - Current temperature display with units (°C)
  - Forecast temperature trends
  - Rain probability percentages
  - Pollutant concentration indicators (CO, PM2.5, PM10, NO₂, SO₂, O₃)
- Applied conditional formatting to allow users to quickly identify environmental conditions.

---

### 6. Interactivity & User Experience
- Added city selection controls to allow users to switch between different locations dynamically.
- Designed forecast labels to automatically adjust based on the current date, ensuring the dashboard always displays the upcoming 7-day forecast.
- Published the dashboard through **Power BI Service** with scheduled refresh capability to maintain updated weather information from the live API source.
- Optimized the overall layout and navigation to provide a simple and intuitive user experience.

---

## 📷 Dashboard Snapshot

![Dashboard Overview](Assets/Dashboard_Final.png)

---

## 🔗 Tools Used
`Power BI Desktop` • `Power Query` • `DAX` • Weather & Air Quality Data Sources
