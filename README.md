# Lessons Learnt
___
## Introduction
In this repository you will find several projects that did not produce the expected results. This is where I learnt valuable lessons on “doing” data science. This is where I tried to understand how various types of regression worked or did not work. They are all failures,  but I keep them as a reminder of what went wrong and why. Some projects shown here are sometimes incomplete as I realised it was not going to work

In this repository I also keep templates which are based on sound lessons that I found on the Internet. Most times I followed the lesson sometimes using a different dataset other times same dataset. I used these examples to learn how to do a particular project correctly and understand the process. These templates are always referenced with the source website.
___

# Project 1: Poisson NB2 Bike NYC – BOTH
___

Notebook: 01_Failure_Poission_NB2_Bike_NYC – BOTH
___
#### About the project
Poisson regression model for regressing the bicyclist counts observed on the Brooklyn bridge between 01 April 2017 and 31 October 2017.  
Source: https://timeseriesreasoning.com/contents/poisson-regression-model/  
The project starts with the Poisson regression model and use it as the “control” for the Negative Binomial regression model in part 2 of this project. Cameron and Trivedi recommend best practice is to estimate both Poisson and Negative Binomial regression models (Cameron and Trivedi, 2013).  
  
#### Project outcome: failure but a lesson well learnt.
The problem with this project is that I attempted to do everything in a single notebook which did not work as I seemed to get the same results for the Poisson regression and the Negative Binomial Regression Model. When I did the two models in two separate notebooks then I was able to replicate the results correctly.

I keep this project as a reminder that there are **no shortcuts**

#### Explore Project 1: 
___

# Project 2: Startup Success - Unbalanced response variable (Failed project)
___

Notebook: 02_Failure_StartUp_Success_Unbalanced_Failure
___
#### About the project
The purpose of this project is to predict if a new startup business will succeed. The predictors are 'Total_Funding', 'funding_rounds', 'months_2_first_fund' and 'Unfunded'. The response is Succeed or Fail.

### Data Source
Business Start up dataset source information

URL: https://www.kaggle.com/datasets/ankurzing/success-of-startup

The dataset cleaned and processed dataset contains 66,057 records and 5 fields

#### Project outcome: failure but a lesson well learnt.
The project was a failure because I ignored the imbalanced in the Success/failure ration in the response variable. I will complete the project but this time working from the source cited below to resolve the problem

The Success response variable is imbalanced (90% sucess and 10% failure) but it is important to preserve that imbalance as it informs the model of the likelihood of a startup succeeding or failing.
Source: https://medium.com/towards-data-science/weighted-logistic-regression-for-imbalanced-dataset-9a5cd88e68b

#### Model Results
**Accuracy Score:** 0.90608

**Confusion Matrix: **
	0    :   1860
  0	   :  17945

**Area Under Curve:** 0.5

**Recall score:** 1.0

This is a useless result as it is not predicting failure because the response variable is unbalanced, and this was not weighted in the modelling. 
A valuable lesson that was well learnt.  

#### Explore Project 2: 
___
