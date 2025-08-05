# Seasonal Disease Prediction using Decision Tree Classifier

This project aims to build a machine learning model that predicts in which **season** (Spring, Summer, Autumn, Winter) a disease is most likely to occur, based on patient hospitalization data.

---

## Problem Statement

Given patient hospitalization records including admission dates and disease diagnosis, we seek to classify each record into one of the four seasons. This classification can help public health authorities to:

- Detect seasonal disease trends
- Plan timely healthcare responses
- Allocate resources efficiently

---

## Dataset Description

The dataset includes the following fields:

| Column Name        | Description                                         |
|--------------------|-----------------------------------------------------|
| ID                 | Unique patient identifier                           |
| NAMSINH            | Year of birth                                       |
| DANTOC             | Ethnicity                                           |
| TENPXA             | Ward name                                           |
| TENQUANHUYEN       | District name                                       |
| TENTINHTHANH       | Province/City name                                  |
| MAICD              | ICD disease code                                    |
| CHANDOAN           | Diagnosis description                               |
| NGAYVAO            | Hospital admission date                             |
| NGAYRA             | Discharge date                                      |
| TONGCP             | Total treatment cost                                |
| BHYT_TT            | Health insurance coverage amount                    |
| Thời gian điều trị | Duration of treatment in days (decimal precision)  |
| Unnamed columns    | Additional features or unused columns               |

---

## Project Workflow

1. **Data Cleaning**:
   - Handle missing or irrelevant columns
   - Convert admission date (`NGAYVAO`) to season category

2. **Feature Engineering**:
   - Encode categorical variables using `LabelEncoder`
   - Extract season from date

3. **Model Training**:
   - Model used: `DecisionTreeClassifier` from `sklearn`
   - Data split: `train_test_split` with a default 80/20 ratio

4. **Model Evaluation**:
   - Accuracy Score
   - Confusion Matrix
   - Precision, Recall, F1-Score
   - Classification Report

---

## Season Label Mapping

| Month | Season |
|-------|--------|
| 3–5   | Spring |
| 6–8   | Summer |
| 9–11  | Autumn |
| 12–2  | Winter |

---

## Evaluation Metrics

The model is evaluated using:

- `Accuracy Score`
- `Precision`, `Recall`, `F1-score`
- `Confusion Matrix` and `Classification Report`

---

## File Structure

- `seasonal-disease-prediction.ipynb`: Main Jupyter notebook containing all preprocessing, modeling, and evaluation steps.
- Input dataset: **(Path not provided)** — please specify the CSV or Excel input file manually inside the notebook.

---

## Requirements

Install dependencies with:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
