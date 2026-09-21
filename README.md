# RabTech Academy Task 04 — Supervised Classification Modeling & Tuning

## Objective
Train and compare at least four supervised classification architectures, tune hyperparameters with stratified cross-validation, evaluate performance, and serialize the selected champion model.

## Dataset
UCI Adult / Census Income dataset.

Official source: https://archive.ics.uci.edu/dataset/2/adult  
DOI: https://doi.org/10.24432/C5XW20  
License: CC BY 4.0

## Models compared
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting

## Required evidence included
- Jupyter Notebook
- Four-model comparison
- Stratified K-fold cross-validation
- GridSearchCV hyperparameter tuning
- Precision, Recall, F1 and ROC-AUC
- Confusion matrices
- ROC curves
- Champion selection based on validation ROC-AUC
- Code that serializes the final fitted pipeline as `champion_model.joblib`

## Important
Run the notebook from top to bottom. The final section creates `champion_model.joblib`. Commit that generated file to this repository before submitting the RabTech deliverable.

## Setup
```bash
pip install -r requirements.txt
jupyter notebook supervised-modeling-tuning.ipynb
```

This is an educational project. The Adult dataset contains demographic attributes; predictive performance alone does not establish fairness or suitability for consequential decisions.
