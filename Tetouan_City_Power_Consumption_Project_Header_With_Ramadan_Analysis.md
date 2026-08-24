# Tetouan City Power Consumption Analysis

## Project Overview

This project analyzes electricity consumption across three distribution zones in Tetouan City, Morocco.

The dataset contains measurements recorded at 10-minute intervals throughout 2017. It combines electricity-consumption data with several weather and solar-radiation variables.

The objective is to identify important patterns in electricity demand, determine when peak consumption occurs, investigate how weather conditions relate to demand, and develop insights that may support load planning and operational decision-making.

The dataset contains 52,417 observations and represents a multivariate time-series and regression problem.

---

## Business Problem

Electricity providers must understand when and where demand is highest so that they can:

- maintain reliable electricity service;
- prepare for peak-demand periods;
- identify unusual consumption patterns;
- support capacity and infrastructure planning;
- improve forecasting;
- allocate operational and maintenance resources more effectively.

This project will explore electricity-consumption patterns across three city zones and assess how demand changes according to time, season and weather conditions.

---

## Dataset Columns

| Column Name | Description |
|---|---|
| `DateTime` | Date and time when each observation was recorded. Readings occur at approximately 10-minute intervals throughout 2017. |
| `Temperature` | Outdoor air temperature recorded at the time of the observation. |
| `Humidity` | Amount of moisture present in the air. |
| `Wind Speed` | Outdoor wind-speed measurement. |
| `general diffuse flows` | Total solar radiation reaching the area, including direct and indirect radiation. |
| `diffuse flows` | Solar radiation reaching the surface indirectly after being scattered by clouds, particles and the atmosphere. |
| `Zone 1 Power Consumption` | Electricity-consumption reading for Zone 1. |
| `Zone 2 Power Consumption` | Electricity-consumption reading for Zone 2. |
| `Zone 3 Power Consumption` | Electricity-consumption reading for Zone 3. |

> **Note:** Before reporting exact electricity units, the dataset documentation and original research should be reviewed because the displayed dataset does not clearly identify the measurement unit.

---

# Questions to Ask of the Data

## 1. Data Quality and Preparation

1. What are the dataset dimensions, date range and column data types?
2. Are there missing values, duplicate rows or irregular gaps in the 10-minute time sequence?
3. Are there suspicious, impossible or extreme values in the weather and electricity-consumption columns?

---

## 2. Overall Electricity Demand

1. Which zone has the highest total and average electricity consumption?
2. What percentage of total city consumption is contributed by each zone?
3. Which zone has the greatest overall variation in electricity demand?

---

## 3. Hourly Demand Patterns

1. During which hours is electricity consumption highest and lowest?
2. Do the three zones reach peak demand at the same hour?
3. Are there clear morning, daytime or evening demand patterns?

---

## 4. Daily and Weekly Patterns

1. Which days of the week have the highest and lowest average consumption?
2. Is electricity demand different on weekdays and weekends?
3. Does the weekday-versus-weekend pattern differ across the three zones?

---

## 5. Monthly and Seasonal Patterns

1. Which months and seasons have the highest and lowest average consumption?
2. Do seasonal demand patterns differ across the three zones?
3. Is there a noticeable upward or downward trend in consumption during the year?

---

## 6. Weather and Electricity Consumption

1. What relationships exist between temperature, humidity and electricity consumption?
2. Do wind speed and solar-radiation variables have meaningful relationships with demand?
3. Which weather variables appear most useful for explaining or predicting consumption?

---

## 7. Peak-Demand Analysis

1. When do the highest electricity-consumption readings occur in each zone?
2. Are peak-demand events concentrated during particular hours, months or seasons?
3. What weather conditions are present during major peak-demand periods?
4. Which zone contributes most to combined city demand during system-wide peaks?

---

## 8. Variability and Operational Risk

1. Which zone has the most volatile or least predictable electricity demand?
2. When do the largest daily demand swings occur?
3. Can unusual consumption events be identified using statistical or rolling methods?

---

## 9. Relationships Between Zones

1. How strongly are electricity-consumption levels correlated across the three zones?
2. Which zones have the most similar demand patterns?
3. Are unusual demand events shared across the city or isolated to individual zones?

---

## 10. Ramadan Electricity-Consumption Analysis

Ramadan in Morocco began on **27 May 2017** and continued through **25 June 2017**, with Eid al-Fitr observed on **26 June 2017**.

1. How did hourly electricity-consumption patterns during Ramadan differ from the periods immediately before and after Ramadan?
2. Did demand shift around important daily periods such as the hours before sunset, after iftar and later in the evening?
3. Did the Ramadan demand pattern differ across the three electricity-distribution zones?
4. Were Ramadan peak-demand times or consumption levels significantly different from comparable non-Ramadan days?

> **Scope note:** This analysis will focus on changes in the timing and shape of electricity demand. Where possible, Ramadan days should be compared with nearby non-Ramadan days that have similar weather and seasonal conditions.

---

## 11. Load Forecasting

1. Can short-term electricity consumption be predicted accurately for each zone?
2. Does adding weather and time-based information improve forecast accuracy?
3. Which simple forecasting approach performs best on unseen data?

> **Scope note:** Forecasting will only begin after the exploratory analysis is complete. The first model should be simple and interpretable rather than an extensive comparison of many algorithms.

---

# Possible Engineered Features

The following columns may be created from `DateTime`:

- `Date`
- `Year`
- `Month`
- `Month_Name`
- `Week`
- `Day`
- `Day_Name`
- `Hour`
- `Minute`
- `Season`
- `Is_Weekend`
- `Time_of_Day`

Additional analytical features may include:

- `Total_Power_Consumption`
- `Average_Zone_Consumption`
- `Zone_1_Percentage`
- `Zone_2_Percentage`
- `Zone_3_Percentage`
- `Daily_Peak_Consumption`
- `Daily_Minimum_Consumption`
- `Daily_Load_Range`
- rolling averages;
- lagged consumption values;
- peak-demand indicators;
- anomaly indicators.

> **Scope note:** These features will not all be created automatically. We will add only the features required for the specific analysis question being answered.

---

# Initial Project Scope

The first version of the project will focus on:

1. inspecting and cleaning the dataset;
2. creating essential time-based features;
3. analyzing electricity demand by zone;
4. identifying hourly, weekly and seasonal patterns;
5. investigating the main relationships between weather and demand;
6. identifying peak and unusual consumption periods;
7. analyzing electricity demand during Ramadan;
8. creating clear visualizations;
9. summarizing operational and planning insights.

A simple forecasting model may be developed after the exploratory analysis is complete.

---

# Expected Deliverables

- Cleaned analytical dataset
- Jupyter Notebook containing the analysis
- Data dictionary
- Exploratory data analysis
- Peak-demand analysis
- Weather and consumption analysis
- Ramadan electricity-consumption analysis
- Four-chart analytical dashboard
- Written findings and recommendations
- Optional short-term load-forecasting model

---

# Main Project Question

> How do time, season, weather conditions and Ramadan-related changes in daily activity influence electricity consumption across the three distribution zones of Tetouan City, and what patterns could support peak-demand management, load planning and short-term forecasting?
