# Project 4 – Continuous Target Prediction Using Regression (Titanic)

**Author:** Kellie Leopold  
**Date:** 2025-11-14  

---

## Overview

This project shifts from classification (predicting survival) to regression, focusing on predicting a continuous numeric target: the `fare` paid by passengers on the Titanic. Using the Titanic dataset from Seaborn, we explore different regression models and evaluate their performance.

---

## Objectives

1. Explore and prepare the Titanic dataset for regression.
2. Select meaningful features and justify their inclusion.
3. Train multiple regression models:
   - Linear Regression
   - Ridge Regression
   - Elastic Net
   - Polynomial Regression
4. Compare model performance using metrics like R², RMSE, and MAE.
5. Visualize predictions and analyze model performance.
6. Summarize insights and discuss challenges encountered.

---

### Notebook Sections

1. **Import and Inspect Data**  
   Load the Titanic dataset and verify its structure.

2. **Data Exploration and Preparation**  
   Handle missing values, create derived features (e.g., `family_size`), and convert categorical features to numeric where needed.

3. **Feature Selection and Justification**  
   Define multiple feature sets for regression models:  
   - Case 1: `age`  
   - Case 2: `family_size`  
   - Case 3: `age` + `family_size`  
   - Case 4: Custom feature(s) chosen based on analysis: `pclass`

4. **Train Regression Models**  
   Train and evaluate Linear Regression models for all feature cases, comparing training and test performance.

5. **Compare Alternative Models**  
   Apply Ridge, Elastic Net, and Polynomial Regression to the best-performing feature set.  
   Visualize polynomial fits and higher-order polynomial results for deeper insight.

6. **Final Thoughts & Insights**  
   Summarize findings, challenges, and potential next steps.

---

## Key Findings

- **Best Features:** Case 3 (`age` + `family_size`) performed best.  
- **Best Model:** Polynomial Regression (degree 3) captured non-linear patterns in fare more accurately than linear models.  
- **Insights:** Fare depends on multiple factors, including passenger age, family size, and possibly class or gender. Regularization helped reduce overfitting in models with multiple features.  

---

## Challenges

- Missing values for `age` required median imputation.  
- Visualizing higher-order polynomial predictions required careful plotting to compare actual vs. predicted fares.  
- Selecting meaningful features for Case 4 required experimentation and justification.

---

## Next Steps (Optional)

- Include additional features like `pclass` or `sex_encoded` to improve predictions.  
- Predict `age` instead of `fare` to explore a different regression target.  
- Apply log transformation to `fare` to reduce skew in the target variable.  