# Iris Flower Classification - Technical Report

## Problem Statement

The **Iris flower** belongs to a genus of flowering plants with three primary species:
- *Iris setosa*
- *Iris versicolor*
- *Iris virginica*

These species are distinguishable based on four key measurements:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

## Objective

To develop a **machine learning model** that classifies Iris flowers into their respective species based on the above physical measurements. The goal is to **automate** species identification.

## Dataset

- **Features**: Sepal length, Sepal width, Petal length, Petal width
- **Target classes**: `setosa`, `versicolor`, `virginica`

## Approach

1. **Data Exploration**:
   - Identified feature distributions and patterns among species.
   - *Iris-setosa* showed distinct feature values compared to the other species.

2. **Data Preprocessing**:
   - Handled missing values (if any)
   - Encoded categorical data
   - Normalized features if required

3. **Model Selection**:
   - Multiple models were trained and evaluated.
   - Overfitted models (with 100% train scores) were discarded.

4. **Evaluation Metric**:
   - Primary metric: **Recall**
   - Other metrics: Precision, F1-score

## Model Results

| Sl. No. | Model                 | Recall (Train %) | Recall (Test %) |
|---------|-----------------------|------------------|-----------------|
| 1       | Decision Tree (tuned) | 95.24            | 95.56           |
| 2       | Random Forest (tuned) | 97.14            | 97.78           |
| 3       | Naive Bayes           | 94.28            | 97.78           |
| 4       | Naive Bayes (tuned)   | 94.28            | 97.78           |

## Final Model

**Tuned Random Forest** was selected as the final model due to its:
- High recall on both train and test sets
- Interpretability and robustness
- Generalization performance

## Key Insights

- *Iris-setosa* is linearly separable from the other species.
- Random Forest ranked high in performance without overfitting.
- Naive Bayes provided surprisingly competitive results.

## Challenges and Future Work

- **Feature Engineering**: Further exploration of derived features.
- **Model Optimization**: Try ensemble learning or neural networks.
- **Explainability**: Use SHAP or feature importance analysis for interpretability.

## Applications

- Automated species classification in **botany and horticulture**
- Educational tools for biology students
- Environmental monitoring using floral data

---
**Note**: All evaluations were performed on stratified train-test splits and verified with cross-validation where necessary.
