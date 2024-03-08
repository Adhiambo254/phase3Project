![](image1.PNG)
# Customer Churn Prediction Project

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
The dataset comprises customer-related features such as account length, international plan, voice mail plan, and usage patterns. The target variable, "churn," indicates whether a customer has terminated services.

### Features
1. **Account Length:** Duration of the customer's account.
2. **International Plan:** Whether the customer has an international plan.
3. **Voice Mail Plan:** Whether the customer has a voice mail plan.
4. **Usage Patterns:** Total day, evening, night, and international usage minutes.
5. **Customer Service Calls:** Number of calls made to customer service.

### Target Variable
- **Churn:** Binary variable indicating whether a customer has terminated services (1 for churn, 0 for no churn).

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
