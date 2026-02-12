# Bitcoin OHLCV – Exploratory Data Analysis

## Overview

This project performs Exploratory Data Analysis (EDA) on 1-minute BTC/USD OHLCV data to understand structural characteristics, distributional properties, and volatility behavior prior to predictive modeling.

The analysis focuses on statistical validation and financial reasoning behind each transformation.

---

## Dataset

- Source: Kaggle – Bitcoin Historical Data (https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data)
- Frequency: 1-minute intervals  
- Features: Timestamp, Open, High, Low, Close, Volume  

---

## Objectives

- Validate data integrity
- Analyze long-term price trends
- Transform prices into log returns
- Examine return distribution properties
- Analyze volume skewness
- Estimate rolling volatility
- Identify volatility clustering behavior

---

## Key Analysis Steps

1. Data cleaning and validation  
2. Timestamp conversion to datetime  
3. Price trend visualization  
4. Log return computation  
5. Distribution analysis (heavy tails)  
6. Volume distribution analysis (log-scale)  
7. 60-minute rolling volatility estimation  

Each algorithmic decision is explicitly justified in the notebook.

---

## Key Findings

- BTC price series is non-stationary.
- Log returns exhibit heavy tails.
- Volume distribution is highly skewed.
- Clear evidence of volatility clustering.
- Gaussian assumptions are inappropriate.

---

## Tools Used

- pandas
- numpy
- matplotlib

---

## References

- Mandelbrot (1963) – Heavy-tailed financial returns  
- Engle (1982) – ARCH model  
- Bollerslev (1986) – GARCH model  

---

## Author

Shivani S.
