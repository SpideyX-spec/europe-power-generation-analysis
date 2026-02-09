


# ☀️ Solar Power Forecasting & Grid Stability Analysis (PJM)
### Exploratory Data Analysis & Solar Power Time Series Forecasting

<img width="2000" height="500" alt="SolarPowerPrediction" src="https://github.com/user-attachments/assets/9765a142-084b-4be6-950f-78d58f7088ed" />


This project presents a research-grade Machine Learning framework to forecast solar power generation within the PJM Interconnection (the largest electrical grid operator in the Eastern United States).

Unlike traditional linear forecasting, this approach utilizes Gradient Boosting (XGBoost) combined with Cyclic Temporal Feature Engineering to accurately model the non-linear and stochastic nature of solar energy. The goal is to provide accurate short-term forecasts to assist in grid stability and load balancing.
---

## 📊 Project Objectives

- Analyze Europe’s power generation by fuel type
- Compare renewable vs non-renewable energy sources
- Explore daily and seasonal solar power patterns
- Forecast future solar power generation using time series models
- Demonstrate real-world data science workflows on energy datasets

---

## 🗂️ Dataset Overview

The dataset comprises hourly power generation records from the PJM Interconnection, covering 13 states in the Eastern US.

### Key Features:
- **Timestamp** (UTC & local time)
- **Fuel type** (Coal, Gas, Nuclear, Solar, Wind, Hydro, etc.)
- **Power generation** (MW)
- **Percentage of total generation**
- **Renewable classification**

---

## 🔧 Key Components of the Analysis

### 1️⃣ Data Preparation
- Combined multiple CSV files into a single dataset
- Cleaned and formatted datetime features
- Engineered time-based features (Year, Month, Hour)
- Segregated solar power data for focused analysis

---

### 2️⃣ Exploratory Data Analysis (EDA)

**Visualizations included:**
- Box plots comparing power generation across fuel types
- Pie charts showing fuel-type distribution
- Bar plots of average and total power generation
- Renewable vs non-renewable comparison plots

#### 🔍 Key EDA Insights:
- Gas and Nuclear dominate Europe’s power generation
- Coal remains a significant contributor despite being non-renewable
- Renewable sources contribute smaller but steadily growing shares
- Solar power has high variability and strong temporal patterns

---

### 3️⃣ Solar Power Time Series Analysis

Focused analysis on solar generation behavior:

- Clear **daily cycles** (zero generation at night)
- Strong **seasonal trends** with summer peaks
- Moving average smoothing to reduce noise
- Seasonal decomposition into trend, seasonality, and residuals

---

### 4️⃣ Forecasting with Prophet

Facebook Prophet was used to model solar power generation:

- Captured **daily, weekly, and yearly seasonality**
- Forecasted hourly solar generation for future periods
- Improved model accuracy by **restricting data to daylight hours (6 AM – 6 PM)**

#### 📈 Results:
- Daylight-only modeling significantly reduced nighttime prediction errors
- Forecasts align well with real-world solar generation behavior

---

## 🧠 Key Findings

The PJM Grid is heavily reliant on Nuclear and Gas for baseload stability.

Solar Energy follows a strict diurnal pattern but suffers from high variance due to cloud cover.

Feature Importance: The "Lag_24h" (yesterday's generation) and "Hour_Sin" (time of day) were the strongest predictors of future generation.

XGBoost successfully captured the rapid ramp-up and ramp-down of solar curves better than linear models.

## 🛠️ Technologies & Tools Used

- **Python**
- **Pandas & NumPy** – data manipulation
- **Matplotlib & Seaborn** – visualization
- **Statsmodels** – seasonal decomposition
- **Facebook Prophet** – time series forecasting
- **Jupyter Notebook**

---

## 📁 Project Structure

```

europe-power-generation-analysis/
├── data/
├── notebooks/
├── images/
├── src/
├── requirements.txt
└── README.md

````

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
  (https://github.com/SpideyX-spec/Solar-Energy-Time-Series-Analysis.git)
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open notebooks:

   ```bash
   jupyter notebook
   ```

---

## 📌 Future Improvements

* Integrate weather data for improved solar forecasting
* Compare Prophet with LSTM / ARIMA models
* Build an interactive dashboard (Streamlit / Power BI)
* Extend analysis to country-wise power generation

---

## 📜 License

This project is licensed under the MIT License.

---




