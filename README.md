# House Price Prediction

This project predicts residential property sale prices using the **Ames Housing dataset**, which contains 1,460 observations of homes in Ames, Iowa (2006–2010). The dataset was curated by Dean De Cock for statistical modeling research.

## 📂 Dataset
- Source: [Ames Housing Dataset](https://jse.amstat.org/v19n3/decock.pdf)
- Features: Numeric and categorical variables describing property characteristics.

## ✅ Project Goals
- Clean and preprocess data.
- Explore feature relationships.
- Build and evaluate predictive models for house prices.

## 🔍 Data Preparation
- Missing Values:
  - Drop columns with >60% missing data.
  - Impute remaining values (median for numeric, mode for categorical).
- Target Variable: Log-transform `SalePrice` to reduce skew.
- Feature Engineering:
  - One-Hot Encoding for categorical variables.
  - Standardize numeric features.

## 📊 Models & Results
### 1. Linear Regression
- Strongest predictors: OverallQual, GrLivArea, GarageCars, TotalBsmtSF.
- Applied log transformation to SalePrice.

### 2. Random Forest
- Tuned hyperparameters: n_estimators=500, max_depth=10, etc.
- Metrics:
  - RMSE: $39,683.90
  - MAE: $26,273.38
  - R²: 0.725
- Top features: GrLivArea, TotalBsmtSF, LotArea, YearBuilt.

### 3. XGBoost
- After tuning: RMSE ≈ $23,891.
- Most influential features: Overall quality, neighborhood, above-ground square footage.

### 4. K-Nearest Neighbors
- Best k: 7.
- RMSE: $34,098.89 (≈55% improvement over baseline).

## 📌 Key Takeaways
- Overall Quality and Neighborhood are the most influential factors.
- Size matters, but location and material quality dominate price prediction.
- Advanced models (XGBoost) outperform simpler ones.
- Challenges: Missing data handling, feature selection, and maintaining collaborative workflows.

## 🚀 Recommendations
- Explore regularization techniques (Ridge/Lasso).
- Consider tree-based models for better handling of high-dimensional data.
- Improve preprocessing to reduce RMSE further.

