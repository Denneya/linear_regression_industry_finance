# 📈 linear_regression_industry_finance 💰

A prediction of the following months income presented by developing a linear regression model, deployed on a time series dataset of financial transactions.

[![Made With](https://github.com/Denneya/linear_regression_industry_finance/blob/main/made-with-r.svg)](https://github.com/Denneya/linear_regression_industry_finance/blob/main/AT1A_24418042.R)

Author: Denneya Muscat

## Table of Contents

* [Overview](#Overview)
* [Dataset](#Dataset)
* [Visuals](#Visuals)
* [Findings](#Findings)

## Overview 📄
This was the first assignment for Machine Learning and Algorithims. It was a rather complicated task in terms of coding due to the nature of the dataset. There were 10 industries and 10 locations, with transactions for each month from January 2013 to November 2016. The task was to predict the total income for December 2016. EDA was performed identifying positive skewness in the monthly amounts and industries, as well as displaying a seasonal trend with peaks towards the end of each month. It was also important to notice majority of the dataset was for Industry 6 and Location 1 as well as Industry 4 and Location 10 having minimal values, which would impact the regression model. 

The dataset was aggregated using the `date`, `industry` and `location` columns with the mean monthly amount. The dataset was then split into training and test sets according to date. A simple linear regression model was produced for Industry 1 and Location 1 and then looped over each combination. 

## Dataset 
The dataset can be found [here](https://github.com/Denneya/linear_regression_industry_finance/blob/main/transactions.csv)

The data dictionary below identifies all variables and their data type.

|Field|Data Type|Description|
|---|---|---|
|date|Date|Date of the first day of each month|
|customer_id|String|Unique customer identifier|
|industry|Integer|Code for 10 industries, ranging from 1 to 10|
|location|Integer|Code for 10 locations, ranging from 1 to 10|
|monthly_amount|Numeric|Total transaction amount for customer in given month|
