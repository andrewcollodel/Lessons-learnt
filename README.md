# Lessons Learnt
___
## Introduction
In this repository are projects that did not yield the anticipated results. These projects provided invaluable lessons in the practical application of data science. Through these endeavors, I sought to comprehend the functionality and limitations of various models. Although these projects were unsuccessful, I retain them as reminders of the errors and their underlying causes. Some projects may appear incomplete, as I discontinued them upon realizing the models were ineffective.

Additionally, I maintain templates derived from reliable lessons found online. Often, I adapted these lessons to align with my approach, occasionally utilizing different datasets. These examples facilitated my understanding of how to execute specific projects correctly and grasp the underlying processes. All templates are duly referenced with their source websites.
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
The objective of this project is to predict the success of a new startup business. The predictors include 'Total_Funding', 'funding_rounds', 'months_2_first_fund', and 'Unfunded'. The response variable is binary, indicating either Success or Failure.

### Data Source
Business Start up dataset source information

URL: https://www.kaggle.com/datasets/ankurzing/success-of-startup

The dataset cleaned and processed dataset contains 66,057 records and 5 fields

#### Project outcome: failure but a lesson well learnt.
The initial attempt at this project was unsuccessful due to the oversight of the imbalance in the Success/Failure ratio within the response variable. I intend to revisit and complete the project, addressing this issue by following the correct methodology.

The Success response variable is imbalanced, with 90% indicating success and 10% indicating failure. It is crucial to maintain this imbalance as it provides the model with essential information regarding the likelihood of a startup succeeding or failing but the response variable must be correctly weighted something I neglected to do.
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
