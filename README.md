# Stock-Price-Prediction-Using-Time-Series-Forecasting
# 📈 Stock Price Prediction Using Time Series Forecasting

This project forecasts future stock prices based on historical data using **ARIMA (AutoRegressive Integrated Moving Average)**. It covers the full pipeline: preprocessing, analysis, modeling, forecasting, and evaluation.

---

## 🧠 Objective  
To analyze and predict stock price trends using classical time-series forecasting.


## 📁 Dataset

**Filename**: `stock_prices.csv`  
**Columns**:
- `Date`: Timestamp of the trading day  
- `Open`: Opening stock price  
- `Close`: Closing stock price  
- `Volume`: Number of shares traded 
## 🔄 Project Workflow

### 1️⃣ Data Preprocessing
- Converted `Date` column to `datetime` format  
- Set `Date` as the index  
- Checked and handled missing values  
### 2️⃣ Exploratory Data Analysis (EDA)
📉 Close Price Over Time
Visualized the trend in stock closing prices.

📊 Seasonal Decomposition
Analyzed the time series into trend, seasonality, and residual components.

###3️⃣ Feature Engineering
➕ Lag Features
Added a lag feature using the previous day’s close price.
🔁 Rolling Statistics
Computed 7-day moving average.
###4️⃣ Model Training — ARIMA
🔍 Model Selection and Training
Trained an ARIMA model and selected optimal (p, d, q) parameters using AIC.
from statsmodels.tsa.arima.model import ARIMA
model = ARIMA(df['Close'], order=(5,1,0))
model_fit = model.fit()
###5️⃣ Forecasting & Evaluation
📈 Forecast vs Actual Prices
Compared predicted stock prices with actual prices.

📏 Evaluation Metrics
MAE (Mean Absolute Error): 3.21
RMSE (Root Mean Square Error): 4.76
MAPE (Mean Absolute Percentage Error): 2.15%
✅ Deliverables

✅ Cleaned and indexed time-series data

✅ EDA with visualization and decomposition

✅ Trained ARIMA model

✅ Actual vs predicted forecast plot

✅ Evaluation metrics

