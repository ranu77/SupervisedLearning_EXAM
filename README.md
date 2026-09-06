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


<img width="605" height="432" alt="image" src="https://github.com/user-attachments/assets/2558f6ac-1dd7-4573-ad5a-b265fe2451ca" />

<img width="646" height="643" alt="image" src="https://github.com/user-attachments/assets/907b861b-1d02-44b8-b8d8-9b24db9057f7" />

<img width="1166" height="319" alt="image" src="https://github.com/user-attachments/assets/8c4c129b-d42b-4161-b290-1283ce1b0f37" />

<img width="714" height="511" alt="image" src="https://github.com/user-attachments/assets/ae72c128-fed3-477a-8aad-e7f788862458" />

<img width="1164" height="320" alt="image" src="https://github.com/user-attachments/assets/dea11c3b-c0c8-4401-a711-864429847694" />

<img width="1162" height="379" alt="image" src="https://github.com/user-attachments/assets/b08256f2-e131-446c-80a7-5966172e461c" />

<img width="447" height="320" alt="image" src="https://github.com/user-attachments/assets/6290919f-5397-410c-bc60-9e0dbe13e76c" />

<img width="640" height="385" alt="image" src="https://github.com/user-attachments/assets/ef63ecbf-7687-4065-ac75-03d12a230635" />

<img width="642" height="385" alt="image" src="https://github.com/user-attachments/assets/02323657-031d-4dcc-8f7c-d63c497641d1" />

<img width="511" height="384" alt="image" src="https://github.com/user-attachments/assets/a91e98ee-14b9-4d15-aed8-ddf2572db5d0" />

<img width="1165" height="322" alt="image" src="https://github.com/user-attachments/assets/5201f505-6ad4-422a-bf67-dc900bfcca77" />

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
