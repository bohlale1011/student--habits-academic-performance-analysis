# Student Performance Prediction using Machine Learning

## Introduction
This project aims to analyze and predict student performance using machine learning techniques. The goal is to identify key factors influencing student outcomes and provide actionable insights to improve academic success. By combining data cleaning, visualization, predictive modeling, and interpretability methods, the project offers a complete data-driven workflow.

**Objectives:**
- Clean and preprocess student data for modeling.
- Explore relationships between features and outcomes using visualization.
- Train and evaluate predictive models (Decision Tree and Logistic Regression).
- Interpret model predictions using feature importance and SHAP analysis.
- Provide actionable insights for educators and administrators.

---

## Data Collection
The dataset was collected locally (`habits.csv`) and includes attributes such as:

- **Demographics:** age, gender, parent_education  
- **Academic metrics:** gpa, exam_score, study_hours, attendance  
- **Extra-curricular activities and resources:** extracurricular, internet_access  
- **Target variable:** Pass/Fail (0 = Fail, 1 = Pass)

---

## Data Preprocessing
**Steps Taken:**

1. **Missing Values Handling**  
   - Numerical missing values filled using mean (low skew) or median (high skew).  
   - Categorical missing values filled using mode.

2. **Encoding Categorical Variables**  
   - Low cardinality: One-Hot Encoding  
   - High cardinality: Label Encoding

3. **Feature Scaling**  
   - Standardized numerical columns using `StandardScaler` to ensure mean = 0 and SD = 1.

**Final Cleaned Dataset:**  
- Saved as `students_clean.csv`  
- No missing values; ready for modeling

---

## Exploratory Data Analysis (EDA)
**Visualization Techniques:**
- Scatter Plots (2D & 3D): Examined relationships between study hours, attendance, and exam scores.  
- Box & Violin Plots: Compared distributions of numerical features across pass/fail students.  
- Radar Charts: Compared performance profiles between lower- and higher-performing students.

**Key Insights:**
- Students with higher study hours and attendance generally perform better.  
- Features like study_hours, attendance, and exam_score strongly differentiate pass vs fail students.  
- Outliers and distribution patterns identified to guide feature preprocessing.

---

## Modeling
**Models Trained:**
1. **Decision Tree Classifier**  
   - Max depth = 5  
   - Captures non-linear relationships  

2. **Logistic Regression**  
   - Max iterations = 1000  
   - Captures linear relationships with interpretability

**Train-Test Split:**  
- 70% training, 30% testing  
- Stratified split to maintain class distribution

**Evaluation Metrics:**
- Accuracy  
- Confusion Matrix  
- Classification Report (precision, recall, F1-score)

---

## Feature Analysis
**Decision Tree Feature Importance:**  
- Top features influencing predictions: study_hours, attendance, exam_score, extracurricular activities  
- Visualized with horizontal bar charts

**Logistic Regression Coefficients:**  
- Positive coefficients: features increasing probability of passing  
- Negative coefficients: features associated with failure

**SHAP Analysis:**  
- Global and instance-level explanations  
- Confirmed most influential features across models  
- Force plots highlighted how individual feature values contributed to predictions

---

## Results Visualization
The project includes various visualizations to support analysis, including:
- Feature importance charts  
- Distribution plots  
- SHAP summary and force plots

---

## Conclusion
**Key Takeaways:**
- Study hours, attendance, and exam scores are the strongest predictors of student success.  
- Decision Tree and Logistic Regression models achieved high accuracy and complementary interpretability.  
- SHAP analysis enhanced understanding of feature impact, providing actionable insights.

**Recommendations:**
- Educators should monitor key features (study hours, attendance) to identify at-risk students early.  
- Targeted interventions can improve overall academic performance.  
- Workflow can be extended with additional datasets and advanced models for better prediction.

---

## Dataset
- Local CSV: `habits.csv`  
- Cleaned CSV: `students_clean.csv`

---

## Technologies & Libraries
- Python 3.x  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn, plotly  
- shap (SHAP analysis)  

---


