---
title: "SolarLog Project"
date: 2025-05-13
description: "A web application for analyzing solar energy profit based on real-time electricity market prices."
tags: ["python", "data visualization", "DevOps", "graphics","api"]
showToc: true
---

## Solar Energy Production Analysis System

This is a web application designed to monitor and analyze solar energy production in relation to electricity market prices. The project was born out of a curiosity to understand how profitable solar energy really is throughout the day and to generate insights on when it's most efficient to utilize the system.

### * Project Summary

It all started with the challenge of comparing daily production from photovoltaic panels with electricity price data from HUPX. To centralize everything, I built a system that:

1. Fetches hourly electricity prices from HUPX using a Python scraper.
2. Simultaneously pulls production data from a local inverter via REST API.
3. Cleans and combines the data to calculate revenue per hour and average productivity.
4. Stores everything in a local database for long-term tracking, reporting, and profitability analysis.

---

### -> Key Features

- **Automated Data Collection**  
  - Hourly scraping of market prices from HUPX (using BeautifulSoup + pandas).  
  - API calls to a local inverter for real-time and daily production data.

- **Analysis and Computation**  
  - Revenue calculations per hour and work-hour averages.  
  - Daily reports and monthly trend charts.  
  - "Work-hour" logic based on user-defined productive intervals—essentially the hours when the plant is actually profitable.

- **Interactive User Interface**  
  - Dynamic charts using Chart.js for daily and monthly overviews.  
  - Responsive layout with Bootstrap for all devices.  
  - Auto-refreshing data with no manual reload needed.

---

### 🏗️ Technical Architecture

#### Backend (Python + FastAPI)

1. **Web Scraper**  
   Scrapes and parses HUPX tables, normalizes date formats, and standardizes price data.

2. **Energy Service**  
   A client module that fetches production data from the inverter endpoints.

3. **TailScale Network**  
   Used to securely access the local computer that fetches production data from a SolarLog-Base-2000 device.

4. **Database**  
   SQLite using SQLAlchemy with clearly defined schemas and unique constraints to avoid duplicates.

5. **Background Module**  
   A scheduler that automatically runs at defined intervals (e.g., every hour) to:
   - Fetch updated price and production data  
   - Clean and validate entries  
   - Store records in the database  
   On failure or network error, it automatically retries and logs detailed errors for troubleshooting.

#### Frontend (HTML / CSS / JavaScript)

- **Bootstrap** for clean and fast UI design.  
- **Vanilla JS** for calling backend endpoints.  
- **Chart.js** for data visualization.

---

### 📸 UI Preview

{{< figure src="/images/UI.png" alt="App UI Overview" caption="Daily view: production, price, and revenue per hour" >}}

<div style="display: flex; gap: 1rem;">
  <div style="flex: 1;">
    {{< figure src="/images/ENDPOINTS.png" alt="API Endpoint Overview" caption="REST API architecture and flow" >}}
  </div>
  <div style="flex: 1;">
    {{< figure src="/images/API.png" alt="API Response Sample" caption="Example JSON response from the API" >}}
  </div>
</div>

---

### 📡 Sample REST API Endpoints

| Method | Path                                      | Description                          |
|--------|-------------------------------------------|--------------------------------------|
| GET    | `/api/prices`                             | Returns all collected market prices  |
| GET    | `/api/energy`                             | Returns all production measurements  |
| GET    | `/api/analysis/by-date?date=YYYY-MM-DD`   | Daily analysis for a given date      |
| GET    | `/api/analysis/by-month?month=YYYY-MM`    | Monthly report for a given month     |

---

### 📡 Sample API Requests

Used to power the application.

```bash
# Get the full list of hourly prices
curl -X GET https://your-domain.com/api/prices \
  -H "Accept: application/json"

# Analysis for May 12, 2025
curl -X GET "https://your-domain.com/api/analysis/by-date?date=2025-05-12" \
  -H "Accept: application/json"
