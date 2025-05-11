# hospital-revenue-time-series-analysis
ARIMA time series modeling and forecasting of hospital revenue data with detailed pattern analysis, stationarity testing, and model validation

## Project Overview
This project implements an Autoregressive Integrated Moving Average (ARIMA) model to analyze and forecast hospital revenue patterns. Using a 2-year daily revenue dataset, the analysis explores time series characteristics, identifies optimal ARIMA parameters, and generates short-term revenue forecasts.

## Research Question
What patterns exist in hospital revenue, and how accurately can an ARIMA model forecast future revenue?

## Methodology
The analysis follows a comprehensive time series modeling approach:

1. **Data Preparation**: 
   - Performed completeness checks ensuring sequential, complete time steps
   - Applied time step formatting and datetime indexing
   - Created an 80/20 train-test split for model validation

2. **Stationarity Analysis**:
   - Visualized rolling mean and standard deviation
   - Conducted Augmented Dickey-Fuller (ADF) tests
   - Applied differencing to achieve stationarity

3. **Pattern Exploration**:
   - Generated autocorrelation (ACF) and partial autocorrelation (PACF) plots
   - Performed spectral density analysis
   - Completed time series decomposition to identify trend, seasonal, and residual components

4. **Model Selection**:
   - Evaluated multiple ARIMA configurations (p,d,q)
   - Compared models using AIC/BIC criteria and coefficient significance
   - Selected optimal ARIMA(1,1,0) model

5. **Model Validation**:
   - Analyzed model residuals for randomness and stationarity
   - Calculated Root Mean Squared Error (RMSE)
   - Estimated prediction intervals with 95% confidence

## Key Findings
- The revenue data follows a random walk with drift, exhibiting an upward trend that plateaus
- No significant seasonality detected, with evidence from ACF/PACF plots and spectral analysis
- ARIMA(1,1,0) provides reliable forecasts with an RMSE of approximately 3.6
- Model performance is strong for short-term forecasts (within 147 days) but less reliable for long-term projections
- The model captures the underlying revenue structure, with residuals resembling white noise

## Tools & Technologies
- Python
- Pandas for data manipulation
- Statsmodels for time series modeling
- Matplotlib and Seaborn for visualization
- SciPy for spectral analysis

## Future Work
- Explore more flexible models to capture the natural oscillations in revenue
- Destandardize data for improved interpretability of error metrics

*This project was completed as part of a Data Analytics course (D213).*
