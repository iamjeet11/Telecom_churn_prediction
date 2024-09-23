# Telecom_churn_prediction

## Overview
This project aims to predict customer churn for a telecom company using machine learning models. By identifying high-risk churn customers, the company can take preemptive action (such as offering special plans or discounts) to retain them. The project also identifies key variables contributing to churn, providing valuable business insights.

The dataset consists of customer-level information, including voice call usage, data usage, recharge patterns, and other factors, recorded over four months. The task is to predict whether a customer will churn in the last month based on their behavior in the first three months.

## Dataset
The dataset includes customer information recorded over four months (June, July, August, and September). The goal is to predict churn in September based on the first three months of data. The dataset contains the following key features:

MOBILE_NUMBER: Unique customer identifier
CIRCLE_ID: Telecom circle area to which the customer belongs
ARPU: Average revenue per user
MOU: Minutes of usage (calls)
DATA: Mobile internet usage volume
RECH: Recharge amounts and counts
AON: Age on network (number of days the customer is with the operator)
Various other features related to calls, data usage, and recharge patterns
The columns ending with _6, _7, _8, _9 represent data from June, July, August, and September, respectively.

## Target Variable:
Churn: A binary variable where 1 indicates the customer has churned in September, and 0 indicates they have not.
Data Preparation
The following data preparation steps were applied:

Filter High-Value Customers: High-value customers were defined as those who had a recharge amount greater than or equal to the 70th percentile of the average recharge in the first two months (June and July).
Tag Churners: Customers who had no outgoing or incoming calls, and no mobile internet usage in September, were tagged as churners (churn=1).
Remove Churn Phase Attributes: All data related to September (the churn phase) was removed before modeling, as the goal is to predict churn without using September data.
Feature Scaling: Continuous variables were scaled for models that are sensitive to feature magnitudes.
