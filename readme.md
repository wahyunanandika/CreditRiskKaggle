# Credit Risk Prediction Project

This repository contains the code and documentation for predicting credit risk using machine learning models. The project involves several steps, including data preprocessing, model selection, hyperparameter tuning, threshold tuning, and cost evaluation.

## Project Overview

The goal of this project is to build a machine learning model that can accurately classify loan applicants into good or bad credit risk categories. The project is structured as follows:

1. **Data Preprocessing**
   - **Handling Missing Values**: Replace missing values with `np.nan`.
   - **Outlier Detection and Handling**: Outliers in `loan_int_rate` and `person_emp_length` are detected and treated using predefined thresholds.
   - **Categorical Encoding**: Categorical features are encoded using one-hot encoding or ordinal encoding as appropriate.
   - **Data Splitting**: The data is split into training and testing sets.

2. **Baseline Model**
   - **Dummy Classifier**: A baseline model is created using a `DummyClassifier` with a stratified strategy.
   - **Evaluation**: The baseline model is evaluated using the confusion matrix and a custom cost function.

3. **Model Selection**
   - **Candidate Models**: Multiple models are considered, including Random Forest, Decision Tree, AdaBoost, etc.
   - **ROC-AUC as a Guide**: ROC-AUC is used to select the best model.

4. **Hyperparameter Tuning**
   - **GridSearchCV**: Hyperparameters are tuned using GridSearchCV to find the optimal combination for the selected model.
   - **Selected Parameters**: The tuned parameters include `max_depth`, `min_samples_split`, and `min_samples_leaf` for tree-based models.

5. **Threshold Tuning**
   - **Precision-Recall Trade-off**: The threshold is adjusted to find the best balance between precision and recall.
   - **Optimal Threshold Selection**: The threshold is selected based on the optimal F1 score or by maximizing the sum of precision and recall.

6. **Final Model Evaluation**
   - **Confusion Matrix**: The confusion matrix is calculated for the baseline and the best model with the tuned threshold.
   - **Cost Evaluation**: A custom cost function is used to calculate the total cost based on false positives and false negatives.
   - **Comparison**: The costs of the baseline and best models are compared to determine the more cost-effective solution.# CreditRiskKaggle
