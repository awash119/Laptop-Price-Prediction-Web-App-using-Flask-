# Laptop-Price-Prediction-Web-App-using-Flask-
Developed a web application for laptop price prediction using Flask.  Persisted the trained machine learning model with Pickle to enable efficient loading and inference.  Implemented a clean and intuitive user interface for users to input laptop specifications and receive real-time price predictions.
# Laptop Price Predictor

This project predicts laptop prices using machine learning. It is built in Python and uses regression models to estimate the price based on laptop features.

---

## Project Overview

- The goal is to predict laptop prices (`Price_euros`) based on features like brand, RAM, storage, processor, GPU, screen type, and weight.
- Dataset is cleaned, preprocessed, and features are engineered for better model performance.

---

## Dataset

- The dataset contains laptop specifications and prices.
- There are **no missing values**.
- Columns with units like `RAM (GB)` and `Weight (kg)` were converted to numeric.
- Low-frequency categories in features like `Company` were grouped into "Other".
- GPU, Processor, and OS columns were simplified for easier modeling.
- Screen features were consolidated into one column `Screen_Technology` (Touchscreen > IPS > HD > Other).

---

## Feature Engineering

- Created `Screen_Technology` feature from `ScreenResolution`.
- Extracted GPU manufacturer as `gpu_name`.
- Consolidated Operating System values into categories (`Windows`, `Mac`, `Linux`, `Other`).
- Grouped rare processor types under `Other`.
- One-hot encoding will be applied to categorical features before modeling.

---

## Machine Learning Models

- Models used for regression:
  - `LinearRegression`
  - `Lasso`
  - `DecisionTreeRegressor`
  - `RandomForestRegressor`
- Function `model_acc()` is used to train each model and print the score.
- `model.score()` is used to evaluate R² for regression models.

---

## Installation

1. Create a virtual environment (optional but recommended):
```bash
python -m venv env
