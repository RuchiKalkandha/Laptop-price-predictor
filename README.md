# Laptop Price Prediction

This project builds a regression-based system to predict laptop prices using a dataset of 1302 entries and 13 features, including hardware specifications and brand indicators. The goal is to benchmark multiple models and identify the most accurate and generalizable approach for price estimation.

##  Dataset Overview

- **Source**: Kaggle
- **Rows**: 1302
- **Columns**: 13
- **Features**:
  - Categorical: `Company`, `TypeName`, `Cpu brand`, `Gpu brand`, `os`
  - Numerical: `Ram`, `Weight`, `Price`, `PPI`, `HDD`, `SSD`
  - Binary: `TouchScreen`, `IPS`

##  Models Applied

| Model              | R² Score | MAE     |
|-------------------|----------|---------|
| Linear Regression | 0.807    | 0.210   |
| Ridge Regression  | 0.812    | 0.209   |
| Lasso Regression  | 0.807    | 0.211   |
| KNN Regressor     | 0.803    | 0.193   |
| Decision Tree     | 0.835    | 0.184   |
| SVR               | 0.808    | 0.202   |
| XGBoost           | 0.885    | 0.164   |
| Random Forest     | 0.887    | 0.159   |
| Extra Trees       | 0.885    | 0.162   |
| AdaBoost          | 0.799    | 0.223   |
| Gradient Boosting | 0.882    | 0.160   |
| Voting Regressor  | **0.890**| **0.158**|

##  Optimization Strategy

- **Hyperparameter Tuning**: Used `RandomizedSearchCV` to identify optimal parameters for models like XGBoost, Random Forest, and SVR.
- **Ensemble Learning**: Combined top-performing models using `VotingRegressor` to boost generalization and reduce error.

##  Key Highlights

- Achieved best performance with `VotingRegressor` (R² = 0.89, MAE = 0.158).
- Demonstrated strong ensemble learning and model selection skills.
- Applied rigorous benchmarking across 12+ models.
- Tuned models using randomized search for scalable optimization.

##  Tech Stack

- **Language**: Python
- **Libraries**: pandas, scikit-learn, xgboost, numpy, matplotlib, seaborn

