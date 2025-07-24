# Comparing-Different-Regression-Techniques-With-Pipeline
# 🎓 Student Marks Regression Project

Predicting student exam marks based on **study time** and **number of enrolled courses** using multiple machine learning models — with a clean `scikit-learn` Pipeline and automatic PDF reporting.

---

## 📊 **Project Overview**

This project builds and compares **Linear Regression**, **Decision Tree Regression**, **Support Vector Regression (SVR)**, and **Polynomial Regression** (degrees 1–7) to model how students’ study habits impact their exam scores.

The goal is to:
- Compare different models
- Check for overfitting/underfitting
- Find the best model based on **Train/Test R²**, **Adjusted R²**, **RMSE**, **RSS**, and **AIC**
- Automate all results & plots into a single PDF report

---

## 🗂️ **Dataset**

- **Source:** `Student_Marks.csv`  
- **Features:**
  - `number_courses` — Number of courses a student enrolled in.
  - `time_study` — Hours spent studying.
  - `Marks` — Final exam score (target).

---

## ⚙️ **Why use `scikit-learn` Pipelines?**

✅ **Cleaner workflows:** Chains preprocessing (like polynomial features & scaling) with model training in **one reusable object**.  
✅ **Prevents leakage:** Ensures transformations use only training data.  
✅ **Easy tuning:** Works seamlessly with `GridSearchCV` for hyperparameter search.  
✅ **Production-ready:** Same pipeline can be saved & re-used on new data.

---

## 🗒️ **Benefits of Automated PDF Reporting**

Instead of scattered plots & results, this project uses **`fpdf`** to save **all evaluation plots** and **key metrics** in a single PDF:
- Makes sharing results easy.
- Keeps documentation tidy.
- Useful for academic reports, client handover, or presentations.

---

## 📏 **Evaluation Metrics**

Each model is evaluated on:
- **R² Score:** Explains variance in marks.
- **Adjusted R²:** Penalizes extra features.
- **RMSE (Root Mean Squared Error):** Average prediction error.
- **RSS (Residual Sum of Squares):** Total prediction error.
- **AIC (Akaike Information Criterion):** Rewards good fit with fewer parameters.

Together, they show how **well the model fits**, whether it **overfits**, and how it **generalizes**.

---

## 🔍 **Key Insights**

- **Polynomial Regression (degree 3)** achieved the best balance, with **Test R² ≈ 0.92**, showing the real relationship is slightly **non-linear**.
- **Linear Regression** also performed well (**Test R² ≈ 0.86**) but underfits subtle curves.
- **Decision Tree** gave high Train R² but lower Test R², showing mild overfitting.
- **SVR** needed scaling and showed competitive performance.
