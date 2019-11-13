#Udacity Data Scientist Nanodegree Capstone Project
This repository has all the code and report for my Udacity Data Scientist Nanodegree Capstone project.

##Udacity Nanodegree Capstone Project: using customer data to predict advertisement engagement. 
###1. Installations
This project was written in Python, using Jupyter Notebook on Anaconda. The relevant Python packages for this project are as follows:

-pandas
-numpy
-sklearn.model_selection (train_test_split module)
-sklearn.preprocessing (StandardScaler, PolynomialFeatures)
-xgboost
-seaborn
-sklearn.metrics (mean_squared_error,classification_report)
-sklearn.linear_model (LogisticRegression)
-time
-sklearn.model_selection (GridSearchCV)
-matplotlib
###2. Project Motivation
This project is the Capstone project of my Data Scientist nanodegree with Udacity. As students of the program, I can analyze given data or find my own dataset. I was interested in looking at advertising data, because I find the subject interesting.


In this project, I use the data to answer 2 business questions:

a. What are the main drivers of an effective advertisement to predict customer engagement?
b. Could the data provided, predict whether one will interact with the an advertisment or not?

To answer the above 2 questions, I explored the dataset to uncover relationships numerous features that could help predict whether a customer will click an ad or not.

As a brief summary of my findings:

For Question 1, age of the user and the location of the user ended up not having a significant amount of influence on whether or not a user engages with an ad. It seemed tha time spent on the internet was the most important feature for predicting customer engagement.  

For Question 2,my decision to use 2 separate models to predict the effectiveness of each offer type ended up with good accuracy for both of the models (95% for XGBoost and 92% for LogisticRegression).

###3. File Descriptions
The report of my project is called 'Udacity Capstone - Predicting Customer Behaviour Through Advertising.ipynb'. The data used is advertising.csv

###4. Licensing, Authors, Acknowledgements, etc.
Data for coding project was provided by Kaggle!
