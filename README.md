# 👩‍💻 Employee Attrition Prediction using Machine Learning

> **🎓 Master's Thesis Project – M.S. Business Analytics, Elon University (2025)**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-7CB342?style=for-the-badge)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6F00?style=for-the-badge)
![SHAP](https://img.shields.io/badge/SHAP-Explainable_AI-blue?style=for-the-badge)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

## 📖 Overview

Employee turnover is one of the most significant challenges organizations face, leading to substantial costs related to recruitment, onboarding, productivity loss, and knowledge transfer. This project develops an end-to-end machine learning solution to identify employees at risk of leaving an organization before attrition occurs, enabling Human Resources teams to implement proactive retention strategies.

Unlike many employee attrition studies that focus solely on predictive accuracy, this project emphasizes **interpretability, fairness, and practical deployment**, making the solution suitable for real-world HR analytics applications.

---

## 🎯 Business Problem

Employee attrition is costly and difficult to predict using traditional HR methods.

The objective of this project was to answer four key questions:

* Can employee attrition be accurately predicted using structured HR data?
* Which employee characteristics contribute most to attrition risk?
* Can machine learning predictions remain transparent and fair?
* How can these predictions support strategic HR decision-making?

---

## 📊 Dataset

**Source:** IBM HR Analytics Employee Attrition Dataset (Kaggle)

* 1,470 employees
* 35 employee-related features
* Binary target variable (Attrition)
* Demographic, compensation, satisfaction, performance, and job-related variables

---

## ⚙️ Methodology

The project followed a complete machine learning workflow:

1. Data exploration and preprocessing
2. One-Hot Encoding of categorical variables
3. Feature scaling
4. SMOTE to address class imbalance
5. Model development
6. Cross-validation
7. Hold-out evaluation
8. SHAP explainability
9. Fairness assessment using IBM AI Fairness 360
10. Deployment of the best-performing model as a web application

---

## 🤖 Machine Learning Models

Three supervised learning models were evaluated:

* XGBoost
* LightGBM
* Multi-Layer Perceptron (MLP)

LightGBM achieved the strongest overall performance and was selected for deployment.

---

## 📈 Results

### Best Model

**LightGBM**

| Metric                | Value     |
| --------------------- | --------- |
| ROC-AUC               | **0.802** |
| Accuracy              | **0.878** |
| Precision (Attrition) | **0.789** |
| Recall (Attrition)    | **0.319** |
| F1 Score              | **0.455** |

The project demonstrated that modern gradient boosting methods outperform the deep learning model tested on this structured HR dataset.

<img width="500" height="460" alt="models_comparison_XGBoost_LightGBM_MLP" src="https://github.com/user-attachments/assets/b097e36d-0167-4e62-85ad-2dd39c6ed308" />

---

## 🔍 Explainable AI (SHAP)

To improve transparency and trust, SHAP (SHapley Additive exPlanations) was used to explain individual model predictions.

The most influential features included:

* Overtime
* Stock Option Level
* Environment Satisfaction
* Monthly Income
* Job Satisfaction
* Age
* Years With Current Manager

These insights allow HR professionals to understand **why** employees are predicted to leave rather than relying on black-box predictions.

<img width="563" height="652" alt="SHAP_summary_plot" src="https://github.com/user-attachments/assets/b6859fc3-d904-4f8c-a258-e20491355b22" />

---

## ⚖️ Fairness Evaluation

Because HR applications directly impact employees, fairness was evaluated using IBM AI Fairness 360.

Gender bias analysis showed:

* Disparate Impact ≈ 1.01
* Statistical Parity Difference ≈ 0.007

These results indicate that the deployed model does not exhibit meaningful gender bias.

---

## ☁️ Deployment

The best-performing LightGBM pipeline was serialized and deployed using Google Cloud Functions.

A React-based web application allows HR users to:

* Upload employee datasets (.csv)
* Predict employee attrition
* Generate attrition probabilities
* Download prediction results

The deployment demonstrates how machine learning models can transition from research into practical business applications.

#### Web application repository : https://github.com/NarjisGiacalone/attrition-app
#### Web application deployment video : https://youtu.be/4KDF40O2Yg4

<img width="1842" height="475" alt="web_app_screenshot" src="https://github.com/user-attachments/assets/49c99bb5-5e1b-42f8-a628-1cf038eb21b6" />

---

## 💼 Business Recommendations

Based on model explainability, organizations can reduce employee attrition by focusing on:

* Managing excessive overtime
* Improving workplace satisfaction
* Offering competitive compensation and stock options
* Supporting manager-employee relationships
* Creating clear career progression opportunities

---

## 📁 Repository Structure

```text
employee-attrition-prediction/

├── thesis/
├── presentation-slides/
├── notebooks/
├── data/
├── images/
└── README.md
```

---

## 🛠️ Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* LightGBM
* SHAP
* IBM AI Fairness 360
* SMOTE
* Google Cloud Functions
* React
* Jupyter Notebook

---

## 📚 Repository Contents

This repository includes:

* Complete master's thesis
* Thesis defense presentation
* Jupyter notebooks
* Dataset (IBM HR Analytics)
* Visualizations
* Machine learning workflow

---

## 🚀 Future Improvements

Potential extensions include:

* Testing additional HR datasets
* Incorporating temporal employee data
* Real-time prediction pipelines
* Expanded fairness analysis across additional protected attributes
* Integration with enterprise HR information systems

---

## 👤 Author

**Narjis Jebali Giacalone**

🔗 www.linkedin.com/in/narjis-giacalone

M.S. Business Analytics

Elon University

2025
