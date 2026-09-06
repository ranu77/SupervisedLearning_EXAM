# Summary Report — House Price Prediction

## Business Problem
A PropTech startup needs an automated house price estimator to help buyers and 
sellers benchmark property values. We used the Ames Housing Dataset (1,460 homes, 
79 features) to build a regression model predicting SalePrice in USD.

## Preprocessing & Feature Engineering
- Missing values handled by category: NaN→None for quality columns, NaN→0 for 
  area columns, median for remaining numericals
- Removed 2 extreme outliers in GrLivArea (>4000 sqft, price <$300K) that would 
  distort linear model coefficients
- Engineered 5 new features: TotalSF, HouseAge, RemodAge, HasGarage, HasPool
- Applied ordinal encoding to quality columns, one-hot encoding to nominal 
  categoricals, label encoding to high-cardinality Neighborhood
- Applied log1p transformation to skewed features and target (SalePrice)
- Scaled all features using StandardScaler

## Best Model
**XGBoost Regressor** achieved the best performance:
- RMSE: $19,672 | MAE: $14,134 | R²: 0.9299
- XGBoost captures non-linear relationships and interaction effects between 
  features that linear models miss. Boosting iteratively corrects errors, 
  making it more precise than Random Forest on this dataset.

## Top 3 Predictive Features
1. **OverallQual** — Overall material and finish quality is the single strongest 
   signal. A real estate professional should always assess build quality first.
2. **TotalSF** — Total usable area drives price more than any individual floor. 
   Buyers pay for total livable space across all levels.
3. **GrLivArea** — Above-ground living area commands a premium over basement 
   space. Highlights importance of above-grade square footage in listings.

## Next Steps for Production
- Collect more recent transaction data — Ames dataset is from 2006–2010
- Add external features: school district ratings, proximity to amenities, 
  crime rates
- Explore ensembling XGBoost + Lasso for combined interpretability and accuracy
- Apply Bayesian optimisation (Optuna) for more efficient hyperparameter search
- Build a FastAPI endpoint to serve predictions in real time