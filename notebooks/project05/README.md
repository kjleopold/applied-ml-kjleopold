# Project 5 – Ensemble Machine Learning on Wine Quality

**Author:** Kellie Leopold  
**Date:** 11/21/2025  

---

## Overview

This project explores ensemble machine learning techniques to classify wine quality using the UCI Red Wine Quality dataset. Instead of predicting a numeric score, the dataset is transformed into three quality classes (low, medium, high). The notebook evaluates multiple ensemble methods and compares their performance using accuracy, precision, recall, and F1 score.

---

## Objectives

1. Load and prepare the Red Wine Quality dataset for classification.  
2. Convert the original quality scores into three classes.  
3. Select meaningful features and justify their inclusion.  
4. Train and evaluate ensemble models, including:  
   - AdaBoost Classifier  
   - MLP Classifier  
5. Compare performance using accuracy, precision, recall, and F1 score.  
6. Analyze the accuracy–F1 gap to assess model generalization.  
7. Summarize insights and challenges discovered during experimentation.

---

### Notebook Sections

1. **Import and Inspect Data**  
   Load the dataset, verify its structure, and explore the original numeric quality distribution.

2. **Prepare and Transform Data**  
   Convert continuous quality ratings into three discrete classes.  
   Scale numerical features when needed and split the data into training and testing sets.

3. **Feature Selection and Justification**  
   Identify the most relevant physicochemical properties (such as alcohol, volatile acidity, and sulphates) and justify their inclusion based on correlations and domain intuition.

4. **Train Ensemble Models**  
   Train and evaluate AdaBoost and MLP models.  
   Compare training vs. testing performance to understand overfitting or underfitting.

5. **Model Evaluation and Comparison**  
   Generate a performance summary table including accuracy, precision, recall, and F1 score for each model.  
   Examine the accuracy–F1 gap to assess how well each model generalizes.

6. **Final Thoughts & Insights**  
   Summarize what worked well, which model performed best, and what improvements could be made.

---

## Key Findings

- **Best Overall Model:** The MLP Classifier generally produced the highest accuracy and strongest F1 score across all classes.  
- **Performance Gap:** AdaBoost showed a wider accuracy–F1 gap, indicating poorer generalization compared to MLP.  
- **Class Balance Effects:** Mid-range quality wines were predicted more accurately than low or high extremes, consistent with the dataset’s natural imbalance.  
- **Insights:** Ensemble methods improved performance over simple baseline models, especially when feature scaling and class grouping were correctly applied.

---

## Challenges

- The dataset’s imbalance made it harder for models to correctly predict low and high quality classes.  
- Choosing the proper number of estimators and learning rates required experimentation.  
- MLP training required careful scaling and tuning to avoid unstable or slow convergence.

---

## Next Steps

- Add models such as Random Forest, Gradient Boosting, or XGBoost for deeper comparison.  
- Use SMOTE or class-weight adjustments to improve prediction of minority classes.  
- Explore feature engineering, such as combining related acidity measures.  
- Expand the analysis to the white wine dataset for cross-dataset comparison.
"""