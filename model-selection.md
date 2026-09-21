# Model Selection Plan

## Validation strategy
The training partition is evaluated with **Stratified 5-Fold Cross-Validation**. Stratification preserves the class ratio in each fold.

## Candidate architectures
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting

## Champion rule
The champion is selected using the **highest mean cross-validated ROC-AUC** on the training data. The untouched test set is not used to choose the champion.

## Hyperparameter optimization
After baseline comparison, `GridSearchCV` tunes the selected model family with stratified 5-fold cross-validation and ROC-AUC scoring.

## Final evaluation
The tuned champion is evaluated once on the held-out test set using:
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC curve

## Serialization
The final end-to-end fitted Scikit-Learn pipeline is saved with Joblib as:

`champion_model.joblib`

Because preprocessing is inside the pipeline, the serialized artifact accepts raw records with the same input columns.

## Responsible-use note
The UCI Adult dataset contains demographic attributes including race and sex. This exercise demonstrates ML engineering techniques and is not a recommendation to use income prediction for consequential decisions.
