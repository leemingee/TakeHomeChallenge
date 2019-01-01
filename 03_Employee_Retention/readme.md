# project_EmployeeRetention (Supervised-Classification)
Build machine learning model(s) to predict whether or not an employee is to leave.

## Project Context:
Software company HR department wants to predict whether an employee is likely to leave in order to retain employees proactively.

## Problem Satement:
1. Current retention process is prone to human error
2. No systematic way to derive insights across all employees left
3. Retrospective rather proactive approach

- **Data:**
Employee data of client company (14249 x 10)

- **Machine Learning Task:**
Supervised Learning - Classification

- **Target Variable**"
Status (Employed/Left)

- **Goal:** 
Build models to predict whehter an employee is lifely to leave

- **Deliverable:**
Executable model script

## Project Detail:
- **Steps:**: EDA, Data Cleaning, Feature Engineering, Model Tuning, Project Delivery
- **Algorithms Tried:** Focused on three models to coarse tune as baseline performance is satisfactory: LogisticRegression, RandomForestClassifier, XGBClassifer (using default setting), kept Random Forest as it achieves similar performance as Xgboost
- **Performance Measure:** Use Precision Recall Curve and ROC Curve to compare model performance and calculate Average Precision score, F1 score, and AUC.
- **Identified primal cut off point/thresholds:** 0.5(RF), 0.41(xgb)
- **Test Set Performance:** AUC = 0.99, the model performs well on prediciting whether an employee is likely to leave
- **Generated script file with winning model**