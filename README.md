# 🔋 Battery State of Health (SOH) Prediction using Machine Learning

##  Project Overview

This project predicts the **State of Health (SOH)** of lithium-ion batteries using Machine Learning techniques. Battery SOH is an important indicator of battery performance and remaining capacity. Accurate SOH prediction helps improve battery maintenance, reliability, and lifespan in electric vehicles (EVs) and energy storage systems.

---

##  Problem Statement

The objective of this project is to develop a machine learning model that predicts the **State of Health (SOH)** of a battery based on its operating conditions.

---

##  Dataset

The dataset contains battery operating parameters collected during charge-discharge cycles.

### Features

- Cycle
- Voltage
- Temperature
- Capacity

### Target

- State of Health (SOH)

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook

---

##  Project Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Data Preprocessing
4. Feature Engineering
5. Train-Test Split
6. Model Training
7. Model Evaluation
8. Cross Validation
9. Hyperparameter Tuning
10. Feature Importance Analysis
11. Model Saving
12. New Battery SOH Prediction

---

##  Machine Learning Models Used

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

---

##  Model Performance

| Model | MAE | RMSE | R² Score |
|-------|------:|------:|------:|
| Linear Regression | 0.0534 | 0.0725 | 0.6221 |
| Decision Tree | 0.0103 | 0.0254 | 0.9537 |
| Random Forest | 0.0083 | 0.0190 | 0.9742 |
| Gradient Boosting | 0.0177 | 0.0274 | 0.9460 |
| XGBoost | 0.0173 | 0.0265 | 0.9496 |
| **Random Forest (Tuned)** | **0.0082** | **0.0187** | **0.9749** |

---

##  Best Model

The **Random Forest Regressor** achieved the best performance after hyperparameter tuning.

### Best Hyperparameters

- n_estimators = 200
- max_depth = None
- min_samples_split = 2
- min_samples_leaf = 1

### Performance

- MAE: **0.0082**
- RMSE: **0.0187**
- R² Score: **0.9749**

---

##  Feature Importance

The model identified the following feature importance:

| Feature | Importance |
|----------|-----------:|
| Capacity | 0.6066 |
| Cycle | 0.1755 |
| Temperature | 0.1294 |
| Voltage | 0.0885 |

Battery **capacity** was the most influential feature for predicting SOH.

---

##  Cross Validation

Both standard Cross Validation and **GroupKFold Cross Validation** were performed.

GroupKFold was used to avoid data leakage caused by multiple observations from the same battery, resulting in a more realistic estimate of model performance.

---

##  Model Deployment

The trained model was saved using **Joblib** and later loaded to predict the SOH of new battery samples.

---

##  Future Improvements

- Collect a larger battery dataset.
- Include additional battery parameters such as SOC and internal resistance.
- Develop a Battery Remaining Useful Life (RUL) prediction model.
- Explore deep learning models such as LSTM and GRU.
- Deploy the model using Streamlit or FastAPI.

---

##  Repository Structure

```
battery-soh-prediction/
│
├── README.md
├── requirements.txt
├── battery_soh_prediction.ipynb
├── battery_soh_model.pkl
├── battery_soh.csv
├── images/
└── LICENSE
```

---

##  Author

**Omkar Kavathekar**

Electrical Engineering Student | Machine Learning Enthusiast

---

## ⭐ Acknowledgements

This project was developed for learning and demonstrating the application of Machine Learning techniques in battery health monitoring for electric vehicle and energy storage applications.
