# Credit Risk Prediction using XGBoost & SHAP Explainability

This project builds a Machine Learning model to predict **credit default risk** using the German Credit Dataset.  
The model is trained using **XGBoost**, and the predictions are explained using **SHAP (SHapley Additive exPlanations)** to understand *why* the model gives a particular prediction.

---

## 📌 Project Overview

Credit risk prediction is widely used in banking and finance to decide whether a customer is likely to default on a loan.  
This project demonstrates:

✔ Data preprocessing  
✔ Feature encoding & scaling  
✔ Model training using XGBoost  
✔ Performance evaluation  
✔ Explainability analysis using SHAP  
✔ Global & local model interpretations  

---

## 📂 Project Structure

credit-risk-project/
│
├── data/
│ └── german_credit_data.csv
│
├── output/
│ ├── shap_summary.png
│ ├── shap_waterfall_1.png
│ ├── shap_waterfall_2.png
│ ├── shap_waterfall_3.png
│ ├── quick_report.txt
│ ├── quick_report.json
│ ├── xgb_model.joblib
│ └── preprocessor.joblib
│
├── credit_risk.ipynb # Jupyter Notebook with complete code
├── requirements.txt # Required Python libraries
└── README.md

yaml
Copy code

---

## 📊 Dataset Description

The dataset includes customer demographic & financial information:

| Column Name        | Description |
|--------------------|-------------|
| Age                | Customer age |
| Sex                | male / female |
| Job                | Job skill category |
| Housing            | own / rent / free |
| Saving accounts    | level of savings |
| Checking account   | balance in checking account |
| Credit amount      | loan amount requested |
| Duration           | loan duration in months |
| Purpose            | reason for loan |

A synthetic **default** column (0 = no default, 1 = default) is generated based on high credit amount & long duration.

---

## ⚙️ Preprocessing Steps

- Missing values handled using `SimpleImputer`
- Numerical features scaled using `StandardScaler`
- Categorical features encoded with `OneHotEncoder`
- Train-test split applied (80/20)

---

## 🤖 Machine Learning Model

Algorithm used:

### **XGBoost Classifier**
- n_estimators = 200  
- max_depth = 5  
- learning_rate = 0.1  
- eval_metric = "logloss"  

XGBoost is chosen because:
- Works well with small/medium-sized datasets  
- Offers built-in feature importance  
- Compatible with SHAP explainability  

---

## 📈 Model Evaluation

Metrics used:
- **Accuracy**
- **F1-score**
- **ROC AUC**
- **Confusion Matrix**
- **Classification Report**

These results are saved in the `output/quick_report.txt` file.

---

## 🧠 Explainability using SHAP

SHAP is used to explain:

### ⭐ Global explanation:  
`shap_summary.png`  
Shows top important features contributing to credit default risk.

### ⭐ Local explanations (individual predictions):  
`shap_waterfall_1.png`  
`shap_waterfall_2.png`  
`shap_waterfall_3.png`  

These explain **why** the model predicted default for specific customers.

---

## 📦 Requirements

Install all required Python packages:

pip install -r requirements.txt

yaml
Copy code

(or see `requirements.txt` file)

---

## ▶️ Running the Project

1. Clone the repository:
git clone https://github.com/your-username/credit-risk-project

markdown
Copy code

2. Install dependencies:
pip install -r requirements.txt

mathematica
Copy code

3. Open Jupyter Notebook:
jupyter notebook

yaml
Copy code

4. Run `credit_risk.ipynb` cell by cell.

---

## 📝 Summary

This project demonstrates a full pipeline for:

- Credit risk prediction  
- Model training  
- Performance evaluation  
- Explainable AI using SHAP  

It is suitable for academic assignments, AI/ML practice, and financial risk modelling projects.
