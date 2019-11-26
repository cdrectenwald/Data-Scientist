# Sparkify
## Udacity Data Science Nanodegree Capstone Project

## Overview
One of the most important metrics for subscription based services is member churn. Understanding why members choose to leave your service and taking steps to prevent that exodus, can be the difference between a successful and a failing business model. Using the fictional company “Sparkify”, we will explore the concept of churn and attempt to build a functional model for identifying users at risk for it.

An accompanying Medium article can be found here: https://medium.com/@cdrectenwald/predicting-customer-churn-58faa29bc836

## Findings
We are able to generate a highly predictable model using a time-series based definition of churn and structuring our data accordingly. Rolling windows on pertinent page actions allow us to identify short-term trends that might be predictive of churn. Due to the highly skewed nature of the target variable, utilizing an ensemble-based classifier such as gradient boost may yield the best results. We can use a parameter grid and cross validation to find the ideal hyper-parameters for our problem.

Tuning our model to emphasize positive predictive value allows us to derive the most utility from its output. In the case of churn, false negatives have a significantly higher cost than false positives. Emphasizing recall (true-positive rate) as a metric allows us to minimize the the number of users to whom we failed to predict a churn.

## Refinements and Next Steps

I would like to try to incorporate data streaming into this application. Time is everything in a business, and I believe data streaming would allow the business to identify churned users in a quicker and cheaper fashion.

Additional feature engineering — Maybe I could have brought in addtional data about a user such as their demographics or interests to help better identify their likelihood of churning.

I also would have been able to look at more models and compare their performance such as some neural network, logistic regression, or a random forest classifier. I'm a fan of xgboost, but I don't think Apache Spark has a package yet. 

## Tools Used
IBM Watson Studio
Apache Spark / Spark MLlib
Python
Scikit-Learn
Pandas
Matplotlib
Seaborn
## Contents
DSND Sparkify.ipynb - Jupyter notebook employing pyspark to perform exploratory data analysis, metric definition, feature engineering, modeling, and model evaluation on the Sparkify data set.
References
Barranka. “PySpark: Get Threshold (Cuttoff) Values for Each Point in ROC Curve.” Stack Overflow, 1 July 1969, stackoverflow.com/questions/54425084/pyspark-get-threshold-cuttoff-values-for-each-point-in-roc-curve.

“Gradient Boosting.” Wikipedia, Wikimedia Foundation, 30 May 2019, en.wikipedia.org/wiki/Gradient_boosting.

Patel, Neil. “How to Improve Your Subscription Based Business by Predicting Churn.” Neil Patel, 24 May 2019, neilpatel.com/blog/improve-by-predicting-churn/.

“Receiver Operating Characteristic.” Wikipedia, Wikimedia Foundation, 11 July 2019, en.wikipedia.org/wiki/Receiver_operating_characteristic.

Safdari, Nasir. “Build an End-to-End Machine Learning Model with MLlib in PySpark.” Medium, Towards Data Science, 13 Feb. 2019, towardsdatascience.com/build-an-end-to-end-machine-learning-model-with-mllib-in-pyspark-4917bdf289c5.

Tausend, F. “Hands-on: Predict Customer Churn.” Medium, Towards Data Science, 1 June 2019, towardsdatascience.com/hands-on-predict-customer-churn-5c2a42806266.
