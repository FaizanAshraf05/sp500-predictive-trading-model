# AI Predictive Trading Model: SPY Backtest Pipeline

## 📌 Project Overview
This project is an end-to-end machine learning pipeline designed to predict the daily price direction of the S&P 500 ETF (SPY). By engineering technical market indicators and utilizing a Random Forest Classifier, the model analyzes historical data to generate algorithmic "Buy" signals.

This repository demonstrates practical proficiency in financial data extraction, time-series feature engineering, and predictive modeling for algorithmic trading.

## 🚀 Key Performance Metric
* **Model Precision:** **58.70%**
* *Context:* In quantitative finance, accurately predicting daily market direction above a 50/50 baseline is highly challenging. A 58.70% precision score indicates that when the model generates a "Buy" signal, it is correct significantly more often than it is wrong, establishing a strong foundation for a profitable trading algorithm.

## 🛠️ Tech Stack & Libraries
* **Python** (Core Logic)
* **yfinance** (Live/Historical Data API Extraction)
* **Pandas** (Data Manipulation & Pipeline Structuring)
* **Scikit-Learn** (Machine Learning & Predictive Modeling)
* **Matplotlib** (Data Visualization)

## 📊 Methodology & Pipeline
1. **Data Extraction:** Automated fetching of 5 years of daily historical data for SPY.
2. **Feature Engineering:** Calculated key technical indicators to provide the model with market context:
   * 50-day Simple Moving Average (SMA)
   * 200-day Simple Moving Average (SMA)
   * Daily Percentage Returns
3. **Target Definition:** Binary classification (`1` for upward movement, `0` for downward movement).
4. **Model Training:** Utilized a `RandomForestClassifier`. Crucially, the data was split chronologically (training on the first ~4.5 years, testing on the most recent 100 days) to completely prevent data leakage and simulate real-world trading conditions.

## 📈 Visual Strategy
The Jupyter Notebook included in this repository contains the full visual breakdown of the strategy, overlaying the AI's predicted "Buy" signals on top of actual historical price movements for visual verification of the model's accuracy.

---
*Developed for portfolio demonstration of algorithmic trading architecture and data science capabilities.*
