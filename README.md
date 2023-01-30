# 📈 linear_regression_industry_finance 💰

A prediction of the following months income presented by developing a linear regression model, deployed on a time series dataset of financial transactions.

[![Made With](https://github.com/Denneya/linear_regression_industry_finance/blob/main/made-with-r.svg)](https://github.com/Denneya/linear_regression_industry_finance/blob/main/AT1A_24418042.R)

Author: Denneya Muscat

## Table of Contents

* [Overview](#Overview)
* [Dataset](#Dataset)
* [Model](#Model)
* [Results](#Results)

## Overview 📄
This was the first assignment for Machine Learning and Algorithims. It was a rather complicated task in terms of coding due to the nature of the dataset. There were 10 industries and 10 locations, with transactions for each month from January 2013 to November 2016. The task was to predict the total income for December 2016. EDA was performed identifying positive skewness in the monthly amounts and industries, as well as displaying a seasonal trend with peaks towards the end of each month. It was also important to notice majority of the dataset was for Industry 6 and Location 1 as well as Industry 4 and Location 10 having minimal values, which would impact the regression model. 

The dataset was aggregated using the `date`, `industry` and `location` columns with the mean monthly amount. The dataset was then split into training and test sets according to date. A simple linear regression model was produced for Industry 1 and Location 1 and then looped over each combination. 

## Dataset 📁
The dataset can be found [here](https://github.com/Denneya/linear_regression_industry_finance/blob/main/transactions.csv)

The data dictionary below identifies all variables and their data type.

|Field|Data Type|Description|
|---|---|---|
|date|Date|Date of the first day of each month|
|customer_id|String|Unique customer identifier|
|industry|Integer|Code for 10 industries, ranging from 1 to 10|
|location|Integer|Code for 10 locations, ranging from 1 to 10|
|monthly_amount|Numeric|Total transaction amount for customer in given month|

### Data Preparation 
The dataset was prepared by doing the following:
* Applying a log transformation due to the skewness of the data. 
* Search for any duplicate values.
* Search for any missing values.

## Model
After aggregating and splitting the dataset, dummy variables had to be created to accomodate for seasonality. The linear regression model was then built and the performance was checked before looping over all industries and locations. Next, a prediction dataset was created for December 2016. The predicted results were then put into this dataset. 

## Results 🕵🏼
The following results were obtained after the linear regression model was looped over all combinations of industry and location:
* Multiple R-Squared value of 0.816.
* Mean Squared Error of 0.00007396645, confirming the model used for prediction fit training data well. 
* Model performed worse for industry 6, location 1 and industry 8, location 1 due to the limited values mentioned above. 
* Model didn't perform as well on the test set, MSE of 0.0001970025, which is larger than the MSE for the training set. 

Lastly, the table below shows a preview of the December 2016 predictions for all Industries and Locations. 
![Table of results](https://github.com/Denneya/linear_regression_industry_finance/blob/main/Screenshot%202023-01-30%20at%2012.17.55%20pm.png)

## Final Comments 💤
Hopefully you made it to this point. As mentioned earlier, this was my first ever linear regression model. If you have any comments or feedback, feel free to reach out!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/denneyamuscat)[![INSTAGRAM](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/denneyam/)
