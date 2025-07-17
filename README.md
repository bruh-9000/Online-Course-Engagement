# Online Course Engagement

Given features derived from an online course platform, predict the likelihood that the given user completed their course in its entirety.

**Dataset:** [Link](https://www.kaggle.com/datasets/rabieelkharoua/predict-online-course-engagement-dataset/data)

## Overview
- Binary classification problem
- Used 7 tree-based models
- Engineered synthetic features and evluated them
- Best model: LightGBM with `TimePerVideo` synthetic feature
    - F1 Score: 73.21%
    - Accuracy: 77.46%
    - ROC AUC: .8746

## Modeling Approach
- Analyzed all features for class balance, correlation, and distribution issues
- **Prevented data leakage** by excluding `CompletionRate`, which directly reflects course progress
- Created multiple synthetic features, but kept only `TimePerVideo` due to its impact and low multicollinearity
- Used **5-fold Stratified Cross-Validation** for reliable evaluation
- Compared models on **F1** and **Accuracy**, prioritizing F1 due to slight class imbalance
- Final selection based on balanced performance across all metrics