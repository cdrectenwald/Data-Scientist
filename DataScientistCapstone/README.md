# Sparkify
## Udacity Data Science Nanodegree Capstone Project

## Overview
One of the most important metrics for subscription based services is member churn. Understanding why members choose to leave your service and taking steps to prevent that exodus, can be the difference between a successful and a failing business model. Using the fictional company “Sparkify”, we will explore the concept of churn and attempt to build a functional model for identifying users at risk for it. First I will explore the data to find insights related to a user's subscription age, operating systems and devices, gender, and activeness on the application to name a few features that I think will be critical to prediciting customer churn. From there, I aim to create a pipeline of these features to feed into a supervised learning  boost tree classification algorithm. I am attracted to this algorithm due to its ability to recalculate the weighted inputs, which are useful when dealing with imbalanced data.


A Medium article can be found here: https://medium.com/@cdrectenwald/predicting-customer-churn-58faa29bc836

## Findings
I was able to create a highly predictable model. I used a time-series analysis such as rolling windows on pertinent page actions allow us to identify short-term trends that might be predictive of churn. However, there is a large skewness to the data of representation of churned vs not churned representation. Going forward, I would like to under sample or over sample the data to achieve better representation, although it seems that many classifiers already perform that function. 

Tuning our model to emphasize positive predictive value allows us to derive the most utility from its output. In the case of churn, false negatives have a significantly higher cost than false positives. Emphasizing recall (true-positive rate) as a metric allows us to minimize the the number of users to whom we failed to predict a churn.


## Refinements and Next Steps

I would like to try to incorporate data streaming into this application. Time is everything in a business, and I believe data streaming would allow the business to identify churned users in a quicker and cheaper fashion.

Additional feature engineering — Maybe I could have brought in addtional data about a user such as their demographics or interests to help better identify their likelihood of churning.

I also would have been able to look at more models and compare their performance such as some neural network, logistic regression, or a random forest classifier. I'm a fan of xgboost, but I don't think Apache Spark has a package yet. 

## Tools Used
-IBM Watson Studio
-Apache Spark / Spark MLlib
=Python
-Scikit-Learn
-Pandas
-Matplotlib
-Seaborn
## Contents
Data Scientist- Cr0566.ipynb- Jupyter notebook employing pyspark to perform exploratory data analysis, metric definition, feature engineering, modeling, and model evaluation on the Sparkify data set.


