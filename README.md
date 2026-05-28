# Time_series_Forecasting
Machine learning pipeline for cinema audience forecasting  built on the Kaggle Cinema Audience Forecasting Challenge.

--

## 🏗️ Project Overview

Predicting how many people will visit a cinema on a given day is a critical challenge for theater operators — helping them plan staffing, inventory and scheduling.This project builds an end-to-end forecasting pipeline using real booking and visit data from multiple theater sources, combining exploratory analysis,feature engineering and machine learning to predict daily audience counts.


### 🤖 Models Used

| Model | Notes |
|-------|-------|
| **XGBoost** | Poisson objective, 1000 estimators |
| **Random Forest** | 500 estimators with imputation pipeline |
| **LightGBM** | Poisson objective, 1000 estimators |
| **XGBoost (Tuned)** | RandomizedSearchCV, 20 iterations |

### 📈 Evaluation Metric
- R² Score (coefficient of determination)
- Train/test split: pre-2024 for training, 2024 onwards for testing

---

## 📁 Dataset Description

| File | Description |
|------|-------------|
| `booknow_visits.csv` | Daily audience count per theater (target variable) |
| `booknow_booking.csv` | Online ticket bookings with show and booking datetime |
| `cinePOS_booking.csv` | Offline/POS ticket sales data |
| `booknow_theaters.csv` | Theater metadata — type, area, ID |
| `cinePOS_theaters.csv` | POS-side theater metadata |
| `movie_theater_id_relation.csv` | Mapping between booking and POS theater IDs |
| `date_info.csv` | Date-level metadata |
| `sample_submission.csv` | Submission format template |

---

## 🛠️ Tech Stack

- **Python** — core language
- **Pandas & NumPy** — data processing
- **Seaborn & Matplotlib** — visualisation
- **Scikit-learn** — pipelines, imputation, RandomizedSearchCV, PCA, KMeans
- **XGBoost** — gradient boosting
- **LightGBM** — gradient boosting (fast, memory efficient)
- **Kaggle** — competition platform and compute environment

---


*Built for the Kaggle Cinema Audience Forecasting Challenge.*
