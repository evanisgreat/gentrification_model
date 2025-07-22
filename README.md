# Gentrification Model

# 🏙️ Neighborhood Gentrification Prediction

This project predicts **how soon a neighborhood is likely to undergo gentrification** using socioeconomic, housing, and demographic data. It aims to support urban planners, researchers, and communities in identifying early indicators of gentrification.

---

## 📌 Overview

**Gentrification** is often marked by rising home prices, demographic shifts, new business development, and changes in household income. This model estimates the **number of years until a neighborhood is likely to experience gentrification** based on historical trends and current data.

---

## 📊 Data Sources

- **U.S. Census / ACS** (demographics, housing, income)
- **Zillow / Redfin** (home value and rental trends)
- **City Planning & Permits** (new development signals)
- **Local crime and business activity**
- **Transit & infrastructure proximity (GIS)**

---

## 🧠 Methodology

### 🔧 Feature Engineering
- Median income and income growth
- Median rent and rent-to-income ratio
- Educational attainment
- New business count
- Public transit and amenity proximity

### 🎯 Target Variable
- **Regression:** Estimated years until gentrification
- **Classification (optional):** Binary flag for "likely gentrified within 5 years"

### 🤖 Models Used
- Random Forest Regressor
- XGBoost
- Logistic Regression (for classification variant)
- Time series analysis for trend modeling

---

## 🧪 Example Usage

```python
from model import predict_years_until_gentrification

features = {
    "zip_code": "78738",
    "median_income": 62000,
    "income_growth_5yr": 0.12,
    "median_rent": 1800,
    "college_educated_pct": 0.45,
    "new_businesses_past_3yr": 15,
    "transit_score": 0.8
}

years = predict_years_until_gentrification(features)
print(f"Estimated years until gentrification: {years}")
