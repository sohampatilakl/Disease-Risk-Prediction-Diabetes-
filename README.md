# Diabetes Risk Prediction: Machine Learning & Smart Imputation

**Overview**
This project bridges the gap between complex clinical data and accessible at-home healthcare screening. It features a machine learning pipeline trained on comprehensive patient records to predict the likelihood of a diabetes diagnosis. The system optimizes for recall to minimize false negatives, ensuring high-risk patients are flagged for medical review.

## 🧠 Core Features & Engineering
* **Dual-Model Architecture:** Built and evaluated both Logistic Regression (baseline) and Random Forest Classifier algorithms.
* **Metric Optimization (Healthcare Focus):** In medical diagnostics, missed diagnoses (false negatives) carry severe consequences. The model’s decision threshold was mathematically tuned to prioritize **Recall and F1-score (82%)** over baseline accuracy.
* **Smart Default Imputation (UI Layer):** Engineered a public-facing screening interface that asks users for only 5 simple inputs (Age, Weight, Height, Family History, Blood Sugar). The system automatically calculates BMI and intelligently populates the remaining 20+ missing clinical features using population averages (medians/modes), allowing the complex 27-feature model to process basic user inputs seamlessly without crashing.

## 📊 The Dataset
The model is trained on a 5,200+ record dataset containing 27 diverse clinical and lifestyle parameters, including:
* **Vitals & Demographics:** Age, BMI, Resting Heart Rate, Blood Pressure.
* **Lifestyle Factors:** Diet, Physical Activity, Smoking Status, Stress Levels.
* **Clinical Lab Results:** Fasting Blood Sugar, HBA1C, C-Protein Levels, Glucose Tolerance.

## 📈 Key Findings
Feature importance analysis extracted from the Random Forest model validated the algorithm against known medical science. The model identified **Fasting Blood Sugar, BMI, and Age** as the most significant predictors of diabetes risk.

## 🛠️ Technologies Used
* **Python** (Core programming)
* **Pandas & NumPy** (Data manipulation, One-Hot Encoding, missing value imputation)
* **Scikit-Learn** (Model training, Feature Scaling via `StandardScaler`, Evaluation metrics)
* **Matplotlib & Seaborn** (Visualization of clinical feature importance)

## 🚀 How to Run
1. Clone the repository.
2. Ensure you have the required libraries installed: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Download the `diabetes_prediction_india (1).csv` dataset and place it in the root directory.
4. Run the Python script or Jupyter/Colab Notebook to train the model and launch the interactive at-home screener.
