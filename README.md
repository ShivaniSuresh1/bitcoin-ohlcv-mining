# Bitcoin OHLCV Data Mining & Forecasting

## Project Overview
This project analyzes high-frequency Bitcoin price and volume data to uncover temporal patterns, volatility clusters, and potential anomalies. The ultimate goal is to prepare the dataset for predictive modeling using both course and beyond-course techniques.

**Scope:**
- Exploratory Data Analysis (EDA)
- Feature Engineering: log returns, rolling volatility
- Anomaly detection
- Future work: LSTM/Transformer-based forecasting

---

## Dataset
- **Source:** [Kaggle – Bitcoin Historical Data](https://www.kaggle.com/datasets/swaptr/bitcoin-historical-data)  
- **Size:** ~7.4 million rows (1-minute intervals)  
- **Columns:** `Timestamp, Open, High, Low, Close, Volume`  
- **Licensing:** Public dataset for academic use  
- **Notes:** No missing values; highly skewed price and volume distributions

---

## Progress / Current Work

### Exploratory Data Analysis
1. **Data Inspection**
   - Verified dataset size and data types
   - Confirmed no missing values
2. **Timestamp Conversion**
   - Converted Unix seconds - for proper time-series handling
3. **Visualizations**
   - Closing price over time - shows trends and regime shifts
   - Log return distribution - identifies heavy tails and extreme returns
   - Volume distribution (log scale) - highlights skewness and spikes
   - Rolling 1-hour volatility - captures volatility clustering
4. **Feature Engineering**
   - **Log returns:** `log(Close / Open)` stabilizes variance
   - **Rolling volatility:** 1-hour rolling std captures market risk

### Key Insights
- Most price changes are small in 1-minute intervals; rare extreme outliers exist  
- Volume spikes coincide with large price moves → potential anomaly signals  
- High-frequency noise suggests smoothing / rolling-window features for modeling  

### Planned Next Steps
- Implement LSTM/Transformer models for short-term forecasting  
- Apply anomaly detection on log returns and volume spikes  
- Evaluate impact of rolling window size on volatility and prediction  
- Explore technical indicators (RSI, MACD) for improved forecasting

## Collaboration Declaration

On my honor, I declare the following resources:

1. **Collaborators:**
- None

2. **Web Sources:**
- https://pandas.pydata.org/docs/  
- https://numpy.org/doc/  
- https://matplotlib.org/stable/  
- https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data  

3. **AI Tools:**
- ChatGPT – Used for structural refinement, documentation formatting, and domain-specific information.

4. **Citations (Papers Referenced Conceptually):**
- Mandelbrot, B. (1963). *The Variation of Certain Speculative Prices.* Journal of Business.  
  *Justifies the observation that log returns exhibit heavy tails and deviate from Gaussian assumptions due to frequent extreme price movements.*

- Engle, R. (1982). *Autoregressive Conditional Heteroskedasticity with Estimates of the Variance of UK Inflation.* Econometrica.  
  *Supports the identification of volatility clustering and time-varying variance in financial return series.*

- Bollerslev, T. (1986). *Generalized Autoregressive Conditional Heteroskedasticity.* Journal of Econometrics.  
  *Motivates the use of rolling volatility and GARCH-type models to capture persistent conditional heteroskedasticity in returns.*


