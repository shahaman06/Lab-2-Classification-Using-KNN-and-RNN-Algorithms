# Lab 2

## Overview
This lab explores the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers using the Wine dataset from the `sklearn` library. The dataset contains three classes of wine, each with multiple chemical property features. The goal of this lab is to understand how different parameter values for KNN and RNN affect classification accuracy and to compare the performance of both models.

---

## Purpose
- Implement KNN and RNN classifiers on the Wine dataset.
- Observe the effect of varying parameters (k for KNN, radius for RNN) on model performance.
- Visualize trends in classification accuracy.
- Analyze and compare results to determine when each classifier might be preferable.

---

## Methodology
1. **Dataset Preparation**
   - Loaded the Wine dataset.
   - Explored features and class distribution.
   - Split data into 80% training and 20% testing sets.

2. **K-Nearest Neighbors (KNN)**
   - Tested k values: 1, 5, 11, 15, 21.
   - Trained the model on the training set.
   - Evaluated accuracy on the test set.
   - Visualized accuracy trends across different k values.

3. **Radius Neighbors (RNN)**
   - Tested radius values: 350, 400, 450, 500, 550, 600.
   - Trained the model and evaluated accuracy on the test set.
   - Visualized accuracy trends across different radius values.

---

## Key Insights
- **KNN Results**
  - Accuracy varies with k.
  - Smaller k values may lead to overfitting, while very large k values can underfit.
  - There is an optimal k that balances bias and variance for this dataset.

- **RNN Results**
  - Accuracy depends on the chosen radius.
  - Very small radii may produce many outliers, reducing accuracy.
  - Larger radii may include too many neighbors, which can dilute class distinctions.

- **Comparison**
  - KNN generally produced more consistent accuracy trends across tested values.
  - RNN can be sensitive to radius choice and may generate outliers in prediction.
  - KNN is preferable when dataset classes are well-separated and evenly distributed.
  - RNN may be useful when local density varies across the dataset.

---

## Challenges
- Choosing an appropriate radius for RNN required careful observation due to potential outliers.
- Visualizing the results helped in identifying optimal parameter values.
