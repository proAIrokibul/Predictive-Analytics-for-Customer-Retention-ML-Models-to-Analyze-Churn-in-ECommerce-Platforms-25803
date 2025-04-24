# Predictive-Analytics-for-Customer-Retention-ML-Models-to-Analyze-Churn-in-ECommerce-Platforms-25803
## Project Overview

This project focuses on building **machine learning models** to analyze customer churn and enhance retention strategies for **eCommerce platforms**. The goal is to identify customers who are at risk of leaving and develop predictive models to mitigate churn, ultimately helping businesses increase customer lifetime value and improve user satisfaction.

The dataset includes various customer features such as demographics, transaction history, satisfaction scores, and usage patterns, with the target variable being whether a customer churned (1) or stayed (0).

## Problem Statement

Customer churn is one of the most critical issues for eCommerce businesses as retaining existing customers is more cost-effective than acquiring new ones. Identifying churn early allows businesses to act proactively, offering promotions or personalized services to retain high-value customers.

### Columns in Dataset:
- `CustomerID`: Unique identifier for the customer.
- `Churn`: Target variable indicating whether the customer churned.
- `Tenure`, `Gender`, `CityTier`, `PreferredPaymentMode`: Customer demographics and behaviors.
- `SatisfactionScore`, `Complain`, `CouponUsed`: Engagement and interaction metrics.
- `OrderAmountHikeFromLastYear`, `DaySinceLastOrder`: Transactional data that helps to assess customer activity and loyalty.

## Methodology

### Data Preprocessing
The data is preprocessed by:
1. **Handling missing values** with appropriate imputation strategies.
2. **Feature scaling** of numerical columns using **StandardScaler**.
3. **Encoding categorical variables** using **OneHotEncoder**.
4. Splitting the dataset into **train** and **test** sets (75% / 25%).

### Models Used:
We evaluated and fine-tuned the following models for churn prediction:
1. **Logistic Regression** – A baseline model to establish initial accuracy and understand the relationship between features and churn.
2. **Random Forest** – An ensemble learning model to capture complex patterns in data with feature importance.
3. **XGBoost** – A high-performance model based on gradient boosting that aims to reduce overfitting and handle imbalanced data.

### Hyperparameter Tuning
For each model, **GridSearchCV** was used to tune hyperparameters to improve model performance, including parameters such as:
- **Logistic Regression**: Regularization strength (`C`) and solvers.
- **Random Forest**: Number of estimators, max depth, and minimum samples per split.
- **XGBoost**: Learning rate, max depth, and number of estimators.

### Performance Evaluation
We evaluated models using the following metrics:
- **Accuracy**: Overall correctness of the model.
- **Precision**: Ability to identify positive churn correctly.
- **Recall**: Sensitivity in detecting churn cases.
- **F1-Score**: Balance between Precision and Recall, especially for imbalanced classes.

### Model Comparison
Three models were trained, and their performance was compared. The evaluation results highlighted key differences in how each model handles the churn prediction task:

- **Logistic Regression**: Strong performance with a simpler decision boundary.
- **Random Forest**: Excellent ability to capture nonlinear patterns and provide feature importance.
- **XGBoost**: Top-tier model with optimal performance due to gradient boosting and overfitting control.

## Business Impact

The insights derived from this analysis can significantly impact eCommerce businesses in the following ways:

1. **Proactive Retention Strategies**: By predicting which customers are most likely to churn, businesses can develop targeted marketing campaigns or offer incentives to retain valuable customers, thus improving customer retention rates.
2. **Customer Segmentation**: Understanding the factors that lead to churn helps businesses segment customers by risk level, tailoring interventions for high-risk customers.
3. **Cost Reduction**: Identifying at-risk customers early enables businesses to minimize churn-related costs by offering personalized incentives rather than spending heavily on customer acquisition.
4. **Improved Customer Lifetime Value (CLTV)**: Reducing churn and increasing retention leads to higher CLTV, which directly contributes to long-term business profitability.
5. **Informed Decision-Making**: The feature importance insights can guide business leaders in making data-driven decisions regarding product offerings, pricing strategies, and customer service enhancements.

## Conclusion

This project demonstrates the power of **machine learning** in predicting customer churn and providing actionable insights for business growth. By deploying these models, eCommerce platforms can reduce churn, enhance customer retention, and increase overall profitability. The combination of advanced techniques like **Random Forest** and **XGBoost** ensures high predictive accuracy, even with complex and noisy data.


---

## Model Results

### 📘 Logistic Regression Results
          precision    recall  f1-score   support

       0       0.89      0.98      0.93      1171
       1       0.76      0.38      0.51       237

    accuracy                           0.88      1408
    macro avg  0.83       0.68       0.72      1408 
    weighted avg 0.87     0.88       0.86      1408

    Accuracy: 0.8764204545454546



### 🌲 Random Forest Results
          precision    recall  f1-score   support

       0       0.97      0.99      0.98      1171
       1       0.95      0.86      0.90       237

    accuracy                        0.97      1408
    macro avg 0.96       0.92       0.94      1408 
    weighted avg 0.97    0.97       0.97      1408
    Accuracy: 0.9680397727272727


    
### 🚀 XGBoost Results

          precision    recall  f1-score   support

       0       0.99      0.99      0.99      1171
       1       0.96      0.94      0.95       237

    accuracy                       0.98      1408
    macro avg   0.97     0.97      0.97      1408 
    weighted avg 0.98    0.98      0.98      1408

    Accuracy: 0.9836647727272727



    
