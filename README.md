# 🌦️ Weather & Air Quality Monitoring Dashboard

### *One glance. Six cities. Every condition that matters.*

<p align="center">

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge&logo=powerbi)]()
[![Weather API](https://img.shields.io/badge/API-WeatherAPI-blue?style=for-the-badge)]()
[![Data](https://img.shields.io/badge/Data-Real--Time-green?style=for-the-badge)]()

</p>

🔗 **[🌤 View Live Dashboard](https://app.powerbi.com/links/nqrilG-n5C?ctid=72a00c12-baf3-47eb-963b-273fb99e18ae&pbi_source=linkShare)**

---

# 📌 Project Overview

Every day, people rely on weather information to make decisions:

*"Will it rain today?"*  
*"Is the air quality safe?"*  
*"Should I plan outdoor activities?"*

However, weather forecasts and pollution information are often scattered across multiple platforms.

This project combines **real-time weather and air quality data into a single interactive Power BI dashboard**. Using data from **[WeatherAPI](https://www.weatherapi.com/)**, the dashboard provides environmental insights across six major cities in Bangladesh:

**Dhaka | Chittagong | Rajshahi | Barisal | Khulna | Rangpur**

The dashboard transforms raw meteorological data into meaningful insights through:

- 🌡 Current weather conditions (temperature, humidity, wind, visibility, UV index)
- 📅 7-day temperature forecast
- 🌧 Rain probability prediction
- 🌅 Sunrise and sunset timings
- 🌫 Air quality monitoring (PM2.5, PM10, CO, NO₂, SO₂, O₃)

The objective is to provide users with a quick understanding of current conditions and support better environmental and daily activity planning.

---

# ✨ Key Features

| Feature | Description |
|-|-|
| 🌡 Weather Monitoring | Real-time temperature, humidity, wind speed, UV index, visibility, and pressure |
| 📅 Forecast Analysis | Dynamic 7-day temperature forecast updated according to current date |
| 🌧 Rain Prediction | Daily precipitation probability |
| 🌅 Sun Cycle | Sunrise and sunset information |
| 🌫 Air Quality | Monitoring of major pollutants with dynamic AQI indicators |
| 🏙 City Comparison | Weather analysis across six major Bangladeshi cities |

---

# ⚙️ Development Process

## 1. Data Acquisition

The dashboard retrieves live meteorological and air quality data from **WeatherAPI** through JSON-based API responses.

Data collected includes:
- Current weather conditions
- Forecast information
- Hourly weather data
- Air pollutant concentrations

---

## 2. Data Transformation

Using **Power Query Editor**, raw API responses were cleaned and prepared for analysis.

Key transformations:
- Expanded nested JSON structures
- Standardized data types
- Removed unnecessary fields
- Organized data into:

| Table | Purpose |
|-|-|
| Current Data | Real-time weather conditions |
| Forecast Data | Daily predictions |
| Hourly Forecast | Hour-by-hour conditions |
| Air Quality | Pollutant measurements |
| Locations | City filtering |

---

## 3. Data Modelling

A structured Power BI data model was created by connecting weather, forecast, air quality, and location tables.

The model enables:
- Dynamic city filtering
- Automatic visual updates
- Efficient dashboard performance

---

# 🎨 Dashboard Design & Visualization

The dashboard uses a dark-themed interface to improve readability and visual appeal.

Main visual components:

- **KPI Cards:** Temperature, humidity, wind speed, visibility, UV index, and AQI
- **Line Chart:** 7-day temperature forecast trends
- **Bar Chart:** Rain probability forecast
- **AQI Indicators:** Pollutant levels with colour-based classification
- **Sun Cycle Cards:** Sunrise and sunset information

AQI colour classification:

| Colour | Level |
|-|-|
| 🟢 Green | Good |
| 🟡 Yellow | Moderate |
| 🟠 Orange | Unhealthy |
| 🔴 Red | Hazardous |

---

# 📐 DAX Implementation

Custom DAX measures were developed for dynamic calculations and conditional formatting.

### Temperature Display

```DAX
Temperature =
ROUND(
    SELECTEDVALUE(Forecast[avgtemp_c]),
    1
) & " °C"
```

### PM2.5 Colour Classification

```DAX
PM25_Color =
VAR Value =
SELECTEDVALUE(AirQuality[pm2_5])

RETURN
SWITCH(
    TRUE(),
    Value <= 50, "#43d946",
    Value <= 100, "#fff570",
    Value <= 150, "#ff9800",
    Value <= 200, "#d93343",
    "#8b0000"
)
```

---

# 📊 Key Insights

### 🌡 Weather Trends
- Temperature patterns vary between different regions of Bangladesh.
- The 7-day forecast helps users anticipate upcoming weather conditions.

### 🌫 Air Quality Monitoring
- PM2.5 and CO provide important indicators of pollution levels.
- AQI colour classification allows quick identification of environmental conditions.

### 🌧 Weather Planning
- Rain probability and sun cycle information support better outdoor planning.

---

# 📷 Dashboard Snapshot

![Dashboard Overview](Assets/Dashboard_Final.png)

---

# 🛠 Tools & Technologies

| Category | Tools |
|-|-|
| Data Visualization | Microsoft Power BI |
| Data Transformation | Power Query |
| Analytics | DAX |
| Data Source | WeatherAPI |
| Data Format | JSON |
| Deployment | Power BI Service |

---

# 🎯 Skills Demonstrated

- Real-time API integration
- JSON data processing
- Data cleaning and transformation
- Power BI data modelling
- DAX development
- Interactive dashboard design
- Data storytelling

---

# 🔗 References

- WeatherAPI Documentation  
https://www.weatherapi.com/docs/

- Microsoft Power BI Documentation  
https://learn.microsoft.com/en-us/power-bi/

---

## 👨‍💻 Author

**Ayaz Rahman**

Power BI | Data Analytics | Data Visualization
