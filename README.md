# 🏦 Loan Approval Prediction

## 📋 Project Overview
This project aims to predict loan approval status using machine learning techniques. The objective is to build models that can accurately classify whether a loan application will be approved or rejected based on applicant data, with a focus on handling class imbalance.

## 🎯 Goals
- Preprocess and clean the loan approval dataset.
- Address class imbalance using SMOTE.
- Train and evaluate multiple models (Logistic Regression, Decision Tree).
- Compare model performance using precision, recall, and F1 score.

## 🛠️ Requirements
- **Dataset:** Loan Approval Prediction Dataset (downloaded via kagglehub)
- **Python Libraries:**
  - pandas
  - numpy
  - scikit-learn
  - imbalanced-learn
  - seaborn
  - matplotlib

## 🚦 Stages

1. **Data Preparation** 🧹
   - Loaded dataset from Kaggle.
   - Cleaned missing values.
   - Encoded categorical features using label encoding.
   - Explored feature correlations and visualized distributions.

2. **Model Training** 🤖
   - Split data into training and test sets.
   - Trained Logistic Regression and Decision Tree models.
   - Applied SMOTE to balance the training data and retrained models.

3. **Evaluation** 📊
   - Evaluated models using precision, recall, and F1 score.
   - Compared performance before and after SMOTE resampling.

## 🏁 Results

| Model                       | Precision | Recall | F1 Score |
|-----------------------------|-----------|--------|----------|
| Logistic Regression         |    0.896   |  0.918  |   0.907   |
| Logistic Regression + SMOTE |    0.896   |  0.991  |   0.941   |
| Decision Tree               |    0.899  |  0.956  |   0.927   |
| Decision Tree + SMOTE       |    0.901   |  0.978  |   0.938  |


## 💬 Discussion
The model was trained to predict loan approval based on the applicant's cibil score, as it showed a significant correlation with loan status. The results show that applying SMOTE significantly improved recall and F1 score for both models, especially for the minority class. Logistic Regression and Decision Tree models performed well, but Decision Tree + SMOTE achieved the highest F1 score (0.938). SMOTE resampling led to more balanced predictions, reducing bias toward the majority class. Overall, addressing class imbalance with SMOTE enhanced the models' ability to correctly identify rejected loan applications, demonstrating the effectiveness of resampling in classification tasks.
---

**To run the project:**  
Install the required libraries and download the dataset using kagglehub.  
Run the notebook in `Loan Approval Prediction.ipynb` to reproduce the results.