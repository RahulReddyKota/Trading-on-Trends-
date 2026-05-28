# 📈 Trading on Trends — Advanced Stock Sentiment Analysis System

> An intelligent, end-to-end system that combines **social media sentiment**, **financial market data**, and **technical analysis** to predict stock price movements.

Built with Python, Flask, and advanced machine learning models, this project enables real-time analysis, predictive modeling, and interactive visualizations.

---

## 🚀 Key Features

### 🔌 API Integrations

| Source | Description | Method |
|--------|-------------|--------|
| **Reddit API (PRAW)** | Collects sentiment data from financial subreddits | `fetch_reddit_data()` |
| **Yahoo Finance (yfinance)** | Fetches OHLCV data and historical stock prices | `fetch_stock_data()` |
| **Flask API** | Provides web endpoints for real-time analysis | `Route: /analyze` |

---

### 🧹 Data Preprocessing & Transformation

- **Text Cleaning** — Removes URLs, special characters, and normalizes whitespace via `clean_text()`
- **Data Merging** — Aligns stock and sentiment data by date via `merge_stock_and_sentiment()`
- **Missing Value Handling** — Forward/backward fill for stock data; zero-fill for sentiment fields

---

### ⚙️ Feature Engineering

Technical indicators and enriched features added via `add_technical_indicators()`:

- RSI, MACD, Bollinger Bands
- Lag features and rolling means
- Interaction terms between sentiment and price signals

---

### 🤖 Machine Learning Models

#### Classification — Stock Price Direction (Up / Down)

| Model | Notes |
|-------|-------|
| Logistic Regression | L2 Regularization |
| Random Forest Classifier | Ensemble-based |
| XGBoost Classifier | Gradient boosting |

**Methods:** `train_models()`, `_evaluate_logistic_model()`

**Metrics:** Accuracy · Precision · Recall · F1-Score · AUC-ROC · Confusion Matrix

#### Regression — Stock Return %

| Model | Notes |
|-------|-------|
| Ridge Regression | L2-regularized linear model |
| Gradient Boosting Regressor | Sequential ensemble |
| XGBoost Regressor | High-performance gradient boosting |

**Methods:** `train_models()`, `_evaluate_linear_model()`

**Metrics:** RMSE · MAE · R² Score · Directional Accuracy

---

### 🌐 Interactive Web Application

- Built with **Flask** for API interaction
- Real-time visualizations powered by **Plotly**
- Dashboard includes: price charts, volume, sentiment scores, and technical indicators

---

### 💬 Enhanced Sentiment Analysis

- Custom financial lexicon layered on top of **VADER**
- Aggregates signals from multiple financial subreddits
- Time-aware features: sentiment momentum, rolling sentiment averages

---

### 🏋️ Training Pipeline Optimization

- **Feature selection** via Random Forest feature importance
- **Time-series cross-validation** for temporal modeling integrity
- **SMOTE** for handling class imbalance
- Automatic multi-model comparison and selection

---

### 🛡️ Robust Error Handling

- Graceful handling of missing and infinite values
- API error fallbacks during data collection
- Input validation for safe plotting and analysis

---

### 📊 Performance Monitoring

- Model metrics stored in JSON for reproducibility
- Visual comparison of feature importance across models
- Backtesting module for historical strategy validation

---

## 📁 Project Structure

```
stock_sentiment_analysis/
├── data/
│   ├── raw/              # Original API data
│   ├── processed/        # Cleaned and merged datasets
│   └── final/            # Analysis-ready data
├── models/               # Trained model artifacts
├── visualizations/       # Generated charts and plots
├── app.py                # Flask web application
├── StockSentimentAnalyzer.py  # Main analysis class
└── requirements.txt      # Python dependencies
```

---

## 🔮 Future Enhancements

- [ ] Real-time streaming from Reddit and stock tickers
- [ ] Deep learning models (LSTM, Transformer-based architectures)
- [ ] Multi-asset portfolio analysis
- [ ] Risk management strategies and position sizing
- [ ] Cloud deployment (AWS / GCP / Azure)
- [ ] Responsive web front-end with mobile support

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Reddit](https://img.shields.io/badge/Reddit%20API-FF4500?style=flat&logo=reddit&logoColor=white)
![Yahoo Finance](https://img.shields.io/badge/Yahoo%20Finance-6001D2?style=flat&logoColor=white)
