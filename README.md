# Linear Regression on Advertising Data

A regression analysis exploring how TV, Radio, and Newspaper advertising
spend relate to Sales, using scikit-learn for modeling and statsmodels/
scipy for diagnostic testing of the model's assumptions.

## Overview

This project fits a multiple linear regression model to the classic
`Advertising.csv` dataset and validates the model by checking the
standard linear regression assumptions:

- **Homoscedasticity** — Goldfeld-Quandt test and Bartlett's test
- **Normality of residuals** — distribution plot of residuals
- **Autocorrelation** — Ljung-Box test, ACF/PACF plots
- **Multicollinearity** — correlation heatmap of features

## Dataset

`Advertising.csv` — advertising spend (TV, Radio, Newspaper) and
resulting Sales figures. Place this file in the project root before
running the notebook.

## Requirements

```bash
pip install numpy pandas seaborn matplotlib scikit-learn statsmodels scipy
```

## Usage

1. Clone the repo and make sure `Advertising.csv` is in the same directory
   as the notebook.
2. Launch Jupyter and open `linear_regression.ipynb`:
```bash
   jupyter notebook linear_regression.ipynb
```
3. Run all cells to reproduce the analysis.

## Workflow

1. Load and explore the data (`.head()`, `.describe()`, pairplots)
2. Split features/target, standardize features with `StandardScaler`
3. Train/test split and fit a `LinearRegression` model
4. Evaluate fit (R²) and residuals
5. Run diagnostic tests for regression assumptions
6. Visualize feature correlations with a heatmap

## Results

- Reports R² score on the training set
- Residual diagnostics to confirm (or flag violations of) linear
  regression assumptions

## License

MIT