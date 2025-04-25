# Data Dinosaurs: NO₂ Concentration Trends in Maine and Utah

## Repository Overview
Welcome to the Data Dinosaurs' project repository! This repository contains our analysis of NO₂ concentration trends in Maine and Utah as part of our **DS 4002 - Data Science Project**. The project explores how environmental, lifestyle, and economic factors contribute to variations in NO₂ levels, utilizing **time series modeling in R** to analyze historical data and forecast future trends.

## Team Members
- **Mohini Gupta** (rde6mn) - Group Leader  
- **Neha Dacherla** (mcn4ws)  
- **Amani Akkoub** (ctf3un)  

## Course Details
- **Course**: DS 4002 - Data Science Project  
- **Date**: March 4, 2025  

## Hypothesis
The NO₂ concentration trends in **Utah** will showcase higher **seasonal variability** and a **slower decline rate** compared to **Maine** due to Utah’s temperature inversions and higher urbanization. Additionally, future NO₂ projections will illustrate a **greater influence from policy changes** (e.g., emissions regulations, electric vehicle adoption) in **Maine**, whereas in **Utah**, geographical factors will play a more dominant role in air quality trends.

## Research Question
**How do current and projected NO₂ concentration trends vary between Maine and Utah, and what environmental, lifestyle, and economic factors contribute to these differences?**

## Data Source and Preprocessing
- **Source**: U.S. Environmental Protection Agency (EPA)  
- **Sites**:  
  - Maine: **Site 230050029**  
  - Utah: **Site 490030005**  
- **Time Frame**: February 2024 - January 2025  

### Preprocessing Steps:
- Extracted relevant data fields: **Date and Daily Max 1-hour NO₂ Concentration**  
- Cleaned and formatted data for time series analysis  
- Standardized time range across both sites for accurate comparison  
- Created two datasets: **maine.csv** and **utah.csv**  

## Exploratory Data Analysis (EDA)
- **Visualized time series data** for both sites  
- **Compared NO₂ values**:  

| Metric  | Maine | Utah  |
|---------|-------|-------|
| Min Value | 1.4 | 2.2 |
| Max Value | 39.6 | 43.5 |
| Average | 19.0 | 14.9 |
| Median | 19.15 | 12.55 |

- Identified **Utah’s outliers**, indicating occasional extreme pollution events  
- Found **stable trends in Maine**, suggesting a more uniform NO₂ distribution  

## Model Approach
We use **R** to conduct time series analysis and forecasting due to its robust statistical modeling capabilities. The analysis was performed on the Windows platform. Our workflow includes:

1. **Visualizing Time Series Data**: Understanding trends, seasonal patterns, and fluctuations.  
2. **ACF and PACF Analysis**: Identifying autocorrelation and lag structures.  
3. **Forecasting Future Trends**: Using **ARIMA** and **Exponential Smoothing (ETS)** models to project NO₂ levels for six months.  

## Methodology
- **Data Splitting**: 80% training, 20% testing  
- **Algorithm Selection**:  
  - **ARIMA** (AutoRegressive Integrated Moving Average)  
  - **Exponential Smoothing State Space Model (ETS)**  
- **Cross-Validation**: Applied **rolling and expanding window techniques**  
- **Evaluation Metrics**:  
  - RMSE (Root Mean Square Error)  
  - MAE (Mean Absolute Error)  
  - AIC (Akaike Information Criterion)  
  - BIC (Bayesian Information Criterion)
  ## Reproduceability
   To reproduce the results of this analysis, first install the required R packages by running install.packages(c("forecast", "mtsdi", "MTS", "ggplot2", "lubridate", "tidyverse", "ggfortify", "ggpubr", "tseries")) in R. Then, load the datasets maine.csv and utah.csv from the data/ folder, and run the scripts exploratory_analysis.R and modeling.R in the notebooks/ folder to perform the time series analysis and forecasting.

## Required R Packages
Ensure the following R packages are installed before running the code:

```r
library(forecast)
library(mtsdi)
library(MTS)
library(ggplot2)
library(lubridate)
library(tidyverse)
library(ggfortify)
library(ggpubr)
library(tseries)

```

## Goal
To analyze current and future NO₂ trends in Maine and Utah, identifying significant differences and their potential environmental, economic, and policy-driven causes.

## Repo Structure
├── data/
│   ├── maine.csv
│   ├── utah.csv
├── notebooks/
│   ├── exploratory_analysis.R
│   ├── modeling.R
├── results/
│   ├── plots/
│   ├── forecasts/
|---data appendix
├── README.md

## Conclusion
Our analysis aims to provide insights into regional air quality trends and their broader implications. By comparing Maine and Utah, we hope to highlight the interplay between policy, geography, and lifestyle in shaping NO₂ levels.
For any questions or contributions, please reach out to the team!

Data Dinosaurs | DS 4002 - Data Science Project
