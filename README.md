# Diabetes Prediction Using Logistic Regression

Predictive Analytics project, Section D.
**Student:** Anvay Sachin Sanil (2427030150)

## About
This project predicts whether a patient has diabetes from basic medical measurements
(glucose, BMI, blood pressure, insulin, age, number of pregnancies, and more) using a
**Logistic Regression** classifier (supervised learning, binary classification).

**Key result:** the model reaches 71% accuracy and a ROC-AUC of 0.81 on unseen patients, with glucose level as the strongest predictor.

## Dataset
[Pima Indians Diabetes Database (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database).
768 patients, 8 features, target `Outcome` (1 = diabetes, 0 = no diabetes).
A copy is included in [`data/diabetes.csv`](data/diabetes.csv).

## Steps
1. Load and explore the data
2. Clean impossible zero values (Glucose, BloodPressure, SkinThickness, Insulin, BMI) by replacing them with training-set medians
3. Exploratory data analysis: histograms, correlation heatmap, box plots
4. Stratified 80/20 train-test split and feature scaling
5. Train a Logistic Regression model
6. Evaluate with accuracy, precision, recall, F1, confusion matrix and ROC-AUC
7. Read feature importance from the coefficients and odds ratios
8. Predict for a new patient

## Results (test set, 154 patients)
| Metric | Value |
|---|---|
| Accuracy | 0.71 |
| ROC-AUC | 0.81 |
| Recall (diabetes) | 0.50 |
| Precision (diabetes) | 0.60 |

Strongest predictors: **Glucose** (odds ratio ≈ 3.3 per standard deviation), **BMI** (≈ 2.0) and **Pregnancies** (≈ 1.5).

## How to run
```bash
pip install -r requirements.txt
jupyter notebook diabetes_prediction.ipynb
```
Or open the notebook in Google Colab and upload `data/diabetes.csv`.

## Files
| File | Description |
|---|---|
| `diabetes_prediction.ipynb` | Full analysis notebook |
| `data/diabetes.csv` | Dataset |
| `requirements.txt` | Python dependencies |
