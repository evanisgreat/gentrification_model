# 🏙️ Zipcode Gentrification Prediction

This project predicts **how soon a zipcode is likely to undergo gentrification** using socioeconomic, housing, and demographic data. It aims to support urban planners, researchers, and communities in identifying early indicators of gentrification.

---

## 📌 Overview

**Gentrification** is often marked by rising home prices, demographic shifts, new business development, and changes in household income. This model estimates the **probability of a neighborhood to be gentrified in a given year** based on historical trends and current data.

---

## 📊 Data Sources

- **U.S. Census / ACS** (demographics, housing, income)

---

## 🧠 Methodology

### 🔧 Feature Engineering
- Median income and income growth
- Median rent and rent growth
- Educational attainment

### 🎯 Target Variable
- **Regression:** Estimated years until gentrification
- **Classification:** Binary flag for already gentrified

### 🤖 Models Used
- Logistic Regression
- Random Forest
- Stacked Model

### Procedure
- First create a classification model to determine if zipcodes are gentrified in any given year
- Replicated the Urban Displacement Project Gentrification methodology
- We then fitted it with different forecasting models
---

## 🧪 Example Usage

```python
from model import probability_gentrified

features = {
    "zip_code": "78738",
    "median_income": 62000,
    "median_rent": 1800,
    "college_educated_pct": 0.45,
}

prob = probability_gentrified(features)
print(f"Estimated gentrification probability {prob}")
