# Online Course Engagement

Given features derived from an online course platform, predict the likelihood that the given user completed their course in its entirety. The goal of the model is to identify students at risk of not completing the course, in order to enable early intervention.

**Dataset:** [Link](https://www.kaggle.com/datasets/rabieelkharoua/predict-online-course-engagement-dataset/data)

## Overview
- Binary classification problem
- Used three tree-based models
- Engineered synthetic features and evaluated them
- Best model: LightGBM
    - F1 Score: 75.33%
    - Accuracy: 75.26%
    - ROC AUC: .8624

## Modeling Approach
- Analyzed all features for class balance, correlation, and distribution issues.
- **Prevented data leakage** by excluding `CompletionRate`, which directly reflects course progress.
- Created multiple synthetic features, did not keep any due to their high feature correlation.
- Used **5-fold Stratified Cross-Validation** for reliable evaluation.
- Compared models on **F1** and **Accuracy**, prioritizing F1 due to slight class imbalance.
- Final selection based on balanced performance across all metrics.
