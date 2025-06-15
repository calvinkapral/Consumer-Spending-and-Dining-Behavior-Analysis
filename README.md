# Consumer Spending and Dining Behavior Analysis

**Author**: Calvin Kapral  
**Language**: R  
**Dataset**: Percent Change in Consumer Spending (Kaggle)

---

## Project Overview

This project explores how spending on various goods and services correlates with dining out behavior in the U.S. economy.

Does spending more on non-essential items mean people eat out more? Does higher essential spending imply eating out less?

Using multiple linear regression and diagnostic tools, this project tests these hypotheses using R.

---

## Dataset

- **Source**: Kaggle  
- **Observations**: 4,730 rows  
- **Variables Used**:
  - `acf_spending`: Accommodation and food services (response)
  - `all_merchant`: All merchant category spending
  - `aer_spending`: Arts, entertainment, and recreation
  - `gen_spending`: General merchandise and apparel
  - `grf_spending`: Grocery and food stores
  - `hcs_spending`: Health care and social assistance

---

## Methods

- **EDA**: Summary statistics, correlation matrix
- **Models**:
  - Multiple Linear Regression (OLS)
  - Box-Cox Transformation (λ = 2/3)
  - Weighted Least Squares (WLS)
  - Generalized Least Squares (GLS)
  - Subset Selection with `regsubsets`
  - Forward and Backward Stepwise Selection
- **Diagnostics**:
  - Residual plots for homoskedasticity
  - Q-Q plots and Shapiro-Wilk test for normality
  - Cook’s distance and leverage for influential points
  - VIF for multicollinearity
  - Breusch–Pagan test for heteroskedasticity

---

## Key Results

- Positive relationships:
  - Arts, entertainment, general merchandise, and health spending all positively predict eating out
- Negative relationship:
  - Grocery spending is negatively correlated with dining out
- Model fit:
  - Adjusted R² ≈ 0.86
  - All predictors statistically significant (p < 0.05)
- Challenges:
  - Residuals not normally distributed
  - Heteroskedasticity present in OLS
  - Some multicollinearity (especially between spending categories)
  - Residual autocorrelation in GLS

---

## Files Included

- `Consumer_spending.Rmd`: R Markdown file for full analysis
- `Consumer_Spending.pdf`: Rendered project report
- `README.md`: This file

---

## Conclusion

The results suggest that people who spend more on non-essential items like entertainment and apparel also tend to spend more on dining out. Conversely, higher grocery spending is associated with less eating out. While the model performs well overall, some assumption violations (non-normality, heteroskedasticity) highlight the need for caution when interpreting inference.
