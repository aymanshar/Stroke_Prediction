# Stroke Prediction Project

## Instructor: Hanna Abi Akl

## Program: Applied MSc in Data Analytics / Data Science & AI

Predicting stroke occurrence based on patient information such as age, hypertension, heart disease, BMI, and lifestyle
factors.

## Datasets Used

Two datasets were used one with few records and one with 40k record from kaggle:

1. **Original Dataset provided with the project(`stroke_data.csv`)**
   - imbalanced (only very few cases were positive strokes).
   - will apply balancing techniques (SMOTE).

2. **New Kaggle Dataset (`stroke_data_kaggle.csv`)**
    - More balanced (with more positive strokes).
    - Richer data.
   - https://www.kaggle.com/code/chanchal24/stroke-prediction-using-python/input?select=stroke_data.csv

Both datasets contain the following attributes:

- Patient demographics (gender, age, marital status, residence type).
- Health conditions (hypertension, heart disease, BMI, glucose level).
- Smoking status.

---

## Data Exploration Findings

Key findings after exploratory data analysis (EDA):

- **Age** is a strong predictor: Stroke risk increases significantly with age.
- Patients with **hypertension** or **heart disease** have a much higher stroke risk.
- **Smoking** is associated with increased stroke occurrence.
- **BMI** and **glucose levels** show moderate influence on stroke occurrence.
- **Gender** and **residence type** have minor effects.

The data correlation heatmaps and visual plots confirmed these relationships.

## Note:

In the new Kaggle dataset, stroke cases appear slightly more common among patients without diagnosed heart disease or
hypertension, which is different from the original dataset's pattern.

This could indicate sample bias, younger stroke cases, or incomplete health history documentation.


---

## Machine Learning Approach

### Feature Engineering

- Handled missing values (e.g., filled missing `bmi` with median in the original dataset).
- Encoded categorical features using one-hot encoding.
- Balanced the original dataset using **SMOTE** to solve the imbalance issue.

### Model Training

Three different models were used for the training:

- **Logistic Regression**
- **Random Forest Classifier**
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

2. required packages already in the requirements.txt
   - pandas
   - numpy
   - matplotlib
   - seaborn
   - scikit-learn
   - xgboost
   - imbalanced-learn
   ```bash
   ! pip install pandas
   ! pip install seaborn
   ! pip install xgboost
   ! pip install imbalanced-learn

3. Just run all cells
   