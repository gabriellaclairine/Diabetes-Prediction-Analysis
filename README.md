# 🩺 Diabetes Prediction Using Machine Learning

This project aims to build a machine learning classification model that can predict the likelihood of a person having diabetes based on their medical and demographic data. This notebook covers the entire data science workflow, from exploratory data analysis (EDA) and data cleaning to preprocessing, training, and evaluation of several classification models.



## 📊 Dataset

The dataset used is from Kaggle and contains 100,000 patient records with 9 features, including:
* **gender**: Patient's gender
* **age**: Patient's age
* **hypertension**: History of hypertension (1: yes, 0: no)
* **heart_disease**: History of heart disease (1: yes, 0: no)
* **smoking_history**: Patient's smoking history
* **bmi**: Body Mass Index
* **HbA1c_level**: HbA1c level (average blood sugar over the last 2-3 months)
* **blood_glucose_level**: Current blood glucose level
* **diabetes**: The target variable (1: has diabetes, 0: does not have diabetes)

---

## ⚙️ Project Workflow

1.  **Exploratory Data Analysis (EDA)**:
    * Checked data types, missing values, and duplicate records.
    * Analyzed the distribution of numerical data and handled outliers.
    * Visualized feature correlations using a heatmap.

2.  **Data Preprocessing**:
    * Cleaned inconsistent values in the `smoking_history` column.
    * Encoded categorical features (`gender`, `smoking_history`) using Label Encoding and One-Hot Encoding.
    * Handled the imbalanced class in the target variable using the **SMOTE** (Synthetic Minority Over-sampling Technique) oversampling method.
    * Scaled numerical features using `StandardScaler`.

3.  **Modeling and Evaluation**:
    * The dataset was split into training (80%) and testing (20%) sets.
    * Two classification models were trained and evaluated:
        1.  **K-Nearest Neighbors (KNN)**
        2.  **Random Forest**
    * **Hyperparameter tuning** was performed using `GridSearchCV` to find the best parameters for each model.
    * Models were evaluated based on **Recall**, **Precision**, **F1-Score**, and the **AUC-ROC Curve** to select the best-performing model.

---

## 📈 Results and Conclusion

Based on the evaluation, **Random Forest** was selected as the best model for diabetes diagnosis. It provided a superior balance across all evaluation metrics, especially **Recall** and **F1-Score**, which are critical for minimizing false negatives in a medical context.

The most influential features for predicting diabetes were:
1.  **HbA1c_level** (~36%)
2.  **blood_glucose_level** (~33%)
3.  **age** (~16%)
