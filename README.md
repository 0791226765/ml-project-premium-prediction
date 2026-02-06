# 🏥 Predictive Health Insurance Model

This project predicts **health insurance premiums** based on individual demographic and health-related features using **Machine Learning**.  
It also includes an interactive **Streamlit web application** for real-time premium prediction.

---

## 📌 Project Overview

I will develop a predictive model for Shield Insurance to estimate health insurance
premiums based on factors like age, smoking habits, BMI, and medical history. The project has
two phases:
1. Phase 1 (MVP): Build and deploy a predictive model with a Streamlit application.
2. Phase 2: Develop infrastructure for straight-through processing (STP) of insurance quotes
(detailed planning and estimation for this phase will be done later).

---

## 🧠 Machine Learning Approach

- **Problem Type:** Regression
- **Model Used:** After Detailed Error Analysis, 2 models trained based on age group (Regression model for <25 and XGBoost>25)
- **Target Variable:** `charges` (Annual premium amount)
- **Evaluation Metrics:**  
  - R² Score  
  - Mean Absolute Error (MAE)  
  - Root Mean Squared Error (RMSE)

---

## 📊 Features Used

| Feature              | Description                                |
|----------------------|--------------------------------------------|
| age                  | Age of the insured person                  |
| gender               | Male, Female                               |
| region               | Where the insured come from                |
| marital_status       | Married, Unmarried                         |
| number_of_dependants | Dependants the insured person has          |
| bmi_category         | Underweight, Normal, Overweight            |
| smoking_status       | Regular, Occasional, No smoking            |
| employment_status    | self employed, freelancer, employed        |
| income_level         | Income band of the insured                 |
| income_lakhs         | Actual income of the insured               |
| medical_history      | Existing medical conditions                |
| genetical risk       | the level of genetical risk of the insured |
| insurance plan       | Bronze, Silver, Gold                       |

---

## 🗂 Project Structure

```text
ml-project-premium-prediction/
│
├── artifacts:
    └── model_rest.joblib # Model for age group >25
    └── model_young.joblib # Model for age group <=25
    └── scaler_rest.joblib # Scaler for age group >25
    └── scaler_young.joblib # Scaler for age group <=25
        
│   ├── main.py    # Streamlit application
    └── prediction.py # backend processing
│   └── requirements.txt    # App dependencies
│
├── notebooks/
│   └── Healthcare_premium_prediction_rest_with_gr.ipynb # Model training for age group >25
│   └── Healthcare_premium_prediction_young_with_gr.ipynb # Model training for age group <=25
├── data/
│   └── premiums_rest.xlsx # Data for the age group >25
    └── premiums_young_with_gr.xlsx # Data for the age group <=25
│
├── README.md
└── .gitignore
