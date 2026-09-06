# 🏠 House Price Prediction — Supervised Learning

> End-to-end regression pipeline predicting residential house prices using the Ames Housing Dataset.  
> Built as part of the Supervised Learning Practical Exam at Red & White Skill Education, Surat.

---

## 📌 Project Overview

Imagine you are a Junior Data Scientist at a PropTech startup like NoBroker or MagicBricks.  
The product team needs an automated house price estimator to help buyers and sellers benchmark property values.  
That is exactly what this project builds — a complete ML pipeline from raw data to a deployable prediction model.

---

## 📁 Dataset

| Detail | Info |
|---|---|
| Source | [Kaggle — House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data) |
| Rows | 1,460 training records |
| Features | 79 (numerical + categorical) |
| Target | SalePrice (continuous, USD) |

---

## 🔧 What I Did

- ✅ Exploratory Data Analysis — distributions, correlations, outlier detection
- ✅ Missing value treatment — 3 strategies based on feature type
- ✅ Feature Engineering — TotalSF, HouseAge, RemodAge, HasGarage, HasPool
- ✅ Encoding — Ordinal, One-Hot, Label Encoding
- ✅ Log transformation on skewed features and target
- ✅ Trained 5 regression models and compared performance
- ✅ Residual analysis and business interpretation
- ✅ Saved final pipeline using joblib

---

## 📊 Model Comparison

| Model | RMSE (USD) | MAE (USD) | R² Score |
|---|---|---|---|
| Linear Regression | 23,425 | 16,070 | 0.9007 |
| Ridge Regression | 22,299 | 15,694 | 0.9100 |
| Lasso Regression | 21,125 | 15,454 | 0.9192 |
| Random Forest | 23,205 | 16,369 | 0.9025 |
| **XGBoost** ⭐ | **19,672** | **14,134** | **0.9299** |

---

## 🏆 Best Model — XGBoost Regressor

XGBoost achieved the lowest RMSE of $19,672 and R² of 0.9299.  
It outperforms linear models by capturing non-linear relationships between features.  
Boosting iteratively corrects errors — making it more precise than Random Forest.  
For a PropTech startup, this means predictions are within ~₹16 lakh of actual price on average.

---

## 🔑 Top 5 Predictive Features

1. **OverallQual** — Build quality is the single strongest signal for price
2. **TotalSF** — Total usable area across all floors drives value
3. **GrLivArea** — Above-ground living space commands a premium
4. **HouseAge** — Newer homes consistently price higher
5. **Neighborhood** — Location matters even after controlling for size and quality

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/ranu77/SupervisedLearning_EXAM

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download train.csv from Kaggle and place it in the project folder

# 4. Open and run the notebook
jupyter notebook exam.ipynb
```

---

## 📂 Repository Structure

SupervisedLearning_EXAM/
│
├── exam.ipynb # Main notebook (fully executed)
├── house_price_model.pkl # Saved sklearn pipeline
├── summary_report.md # Project summary
├── requirements.txt # Dependencies
├── Practical Exam _ Set A.pdf # Exam question paper
└── README.md # You are here


---

## 🎥 Video Walkthrough

📹 [Click here to watch the project explanation video](https://drive.google.com/file/d/13JbzZHufkvOtZiqEvr_kAlGg5qQJi6ka/view?usp=sharing)

---

## 👩‍💻 Author

**Devanshi Kanthariya**  
