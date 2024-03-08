
# Customer Churn Prediction 
![image](https://github.com/Adhiambo254/phase3Project/assets/125627822/99b4f7c2-40df-4e44-9111-7257c517e4aa)

## Overview

This project focuses on predicting customer churn for SyriaTel, a telecommunications company, utilizing machine learning techniques. The project involves data exploration, preprocessing, feature engineering, modeling, and evaluation to develop an accurate predictive model.

## Table of Contents

- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Hypothesis Testing](#hypothesis-testing)
- [Further Investigation](#further-investigation)
- [Getting Started](#getting-started)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Reproducibility](#reproducibility)
- [Contributing](#contributing)
- [License](#license)

## Business Understanding

### Stakeholder Audience
The primary stakeholders are SyriaTel's decision-makers, aiming to reduce customer churn for increased profitability and customer satisfaction. Understanding customer behavior and predicting churn is crucial for implementing effective retention strategies.

### Objectives
1. Identify patterns leading to customer churn.
2. Develop a predictive model for early identification of at-risk customers.
3. Inform data-driven retention strategies to minimize churn.

### Key Metrics
- **Churn Rate:** Percentage of customers who have terminated services.
- **Customer Lifetime Value (CLV):** Predict the value a customer brings over their entire relationship with SyriaTel.
- **Retention Cost:** The cost associated with retaining a customer compared to acquiring a new one.

## Data Understanding

### Dataset
The dataset was obtained from [KAGGLE](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/data) and it comprises of the following columns:

1. **State:** State in which the customer resides.
2. **Account Length:** Duration of the customer's account.
3. **Area Code:** Area code of the customer's phone number.
4. **Phone Number:** Unique identifier for each customer's phone number.
5. **International Plan:** Whether the customer has an international plan.
6. **Voice Mail Plan:** Whether the customer has a voice mail plan.
7. **Number of Voicemail Messages:** Count of voicemail messages.
8. **Total Day Minutes:** Total minutes of usage during the day.
9. **Total Day Calls:** Total number of calls made during the day.
10. **Total Day Charge:** Total charge for day usage.
11. **Total Evening Minutes:** Total minutes of usage during the evening.
12. **Total Evening Calls:** Total number of calls made during the evening.
13. **Total Evening Charge:** Total charge for evening usage.
14. **Total Night Minutes:** Total minutes of usage during the night.
15. **Total Night Calls:** Total number of calls made during the night.
16. **Total Night Charge:** Total charge for night usage.
17. **Total International Minutes:** Total minutes of international usage.
18. **Total International Calls:** Total number of international calls made.
19. **Total International Charge:** Total charge for international usage.
20. **Customer Service Calls:** Number of calls made to customer service.
21. **Churn:** Binary variable indicating whether a customer has terminated services (1 for churn, 0 for no churn).

### Features
1. Categorical features: State, Area Code, International Plan, Voice Mail Plan.
2. Numeric features: Account Length, Number of Voicemail Messages, Total Day Minutes, Total Day Calls, Total Day Charge, Total Evening Minutes, Total Evening Calls, Total Evening Charge, Total Night Minutes, Total Night Calls, Total Night Charge, Total International Minutes, Total International Calls, Total International Charge, Customer Service Calls.

## Feature Engineering

### New Features
New features were created to enhance predictive power:
1. **Total Charges per Day:** Sum of day, evening, night, and international charges.
2. **Ratio of Total Day Minutes to Total Night Minutes:** A derived ratio capturing usage patterns.


## Modeling

### Models Built
1. **Simple Baseline Model:**
   - Algorithm: Random Forest with default parameters.
   - Performance: Accuracy ~94.6%.

2. **More-Complex Model:**
   - Algorithm: Random Forest with specific hyperparameters (100 estimators, max depth of 10).
   - Performance: Accuracy ~94.9%.

3. **Hyperparameter-Tuned Model:**
   - Algorithm: Random Forest with tuned hyperparameters (max depth=None, n_estimators=50).
   - Performance: Similar to the baseline model.

## Evaluation

### Simple Baseline Model Evaluation
- Accuracy: ~94.6%
- Precision, Recall, and F1-score analyzed for each class.

### More-Complex Model Evaluation
- Accuracy: ~94.9%
- Improved recall for Class 1.

### Hyperparameter-Tuned Model Evaluation
- Best Hyperparameters: {'max_depth': None, 'n_estimators': 50}.
- Performance similar to the baseline model.

## Hypothesis Testing

A hypothesis test assessed the significance of average total day minutes in predicting customer churn. The result, a t-statistic of 12.10 with a p-value close to zero, indicates a significant difference in average total day minutes between churn and no churn customers.

## Further Investigation

Further investigation involves exploring the relationship between total day minutes and churn in the context of other variables. Visualizations include histograms, boxplots, and correlation matrices. The insights gained from these visualizations can inform business strategies and model refinements.

## Getting Started

To get started with the project, follow these steps:

1. Clone the repository.
2. Install the necessary dependencies (see [Dependencies](#dependencies)).
3. Explore the Jupyter notebooks and scripts for data analysis, modeling, and evaluation.

## Dependencies

Ensure you have the following dependencies installed:

- Python 3.x
- Jupyter Notebooks
- scikit-learn
- seaborn
- matplotlib

Install dependencies using:

```bash
pip install -r requirements.txt
