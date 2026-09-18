# Exam Score Prediction — Regression Models

![Project Overview](docs/images/1_project_overview.png)

Predicting student exam scores from academic and lifestyle factors using Linear Regression and Support Vector Regression (SVR).

## Dataset

20,000 student records with 11 attributes spanning demographics, education, and lifestyle (age, study hours, attendance, sleep hours, gender, course, study method, etc.). A 5,000-record subset is used for faster training while preserving the original distribution. `Exam_Score_Prediction.csv` is included so the notebook runs end-to-end with no external setup.

## Approach
- Feature encoding for categorical variables
- Standardization of numeric features
- Linear Regression vs. SVR comparison
- Hyperparameter tuning via `GridSearchCV`
- Cross-validation to guard against overfitting

## Results
Linear and Ridge Regression both land around 74% R², narrowly ahead of SVR:

![Model Comparison](docs/images/2_model_comparison.png)

The SVR model's predictions track closely with actual scores, with residuals centered around zero and no strong bias pattern:

<p align="center">
  <img src="docs/images/3_predicted_vs_actual.png" width="400"/>
  <img src="docs/images/4_residual_plot.png" width="400"/>
</p>

## Tech
Python, pandas, scikit-learn
