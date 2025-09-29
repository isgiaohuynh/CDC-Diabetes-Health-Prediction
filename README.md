# CDC Diabetes Health Indicators 🩺

## 📖 Overview
This project is part of the **Statistical Data Processing** course, focusing on analyzing the **CDC Diabetes Health Indicators (BRFSS 2015)** dataset.  
The dataset contains **253,680 survey responses** with **21 health and demographic variables**, aiming to predict the risk of **diabetes**:  
- `0`: Non-diabetes  
- `1`: Pre-diabetes  
- `2`: Diabetes  

The project explores data preprocessing, statistical testing, handling imbalanced data, and building predictive models to support early diagnosis and lifestyle recommendations.

---

## Objectives
- Explore relationships between health indicators and diabetes status.  
- Perform **A/B testing** to validate hypotheses.  
- Handle class imbalance in the dataset.  
- Build machine learning models to predict diabetes risk.  
- Provide insights and recommendations for diabetes prevention and management.  

---

## Dataset
- Source: **CDC BRFSS 2015 Survey** (`diabetes_012_health_indicators_BRFSS2015.csv`).  
- **Target variable**: `diabetes_012` (3 classes).  
- **Features**: 21 variables including: `diabetes_012`, `high_bp`, `high_chol`, `chol_check`,`bmi`,`smoker`,`stroke`,`heart_disorderor_attack`,`phys_activity`,`fruits`,`veggies`, etc
- **Issue**: 
      Highly imbalanced data (Non-diabetes: 213,703 vs Pre-diabetes: 4,631 vs Diabetes: 35,346).
      Except for `bmi`, `men_hlth`, `phys_hlth`, other are quantitative variables

---

## ⚙️ Methodology
1. **Preprocessing**  
   - Cleaning duplicates, renaming variables.  
   - Classifying quantitative vs qualitative features.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualization: histograms, boxplots, density plots.  
   - Correlation analysis.
   - Detail in html file

3. **Statistical Testing (A/B Testing)**  
   - Resampling methods for categorical variables.  
   - Permutation ANOVA for continuous variables.  

4. **Handling Imbalanced Data**  
   - Under-sampling, Over-sampling, SMOTE, Class Weights.
     <img width="939" height="616" alt="image" src="https://github.com/user-attachments/assets/802ce27e-3b21-4317-a09e-829adc6f4b7c" />
   - Chosen approach: **Combination of Under-sampling + SMOTE**.  

5. **Modeling**  
   - **Multiclass classification**: Logistic Regression, Random Forest, Naive Bayes.  
   - **Binary classification**: Logistic Regression, Random Forest, Naive Bayes.  
   - Evaluation metrics: Accuracy, Kappa, Macro-F1, ROC-AUC.  

---

## 💡Results
- **Best Multiclass Model**: Random Forest  
  <img width="897" height="441" alt="image" src="https://github.com/user-attachments/assets/5780c258-e073-46c0-8c24-d5b718ef0c6c" />
- **Best Binary Model**: 
  <img width="884" height="1066" alt="image" src="https://github.com/user-attachments/assets/6f742026-7972-445c-b2ee-a6eba4f5d4e1" />
  Logistic Regression has AUC = 0.81, which indicates that the model's ability to distinguish between classes is quite good and reliable.
- **Top predictive features**:  
  - General health, high blood pressure, BMI, difficulty walking, cholesterol, age, heart disease, physical health, income, education.  

---

## ✅ Conclusion
- Diabetes risk is strongly linked to lifestyle, age, education, and income.  
- Random Forest performs best for multiclass classification.  
- Logistic Regression is reliable for binary classification.  
- Public health strategies should focus on early screening, lifestyle changes, and improving healthcare access for vulnerable groups.  

---

## 👥 Contributors
- Trương Bình Ba  
- Chiêm Huỳnh Giao  
- Nguyễn Ngọc Bảo Hân  
- Nguyễn Thị Xuân Hương  
- Phan Thị Ngọc Linh  
- Hồ Trần Anh Thư  

