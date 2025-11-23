
# S&P 500 Factor Attribution Analysis

> **A comprehensive multi-factor regression model with walk-forward validation for attributing S&P 500 returns to macroeconomic and market factors.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results & Outputs](#results--outputs)
- [Visualizations](#visualizations)
- [Model Comparison](#model-comparison)

---

## 🎯 Overview

This project implements a **sophisticated factor attribution framework** to decompose S&P 500 returns into contributions from various market and macroeconomic factors. By employing multiple regression techniques and rigorous backtesting, we identify which factors drive index performance and quantify their impact over time.

### **Business Problem**

- Which factors drive S&P 500 returns?
- How much does each factor contribute to overall performance?
- Which model provides the most accurate predictions?
- Are factor relationships stable over time?

### **Solution**

A comprehensive analytical pipeline that:
1. Collects and preprocesses multi-frequency financial data
2. Builds and compares 9 different regression models
3. Performs walk-forward validation for robust out-of-sample testing
4. Generates professional visualizations and machine-readable outputs

---

## ✨ Key Features

### **Data Engineering**
- ✅ Automated data collection from Yahoo Finance & FRED
- ✅ Multi-frequency alignment (daily → monthly)
- ✅ Proper time-series handling (lagging, no look-ahead bias)
- ✅ Clean ETL pipeline with error handling

### **Statistical Modeling**
- ✅ **9 Models Tested**: OLS, Ridge, Lasso, ElasticNet, Huber, Bayesian Ridge, Random Forest, Gradient Boosting, SVR
- ✅ Hyperparameter optimization via cross-validation
- ✅ Factor attribution with coefficient interpretation
- ✅ Walk-forward validation (60-month train, 12-month test)

### **Visualizations**
- ✅ Time-series factor contributions
- ✅ Cumulative attribution analysis
- ✅ Yearly heatmaps
- ✅ Rolling correlations
- ✅ Waterfall charts
- ✅ Model comparison dashboards

---

## 🚀 Installation

### **Prerequisites**

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Internet connection (for data download)

### **Setup**

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn
pip install statsmodels scikit-learn scipy
pip install yfinance pandas-datareader
pip install jupyter
```

---

## 📊 Usage

1. **Launch Jupyter Notebook**
```bash
jupyter notebook "Untitled43 (1).ipynb"
```

2. **Run all cells sequentially** (Cell → Run All)
3. **View results** in generated PNG files and `model_results.json`

---

## 🔬 Methodology

### **Data Collection**

**Market Factors (Daily):**
- S&P 500 Index, VIX, Oil, Gold, Tech Sector, Financial Sector

**Macroeconomic Factors (Monthly):**
- CPI (Inflation), Federal Funds Rate

### **Factor Attribution Formula**

```
S&P 500 Return = β₁×VIX + β₂×Oil + β₃×Gold + β₄×Tech 
                 + β₅×Financial + β₆×CPI(t-1) + β₇×FedRate(t-1)
                 + Intercept + Residual
```

### **Walk-Forward Validation**

```
|---60 months TRAIN---|---12 months TEST---|
                      |---60 months TRAIN---|---12 months TEST---|
```

---

## 📈 Results & Outputs

### **Generated Files**
- `model_results.json` - Complete model metrics
- `comprehensive_model_comparison.png` - Model rankings
- `feature_importance_comparison.png` - Factor importance
- `factor_contributions_over_time.png` - Time series
- `cumulative_factor_contributions.png` - Long-term view
- `yearly_factor_contributions.png` - Annual heatmap
- `rolling_factor_correlations.png` - Correlation analysis
- `waterfall_recent_attribution.png` - Recent performance

---

## 🛠️ Models Implemented

| Model | Type | Key Feature |
|-------|------|-------------|
| **OLS** | Linear | Baseline, interpretable |
| **Ridge** | Regularized | L2 penalty |
| **Lasso** | Regularized | Feature selection |
| **ElasticNet** | Regularized | L1 + L2 |
| **Huber** | Robust | Outlier resistant |
| **Bayesian Ridge** | Probabilistic | Uncertainty |
| **Random Forest** | Ensemble | Non-linear |
| **Gradient Boosting** | Ensemble | Sequential |
| **SVR** | Kernel | Non-linear patterns |

---

## 💼 Business Applications

- **Portfolio Management**: Identify factor exposures and hedge risks
- **Risk Management**: Quantify macro sensitivities
- **Trading Strategy**: Factor timing signals
- **Research & Reporting**: Performance attribution

---

## 🎓 Skills Demonstrated

- Data Engineering (ETL, multi-source integration)
- Statistical Modeling (OLS, regularization, ensembles)
- Time Series Analysis (proper validation)
- Machine Learning (hyperparameter tuning)
- Visualization (professional charts)
- Software Engineering (clean, reproducible code)

---

## 🔮 Future Enhancements

- [ ] Add sentiment analysis factors
- [ ] Implement regime detection
- [ ] Real-time data pipeline
- [ ] Interactive dashboard
- [ ] Multi-index support

---

## 📚 References

1. Fama-French Factor Models
2. Statistical Learning - Hastie, Tibshirani, Friedman
3. Factor Investing - Andrew Ang

---

<div align="center">

**⭐ Built for quantitative finance analysis**

Made with ❤️ using Python, Jupyter, and scikit-learn

</div>
