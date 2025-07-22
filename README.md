# 📈 Predictive Analytics for the Federal Funds Rate

## 📘 Overview

This project explores the use of predictive analytics to forecast the U.S. federal funds rate by combining traditional macroeconomic data with sentiment analysis derived from Reddit discussions. The aim is to assess whether public sentiment improves the predictive power of regression models on interest rate movements.

---

## 🎯 Objective

To determine whether incorporating social media sentiment (from Reddit) alongside macroeconomic variables can improve the short-term prediction of the federal funds rate.

---

## 📦 Data Sources

- **Federal Funds Rate** – Federal Reserve Bank of St. Louis (FRED)
- **Macroeconomic Indicators**:
  - 3-Month Treasury Bond Yield
  - CPI (Consumer Price Index)
  - Inflation and Inflation Expectations
  - Net Capital Outflows
  - Investor Sentiment (Bull-Bear Spread)
  - Unemployment Rate
  - Personal Consumption Expenditures (PCE)
  - Gross Domestic Product (GDP)
- **Reddit Sentiment**:
  - Data from r/wallstreetbets (2012–2021)
  - Sentiment scoring via VADER

---

## 🧹 Data Preprocessing

- Time normalization across datasets to monthly frequency
- Imputation of missing values and percent-change transformation
- Dimensionality reduction via Pearson correlation thresholding
- Sentiment scoring of Reddit posts and monthly aggregation

---

## 📈 Modeling

- Two multivariate regression models:
  1. Baseline: Macroeconomic features only
  2. Enhanced: Macroeconomic features + Reddit sentiment
- Evaluation Metrics: R-squared, F-statistic, RMSE, p-values

---

## 🔍 Key Results

| Model               | RMSE   | R²     | F-stat | Sentiment p-value |
|--------------------|--------|--------|--------|-------------------|
| Baseline           | 0.777  | 0.019  | 0.333  | —                 |
| With Sentiment     | 0.643  | 0.329  | 7.219  | < 0.001           |

- Sentiment improves accuracy and statistical significance
- Sentiment coefficient: -6.23 (high explanatory value)

---

## 🛠️ Tools & Libraries

- Python (Pandas, NumPy)
- Scikit-learn
- VADER (for sentiment analysis)
- Jupyter Notebooks

---

## ✅ Conclusion

Reddit sentiment is a strong and statistically significant predictor when added to macroeconomic models of the federal funds rate. This hybrid approach can be used to enhance predictive models in economic forecasting.

---