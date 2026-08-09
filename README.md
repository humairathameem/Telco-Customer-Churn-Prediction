# Telco Customer Churn Prediction

## Project Overview

Customer churn is an important business problem for telecom companies because losing customers directly affects revenue.

This project uses the IBM Telco Customer Churn dataset to explore customer churn patterns and build machine learning models that can identify customers who may be at risk of leaving.

The goal is to provide useful predictive insights that can support targeted customer retention strategies.

---

## Dataset

The project uses the **Telco Customer Churn** dataset from IBM, containing 7,043 customer records and 21 attributes related to customer demographics, services, contracts, billing, and churn status.

The dataset is publicly available on Kaggle:

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

---

## Project Objectives

The main objectives of this project are to:

- Understand customer churn patterns through Exploratory Data Analysis (EDA)
- Clean and prepare the dataset for machine learning
- Encode categorical variables
- Scale numerical features
- Train multiple classification models
- Compare model performance using appropriate evaluation metrics
- Analyze feature importance
- Provide business recommendations to help reduce customer churn

---

## Project Workflow

The project follows the following workflow:

1. Import Libraries
2. Load Dataset
3. Preview Dataset
4. Understand Dataset Structure
5. Check Data Types
6. Check Missing Values
7. Clean Data
8. Exploratory Data Analysis
9. Feature Engineering
10. Data Preprocessing
11. Train-Test Split
12. Model Training
13. Model Evaluation
14. Feature Importance
15. Business Recommendations

---

## Data Preparation

The dataset was inspected and cleaned before modelling.

The main cleaning step involved handling blank values in the `TotalCharges` column and converting the column to an appropriate numerical data type.

Categorical variables were encoded using one-hot encoding, while numerical features were scaled before model training.

The dataset was then separated into features (`X`) and target (`y`) and divided into training and testing sets.

---

## Exploratory Data Analysis

EDA was performed to understand how churn varies across important customer characteristics, including:

- Contract type
- Tenure
- Internet service
- Payment method
- Customer charges and services

The EDA findings were used to better understand the dataset before applying machine learning models.

The visualizations generated during the analysis are available in the `Images/` folder.

---

## Machine Learning Models

Three classification models were trained and evaluated:

### 1. Logistic Regression

Used as a baseline classification model and provided the strongest overall performance in this project.

### 2. Decision Tree

Used to capture non-linear relationships and provide interpretable feature importance.

### 3. Random Forest

Used as an ensemble tree-based model to compare its performance against the simpler models.

---

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | **80.53%** | **65.15%** | 57.49% | **61.08%** |
| Decision Tree | 77.83% | 58.07% | **59.63%** | 58.84% |
| Random Forest | 78.82% | 62.34% | 51.34% | 56.31% |

### Model Comparison

Logistic Regression achieved the highest overall performance, with the highest accuracy, precision, and F1-score.

The Decision Tree achieved the highest recall, meaning it identified the largest proportion of actual churners among the three models.

Random Forest achieved lower recall and F1-score than the other two models in this experiment.

Based on the overall results, **Logistic Regression was selected as the strongest overall baseline model** for this dataset.

---

## Feature Importance

Feature importance was analyzed using the Decision Tree and Random Forest models.

The Decision Tree identified **Tenure** as its most influential feature, followed by **Fiber optic Internet Service** and **Total Charges**.

The Random Forest identified **Total Charges**, **Tenure**, and **Monthly Charges** as its top features.

Several features appeared as important across both tree-based models, including:

- Tenure
- Total Charges
- Monthly Charges
- Fiber optic Internet Service
- Electronic Check payment method
- Contract type

These features provide useful predictive information for identifying customer churn. However, feature importance represents predictive relationships and should not be interpreted as proof of causation.

---

## Business Recommendations

### 1. Strengthen Early Customer Retention

Focus proactive onboarding, engagement, and support efforts on newer customers, as tenure was one of the strongest predictive features.

### 2. Address Billing and Pricing Concerns

Review customers with relevant monthly-charge, total-charge, and payment patterns and provide personalized billing or plan support where appropriate.

### 3. Investigate Service and Contract Patterns

Investigate churn patterns across internet-service and contract segments and develop targeted retention strategies for customers showing higher predicted churn risk.

---

## Project Structure

```text
TELCO/
│
├── Data/
│   └── Telco Customer Churn dataset
│
├── Images/
│   ├── EDA visualizations
│   ├── Confusion matrices
│   └── Feature importance plots
│
├── Notebooks/
│   └── Telco_Churn_Prediction.ipynb
│
├── Outputs/
│   └── model_comparison.csv
│
├── Summary/
│   └── Telco_Churn_Findings_Summary.pdf
│
└── README.md