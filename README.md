# 📈 Stock Price Prediction & Trend Classification

##  Project Overview
This project develops a machine learning system for predicting **stock price movements** using two approaches:
- **Regression** → Predict next-day percentage returns  
- **Classification** → Predict next-day trend direction *(Up/Down)*  

The implementation focuses on **Netflix (NFLX)** stock data.

---

##  Technology Stack
- **Data Collection**: `yfinance`, `pandas`  
- **Feature Engineering**: `numpy`  
- **Machine Learning**: `scikit-learn`  
  - Regression: Linear Regression, Ridge, Lasso, Decision Tree, KNN, SVM  
  - Classification: Logistic Regression, Decision Tree, KNN, SVM  
- **Visualization**: `matplotlib`, `seaborn`  
- **Analysis**: `statsmodels` (VIF analysis)  

---

##  Dataset
- **Source**: Yahoo Finance (via `yfinance`)  
- **Scope**: Daily OHLCV (Open, High, Low, Close, Volume) for Netflix  
- **Enhancements**: 20+ engineered technical indicators (returns, volatility, RSI, MACD, Bollinger Bands, etc.)  

---

##  Key Steps
1. **Data Collection**: Fetch historical stock data from Yahoo Finance  
2. **Feature Engineering**:  
   - Lagged features (Close_Lag1, Close_Lag2)  
   - Volatility, momentum, and trend indicators  
   - VIF analysis to remove multicollinear features  
3. **Preprocessing**: Missing value treatment, scaling, temporal split  
4. **Modeling**: Train/test regression & classification models with hyperparameter tuning  
5. **Evaluation**: RMSE, R² for regression; Accuracy, Precision, Recall, F1-score for classification  

---

##  Results & Insights
- **Regression**: Ridge Regression performed best (R² ≈ 0.0085), but results suggest very low predictability.  
- **Classification**:  
  - Decision Tree (tuned) achieved best recall (≈ 99%) but at cost of precision.  
  - SVM and Logistic Regression gave more balanced performance (~55% accuracy).  
- **Key Challenge**: Stock market prediction remains difficult due to noise, non-stationarity, and market efficiency.  

---

##  Lessons Learned
- Simple **linear models generalize better** than complex ones.  
- **Feature selection (RFE, VIF)** improved stability and reduced overfitting.  
- Hyperparameter tuning must be applied cautiously — risk of bias towards unrealistic recall.  
- Financial ML models need **domain-specific evaluation metrics** beyond standard accuracy.  

---
