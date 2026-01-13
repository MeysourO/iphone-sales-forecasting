# iPhone 17 Sales Forecasting

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)

> Predicting iPhone 17 sales using Linear Regression on historical iPhone 12-16 data

---

## 📌 About This Project

This project forecasts the first 4 months of **iPhone 17 sales** (October 2025 - January 2026) using historical sales data from previous iPhone releases.

Completed as part of **Session 3: Forecasting** coursework.

---

## 🤔 Why Python?

I chose Python for this project because:

- ✅ Prior experience using Python at my job
- ✅ Completed a Python bootcamp
- ✅ `pandas` makes data manipulation easy
- ✅ `scikit-learn` has simple regression tools
- ✅ `matplotlib` for quick visualizations

---

## 📊 The Data

| Column | Description |
|--------|-------------|
| `Date` | Date of sales |
| `Model` | iPhone model (12, 13, 14, 15, 16) |
| `Month` | Day number since release |
| `Estimated_Units_Millions` | Daily sales in millions |

**Data covers:** iPhone 12 through iPhone 16 (Oct 2020 - 2025)

---

## 🔧 Methodology

### Step 1: Data Prep
- Aggregated daily sales → monthly totals
- Month 1 = Days 1-30, Month 2 = Days 31-60, etc.

### Step 2: Feature Engineering
```
iPhone 12 → Generation 0
iPhone 13 → Generation 1
iPhone 14 → Generation 2
iPhone 15 → Generation 3
iPhone 16 → Generation 4
iPhone 17 → Generation 5 (forecast target)
```

### Step 3: Model
- **Type:** Linear Regression
- **Features:** Generation (trend) + Month (seasonality)
- **Train:** iPhone 12-15
- **Test:** iPhone 16
- **Forecast:** iPhone 17

---

## 📈 Results

### Model Equation

```
Sales = 18.40 + (-1.29 × Generation) + (0.83 × Month)
```

| Coefficient | Value | Meaning |
|-------------|-------|---------|
| Intercept | 18.40 | Base sales |
| Generation | -1.29 | Sales drop ~1.3M per new iPhone |
| Month | 0.83 | Sales rise ~0.8M each month |

---

### iPhone 16 Validation

| Month | Predicted | Actual | Error |
|-------|-----------|--------|-------|
| 1 | 14.05M | 13.83M | +1.6% |
| 2 | 14.88M | 14.03M | +6.1% |
| 3 | 15.71M | 15.47M | +1.6% |
| 4 | 16.55M | 17.73M | -6.7% |

**MAE:** 0.63 million units  
**MAPE:** 4.0%

---

### 🔮 iPhone 17 Forecast

| Month | Period | Forecast |
|-------|--------|----------|
| 1 | Oct 2025 | **12.76M** |
| 2 | Nov 2025 | **13.59M** |
| 3 | Dec 2025 | **14.42M** |
| 4 | Jan 2026 | **15.25M** |
| **TOTAL** | | **56.02M** |

---

## 💡 Key Takeaways

1. **📉 Declining Trend** — Each new iPhone sells less than the previous generation
2. **📅 Seasonality** — Sales increase in months 2-3 (holiday season)
3. **⚠️ iPhone 12 Outlier** — Unusually high sales (pandemic + 5G launch)
4. **✅ Model Accuracy** — 4% MAPE on validation = solid performance

---

## 🤖 AI Disclosure

Used **Claude (Anthropic)** for:
- Code structure and debugging
- Understanding forecasting methods
- Creating documentation

Analysis and interpretation done by me.

---

## 📚 References

- [scikit-learn docs](https://scikit-learn.org/)
- [pandas docs](https://pandas.pydata.org/)
- Course Session 3: Forecasting Methods

---

## 👤 Author

**Omezzine Meysour**

---

⭐ **If this helped you, give it a star!**
