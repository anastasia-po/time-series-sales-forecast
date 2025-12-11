# Sales Forecasting for a High-Performing Product Using Time Series Analysis

## Project Overview
The goal of this project is to conduct an exploratory data analysis (EDA) on a dataset containing 
weekly sales of health supplements, identify the top-selling product with highest revenue, and 
forecast its future sales using Time Series modeling technique (SARIMA).

---

## Key Findings
- **Biotin** identified as the top-selling product with the highest revenue
- Detected **clear yearly seasonality** of Biotin sales
- Selected final model: **SARIMA (1,0,1)(1,1,1,52)**
- Achieved **MAPE = 6.84%**
- Built a **52-week sales forecast**
---

## Tools & Methods
- Python  
  - pandas  
  - numpy  
  - matplotlib  
  - statsmodels
  - sklearn (evaluation metrics)

- Exploratory Data Analysis (EDA)
- Time Series Analysis (SARIMA)
- Stationarity testing (ADF), Autocorrelation analysis (ACF / PACF)
- Model Evaluation (MAE, RMSE, MAPE, AIC/BIC criteria)

---

## Dataset Description
- Weekly sales data from **January 1, 2020, to March 31, 2025**
- 4,384 rows, 10 columns
- 16 health supplement products
- 10 products categories

---
## Analysis

### 1. Exploratory Data Analysis (EDA)
- Analyzed weekly, monthly, and yearly revenue
- Compared revenue by product categories
- Identified **Biotin** as the top-selling product with highest revenue

### 2. Time Series Analysis of Biotin

#### Time Series Decomposition
- Aggregated weekly data into monthly data
- Identified:
  - Stable trend
  - Clear yearly seasonality
  - Repeating demand cycles

#### Model Selection
- Tested ARIMA vs SARIMA
- Selected **SARIMA** due to strong seasonality
- Used:
  - ADF test for stationarity
  - ACF and PACF for parameter selection

Final model: order = (1, 0, 1), seasonal_order = (1, 1, 1, 52)

#### Model Evaluation
Train/Test split:
- 214 weeks — train
- 60 weeks — test

Metrics:
- **MAE = 10.12**
- **RMSE = 13.40**
- **MAPE = 6.84%**
- **AIC = 1361**
- **BIC = 1377**


#### Forecast
- Generated a **52-week sales forecast** beyond March 31, 2025
- Visualized:
  - Historical sales
  - Forecast values
  - 95% confidence interval
---

## Business Value
The forecast can be used for:
- Inventory planning  
- Marketing strategy  
- Supply chain optimization  
- Seasonal demand management

---
## Future Improvements
Future work may involve further model optimization to reduce error metrics and improve forecast accuracy. Additionally, analyzing the causes of extreme weekly sales spikes and dips — such as promotions, stockouts, or special events — would enhance understanding of demand volatility and lead to more robust forecasting.
