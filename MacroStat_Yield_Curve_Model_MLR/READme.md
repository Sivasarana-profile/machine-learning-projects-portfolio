# Yield Curve Prediction from Macro Indicators

##  Project Overview
This project aims to **predict changes in government bond yields** using macroeconomic indicators such as:
- Inflation rate
- GDP growth rate
- Unemployment rate
- Central bank policy rate
- Industrial production

The approach is based on **Multiple Linear Regression (MLR)**, a foundational statistical technique in quantitative finance, widely used by fixed-income quants to model the relationship between macro variables and the term structure of interest rates.

---

##  Objectives
- Model the relationship between macroeconomic indicators and government bond yields.
- Predict shifts in the **yield curve** across short-, medium-, and long-term maturities.
- Evaluate model performance using out-of-sample testing.

---

##  Data Sources
The project uses publicly available macroeconomic and bond market datasets, such as:
- **FRED** (Federal Reserve Economic Data) – Inflation, GDP growth, unemployment rate, policy rate, Daily Treasury yield curve rates.
  
---

##  Methodology

1. **Data Collection**
   - Download macroeconomic time series and yield data from FRED.
   - Align data to a common frequency (monthly or quarterly).

2. **Data Preprocessing**
   - Handle missing values and perform necessary transformations (log returns, % changes).
   - Normalize/standardize features for better regression stability.

3. **Feature Engineering**
   - Short-term yield (e.g., 2-year), medium-term yield (e.g., 5-year), long-term yield (e.g., 10-year).
   - Macro indicators: inflation, GDP growth, unemployment, policy rate changes, industrial production growth.

4. **Model Building**
   - Train **Multiple Linear Regression (MLR)** models separately for different maturities.
   - Estimate coefficients and interpret factor sensitivities.

5. **Model Evaluation**
   - In-sample fit: R², adjusted R², p-values of coefficients.
   - Out-of-sample accuracy: RMSE, MAE, MAPE.

6. **Visualization**
   - Plot historical vs. predicted yields.
   - Visualize factor coefficients across maturities.
