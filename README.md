# Stroke Prediction Project

# Instructor: Hanna Abi Akl

# Program: Applied MSc in Data Analytics / Data Science & AI

Predicting stroke occurrence based on patient information such as age, hypertension, heart disease, BMI, and lifestyle
factors.

## Datasets Used

Two datasets were used to build and compare different models:

1. **Original Dataset provided with the project(`stroke_data.csv`)**
    - Highly imbalanced (only very few cases were positive strokes).
    - Required balancing techniques (used SMOTE applied).

2. **New Kaggle Dataset (`stroke_data_kaggle.csv`)**
    - More balanced (with more positive strokes).
    - Richer data.

Both datasets contain the following attributes:

- Patient demographics (gender, age, marital status, residence type).
- Health conditions (hypertension, heart disease, BMI, glucose level).
- Smoking status.

---

## Data Exploration Findings

Key findings after exploratory data analysis (EDA):

- **Age** is a strong predictor: Stroke risk increases significantly with age.
- Patients with **hypertension** or **heart disease** have a much higher stroke risk.
- **Smoking history** is associated with increased stroke incidence.
- **BMI** and **glucose levels** show moderate influence on stroke occurrence.
- **Gender** and **residence type** have minor effects.

The data correlation heatmaps and visual plots confirmed these relationships.

---

## Machine Learning Approach

### Feature Engineering

- Dropped irrelevant columns (`id`).
- Handled missing values (e.g., filled missing `bmi` with median).
- Encoded categorical features using one-hot encoding.
- Balanced the old dataset using **SMOTE** to correct class imbalance.

### Model Training

Three different models were trained and compared:

- **Logistic Regression**: Baseline model.
- **Random Forest Classifier**: handles non-linearities.
- **XGBoost Classifier**: best performance.

### Model Evaluation

Evaluation metrics used:

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

**Best model:**  
In both versions, **XGBoost** achieved the highest recall and overall balanced performance.

**Important features identified:**  
Age, hypertension, heart disease, average glucose level, smoking status.

---

## How to Run

1. Install required packages:
   ```bash
   pip install -r requirements.txt
   