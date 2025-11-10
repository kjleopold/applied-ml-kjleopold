# Titanic Survival Classification Project

## Overview
In this project, we explored the Titanic dataset to predict passenger survival using three machine learning models: Decision Tree, Support Vector Machine (SVC), and Neural Network. We evaluated model performance across three different feature sets and visualized how the models made decisions. The goal was to understand which features and models were most effective at predicting survival.

## Features and Cases
We tested three feature sets:

1. **Case 1: Alone**  
   - Input feature: `alone` (whether the passenger was traveling alone)  
   - Simple 1D feature to see basic predictive power.

2. **Case 2: Age**  
   - Input feature: `age`  
   - Examines whether age alone can help classify survival.

3. **Case 3: Age + Family Size**  
   - Input features: `age` and `family_size`  
   - Combines features to capture more complex patterns in survival.

## Models
- **Decision Tree**: Splits data based on feature thresholds to make predictions.  
- **Support Vector Machine (SVC)**: Finds the best boundary between classes. 
- **Neural Network**: Learns complex patterns from the data.

## Visualization
- **Decision Trees**: Plotted to show how features split the data and lead to survival predictions.  
- **Support Vectors (SVC)**: Scatter plots for 1D and 2D cases highlight which points define the decision boundary.  
- **Neural Network (Case 3)**: 2D decision surface shows the predicted survival regions across age and family size, with actual test points overlaid.

## Findings
- Simple features like `alone` can provide decent predictions, but combining features improves model performance.  
- Neural Networks captured complex patterns best in Case 3.  
- Decision Trees were easy to interpret, and SVC performance depended heavily on input features.  
- Visualizations helped understand how models separate survivors from non-survivors.

## Challenges
- Handling missing data for features like `age` and `family_size`.  
- Visualizing two-dimensional decision boundaries.  
- Tuning models for good accuracy without overfitting.

## Next Steps
- Experiment with additional features such as `sex`, `pclass`, and `fare`.  
- Try different SVC kernels or Neural Network architectures to optimize performance.  
- Apply cross-validation to assess model stability.  
- Explore feature importance across models to identify key factors affecting survival.

## Requirements
- Python 3.x  
- pandas  
- numpy  
- matplotlib  
- scikit-learn  

## How to Run
1. Load the Titanic dataset.  
2. Preprocess the data (handle missing values, create `family_size`, etc.).  
3. Run the scripts for each case and model.  
4. Generate plots for Decision Trees, SVC support vectors, and Neural Network decision surfaces.  
5. Analyze results using classification reports and visualizations.