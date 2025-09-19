# 🩺 Diabetes Prediction Using Machine Learning

This project develops machine learning models to predict the likelihood of diabetes based on **medical and demographic data**.  
It follows the complete data science workflow from **EDA, preprocessing, model building, hyperparameter tuning, and evaluation**.

---

## 📊 Dataset

- **Source**: Kaggle – Diabetes Prediction Dataset  
- **Size**: ~100,000 patient records with 9 features  
- **Features**:
  - Gender, Age, BMI  
  - Hypertension, Heart Disease  
  - Smoking history  
  - HbA1c level  
  - Blood glucose level  
- **Target**: Diabetes status (1 = has diabetes, 0 = no diabetes)

---

## ⚙️ Project Workflow

1. **Exploratory Data Analysis (EDA)**  
   - Checked missing values, duplicates, and class distribution.  
   - Visualized feature distributions and correlations.  

2. **Data Preprocessing**  
   - Encoded categorical features.  
   - Scaled numerical variables.  
   - Handled class imbalance using **SMOTE** oversampling.  

3. **Modeling**  
   - Trained multiple classification models:
     - **K-Nearest Neighbors (KNN)**  
     - **Random Forest**  
   - Used **GridSearchCV** for hyperparameter tuning.  

4. **Evaluation**  
   - Evaluated models on Recall, Precision, F1-Score, and ROC-AUC.  
   - Selected the best model for deployment.  

---

## 📈 Results and Conclusion

- **Random Forest** outperformed KNN, offering the best balance of Recall and F1-score.  
- The most important predictors were:
  1. **HbA1c level**  
  2. **Blood glucose level**  
  3. **Age**  
- This model can support early diabetes detection and assist healthcare providers in screening patients at risk.  

**Future work**:
- Try deep learning models for comparison.  
- Deploy as an API or web app for clinical usage.
