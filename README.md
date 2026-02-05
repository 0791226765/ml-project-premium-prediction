# 🏥 Predictive Health Insurance Model for Shield Insurance

This project predicts **health insurance premiums** based on individual demographic and health-related features using **Machine Learning**.  
It also includes an interactive **Streamlit web application** for real-time premium prediction.

---

## 📌 Project Overview

Develop a predictive model for Shield Insurance to estimate health insurance premiums based on factors like age, 
smoking habits, BMI and medical history and provides an easy-to-use web interface for users.

---

## 🧠 Machine Learning Approach

- **Problem Type:** Regression
- **Model Used:** Model segmentation done. 2 models trained based on age group (Regression <25 and XGBoost>25) after Error Analysis
- **Target Variable:** `charges` (Annual premium amount)
- **Evaluation Metrics:**  
  - R² Score  
  - Mean Absolute Error (MAE)  
  - Root Mean Squared Error (RMSE)

---

## 📊 Features Used

| Feature              | Description                         |
|----------------------|-------------------------------------|
| age                  | Age of the insured person           |
| gender               | Male, Female                        |
| Region               | Where the insured come from         |
| marital_status       | Marriage status                     |
| number_of_dependants | Dependants the insured person has   |
| BMI_Category         | Underweight, Normal, Overweight     |
| smoking_status       | Regular, occassional or No smoking  |
| employment_status    | self employed, freelancer, employed |
| income_level         | Income category of the insured      |
| income_lakhs         | Actual income of the insured        |
| medical_history      | Existing medical conditions         |
| genetical risk       | the level of genetical risk         |
| insurance_plan       | Bronze, Silver, Gold                |

---

## 🗂 Project Structure

```text
ml-project-premium-prediction/
│
├── app/
│   ├── app.py              # Streamlit application
│   ├── model.pkl           # Trained ML model
│   └── requirements.txt    # App dependencies
│
├── notebooks/
│   └── model_training.ipynb
│
├── data/
│   └── insurance.csv
│
├── README.md
└── .gitignore
