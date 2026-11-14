# Time Series Forecasting of Mercedes-Benz Stock Prices

R project comparing ARIMA, ETS and Prophet models to forecast the daily closing price of Mercedes-Benz Group AG (MBG.DE).

## About

- **Goal:** find the best model to forecast stock prices
- **Data:** `Mercedes_Stock.csv`, 7,511 daily observations from Oct 1996 to Feb 2026
- **Variable used:** closing price
- **Course:** ITM508, Applied Time Series for Forecasting Analysis with R (Mediterranean School of Business, Pr. Hedi Essid)

## What We Did

- Explored the data (high volatility, no clear trend or seasonality)
- Tested stationarity with the ADF test (non-stationary)
- Applied a log transformation and first differencing (stationary)
- Split the data chronologically: 70% train, 15% validation, 15% test
- Fitted 3 models:
  - ARIMA(2,1,5)
  - ETS(A,N,N)
  - Prophet
- Compared models with AIC/BIC, RMSE and MAPE
- Checked residual diagnostics

## Results

- **Validation set:** ETS slightly best, ARIMA almost identical, Prophet weakest
- **Test set:** ARIMA is the best model
- ARIMA also has the lowest AIC and BIC
- Prophet performs poorly because stock prices have no strong seasonality

## Files

- `Time_Series_Forecasting_of_Mercedes-Benz_Stock_Prices.Rmd`: R Markdown code and analysis
- `Mercedes_Stock.csv`: dataset (semicolon-separated)
- `Time_Series_Forecasting_of_Mercedes-Benz_Stock_Prices_Report.pdf`: full report
- `Time_Series_Forecasting_of_Mercedes-Benz_Stock_Prices_Presentation.pdf`: presentation
