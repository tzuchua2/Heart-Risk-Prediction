# Heart Disease Risk Prediction Project

This project aims to predict the risk of heart disease (binary classification) using supervised learning models. It includes data preprocessing, exploratory data analysis (EDA), and training multiple models, including Logistic Regression, K-Nearest Neighbors (KNN), Random Forest, XGBoost, and a Neural Network.

## Dataset

The dataset contains 15 predictor variables, which can be categorized as variables that inform whether or not a symptom has occurred and variables about the patient's risk factors. Only the 'Age' variable is continuous and all others are binary. The target variable we are predicting is 'High Risk', which informs whether or not a patient should be classified as high heart risk. The dataset contains 7000 rows and was generated using NumPy and Pandas, aiming to create an absolute balance between classes.

## Training

During training, there are two training sets. One for scaled 'Age', specifically used for the two baseline models and the neural network. 

## Metrics

Models are evaluated by the F1 score and Auc-Roc. F1 was chosen because I think both precision and recall are crucial in medical diagnostics. Despite this dataset being extremely balanced, F1 was useful in balancing precision and recall here. Auc-Roc was chosen simply because various different models were used, and it can be useful for model comparisons.

## Model Performance Summary

The following table presents the F1 Score and ROC-AUC results for each model:

| Model              | F1 Score | ROC-AUC |
|-------------------|----------|---------|
| **Logistic Regression** | 0.9911  | 0.9995  |
| **K-Nearest Neighbors (KNN)** | 0.9918  | 0.9993  |
| **Random Forest** | 0.9920  | 0.9995  |
| **XGBoost** | **0.9939**  | **0.9997**  |
| **Neural Network** | Accuracy: 0.9908 | N/A |

## Conclusion 

XGBoost is the best choice because it achieves the highest F1 Score (0.9939) and ROC-AUC (0.9997), indicating both strong classification performance and excellent class separation. However, this project is mainly for practicing and all models perform pretty well, so it doesn't make a big difference in this case. Due to efficiency and speed, logistic regression may be chosen in practice.
