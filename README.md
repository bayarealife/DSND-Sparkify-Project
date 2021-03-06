# DSND-Sparkify-Project

Udacity Data Science Nano Degree Program Capstone Project - Sparkify Churn User Prediction Model with Big Data

## Project Overview
Preventing or reducing churn is very important for business success.  So I would like to train a machine learning model to predict churn users for a fictional music application created by Udacity.  The model is trained on the user event data provided by Udacity.

I have shared the results of my experiment in a blog published at this link: 

https://kyoko-desiderio.medium.com/sparkify-churn-user-prediction-model-with-pyspark-8ffa9eaad9f2


## Motivation
In this last project I wanted to take on a practical issue using Big Data.  This project requires churn prediction which is a very common and practical business issue.  The project also required the use of Spark, and AWS as an option - both very commonly used in any customer-facing business.  So I have chosen this project to gain the skills to learn the manipulation and feature engineering of large dataset, PySpark and AWS EMR.


## About This Repository
This repository is a container for the python script and data file.  It contains the following files.

DSND-Sparkify-Project

	|--Sparkify.ipynb -- Python Notebook script to analyze the data, train models using different algorithms and tune the best model. 
	
	|--mini_sparkify_event_data.json -- Sparkify user event data
	
	|--Sparkify.html -- HTML format output of Sparkify.ipynb
	
	|--README.md
	
	|--.gitattributes-- Configuration file or Git LFS


## About the Python Script
Library Requirement

	pandas==1.1.3
	
	pyspark==3.1.2
	
	matplotlib==3.3.1
	
	numpy==1.19.2
	
	seaborn==0.11.0

How To Run The Script
In order to run the script, download the files (keep the folder hierarchy as is) under Jupyter directory, open the script file in the Notebook, install the libraries specified above and run.


## Summary - Result of the Analysis
The data evaluation showed in most cases, the non-churn users were more active users (higher counts of events recorded).  The gender and the service level (free/paid) also showed difference in churn and non-churn users.  Then I removed features that were not relevant to user activities (i.e. Error page) and scaled them.
Then I have tried a few algorithms - Logistic Regression, Decision Tree, Random Forest.  
Linear SVC had high false positive rate.  Decision Tree had 0% true positive rate which is the most important prediction for this project.  Random Forest 18% true positive rate and 0% false positive rate after tuning and was the best model.


## Data Description
The data files are in json format.

	root
	
	 |-- artist: string (nullable = true)

	 |-- auth: string (nullable = true)

	 |-- firstName: string (nullable = true)

	 |-- gender: string (nullable = true)

	 |-- itemInSession: long (nullable = true)

	 |-- lastName: string (nullable = true)

	 |-- length: double (nullable = true)

	 |-- level: string (nullable = true)

	 |-- location: string (nullable = true)

	 |-- method: string (nullable = true)

	 |-- page: string (nullable = true)

	 |-- registration: long (nullable = true)

	 |-- sessionId: long (nullable = true)

	 |-- song: string (nullable = true)

	 |-- status: long (nullable = true)

	 |-- ts: long (nullable = true)

	 |-- userAgent: string (nullable = true)

	 |-- userId: string (nullable = true)


## Reference
https://spark.apache.org/docs/latest/ml-features
