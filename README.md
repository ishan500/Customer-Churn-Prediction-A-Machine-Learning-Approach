Customer Churn Prediction: A Machine Learning Approach

This repository contains an end-to-end Machine Learning pipeline designed to predict customer churn and identify at-risk users before they leave. By leveraging customer demographics, behavioral metrics, and transactional data, this project helps businesses implement proactive, data-driven retention strategies to minimize revenue loss and optimize Customer Lifetime Value (CLV).

Problem Statement & Objectives
Customer Churn occurs when users discontinue their usage of a service or business application. In highly competitive sectors like E-commerce, Telecom, Banking, and SaaS, acquiring new customers is significantly more expensive than retaining existing ones.

Key Objectives:

Analyze Behavioral Data: Detect patterns, correlations, and key indicators closely tied to customer churn.

Perform Comprehensive EDA: Conduct univariate and bivariate analysis to extract actionable data insights.

Robust Data Preprocessing: Implement categorical encoding, feature scaling, and stratified splits.

Model Benchmarking: Build, tune, and evaluate multiple classification algorithms.

Business Application: Extract key business insights to reduce monthly churn rates.

Dataset Description
The project utilizes the Customer Churn Dataset sourced from Kaggle.

Total Records: ~65,000 Rows

Total Features: 12 Features

Target Distribution: Balanced Dataset (~53% Non-Churn vs. ~47% Churned)

Feature Dictionary:

CustomerID (Numerical): Unique identifier for each customer

Age (Numerical): Age of the customer

Gender (Categorical): Male or Female

Tenure (Numerical): Number of months the customer has stayed

Usage Frequency (Numerical): Number of times the service is used per month

Support Calls (Numerical): Total number of customer service interactions

Payment Delay (Numerical): Number of days payment has been delayed

Subscription Type (Categorical): Basic, Standard, or Premium tier

Contract Length (Categorical): Monthly, Quarterly, or Annual agreement

Total Spend (Numerical): Total monetary value spent by the customer

Last Interaction (Numerical): Days since the last active user engagement

Churn [Target] (Categorical): Binary indicator (1 = Churned, 0 = Retained)

Project Workflow & Pipelines

Exploratory Data Analysis & Feature Engineering

Checked for duplicate rows and verified that missing fields were completely cleaned and treated.

Categorical Encoding: Applied LabelEncoder to convert categorical text features (Gender, Subscription Type, Contract Length) into numeric matrices optimized for machine learning models.

Feature Scaling: Used StandardScaler to uniformize scales across different numerical columns (e.g., standardizing Total Spend alongside Support Calls).

Validation Split: Executed a structured train-test split using train_test_split to preserve model validation integrity.

Modeling & Evaluation Strategy
Four diverse traditional and ensemble classification algorithms were deployed and cross-compared to find the optimal boundary split:

Logistic Regression: Serves as the baseline linear classifier (highly interpretable).

Decision Tree: Captures hierarchical non-linear patterns through multi-depth splits.

Actionable Business Insights & Conclusions

Primary Churn Drivers: High counts of Support Calls and recurring Payment Delays surfaced as the strongest indicators of imminent customer churn.

Contract Structure Vulnerabilities: Contract structures heavily dictate retention rates. Monthly contract customers churn at nearly 2x the rate of users locked into Annual agreements. Transitioning users from monthly billing to annual subscriptions offers a direct path to reducing churn.

Strategic Impact: Integrating this model into user monitoring dashboards allows customer success teams to run automated, proactive retention campaigns (discounts, extended lifelines) targeted directly at flagged high-risk accounts.

Random Forest: An ensemble of decision trees engineered to reduce variance via bagging.

XGBoost: A gradient-boosted framework built to correct sequential tree errors iteratively.
