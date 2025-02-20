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
[Link to Project 1 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/01_Failure_Poission_NB2_Bike_NYC%20-%20BOTH.ipynb)

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
**Confusion Matrix:**  
0    :   1860  
0    :  17945  
**Area Under Curve:** 0.5  
**Recall score:** 1.0  
This is a useless result as it is not predicting failure because the response variable is unbalanced, and this was not weighted in the modelling.    
A valuable lesson that was well learnt.   

#### Explore Project 2:
[Link to Project 2 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/02_Failure_StartUp_Success_Unbalanced_Failure.ipynb)
___
# Project 3: Vehicle Linear Regression (Failed)
___

Notebook: 03_Failure_Vehicle_Linear_Regression_Failed
___
#### About the project
This notebook uses a historical dataset to build a linear regression model that predicts Co2 emissions based on highway mpg, city mpg and engine displacement

#### Project outcome: 
The mean absolute error implies that the predictions for this model to have an average variance of between +-23.7 in co2 emissions and a model test score of 90%.  
**HOWEVER despite the good indicators this model is fundamentally flawed.**  
At the extremes this linear model does not work because that there is NOT a liner relationship between fuel consumption measured in miles per gallon and Co2 emissions.  
The model must be built using a different technique or be adjusted to account for the curvature in the relationship between fuel consumption and Co2 emissions.   
Refer to Project 4 titled 'Vehicle Polynomial Regression Attempt 2 Improved,' which features an enhanced model utilizing a different algorithm, specifically Polynomial Regression.   

#### Explore Project 3:
[Link to Project 3 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/03_Failure_Vehicle_Linear_Regression_Failed.ipynb)
____

# Project 4: Vehicle Polynomial Regression Attempt 2 Improved
___

Notebook: 04_Failure_Vehicle_Polynomial_Regression_Attempt_2_Improved
____
#### About the project
This notebook uses a historical dataset to build a linear regression model that predicts Co2 emissions based on city mpg.

#### Project outcome: 
Result Test1: Medium 14 mpg city - predicts 562.75 under reporting by 1.33%  
Result Test 2: High 40 mpg city - predicts 193.64 under reporting by 11.55%  
Result Test 3: Low 7 mpg city - predicts 1006.78 under reporting by 8.95%  
**Statistical tests**  
Mean squared error: 618.79  
R-squared: 0.96 (96%)  
  
The model has improved but may lack sufficient predictor variables.

#### Explore Project 4:
[Link to Project 4 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/04_Failure_Vehicle_Polynomial_Regression_Attempt_2_Improved.ipynb)
____
# Project 5: k-means clustering (Template)
___

Notebook: Template_01_k-means clustering
___
#### About the project
This project is adapted from the notebook of the LinkedIn Learning course indicated below: Source (Frederick Nwanganga):https://www.linkedin.com/learning/machine-learning-with-python-k-means-clustering
Use k-means clustering to segment retail card customers based on their income and an assigned spending score.

#### Project outcome: 
**Cluster 0:** older (mostly women), earn and spend less than the other clusters.  
**Cluster 1:** slightly younger than cluster 0, slightly more men, earn the most and spend the least.  
**Cluster 2:** younger but not the youngest,slightly more women who earn well (2nd highest earners) and spend the most.  
**Cluster 3:** youngest (more women) who earn the least and are second highest spenders.  
**Cluster 4:** oldest (mostly women), who are in the middle in terms of earning and spending habits.  

#### Explore Project 5:
[Link to Project 5 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/Template_01_k-means%20clustering.ipynb)
___
# Project 6: Vehicles Power OLS Engine Displacement (Template)
___

Notebook: Template_02_Vehicles_Power_OLS_EngineDisplacement
___
#### About the project
This project is adapted from Source:https://timeseriesreasoning.com/contents/dummy-variables-in-a-regression-model/  
This notebook uses a historical dataset to build a linear regression model that predicts Co2 emissions based on number of cylinders in the engine.  

#### Project outcome: 
The estimated means CO2 emissions of 3, 4, 6, 8, 10, 12 and 16-cylinder engines are all highly significant.  
The 5-cylinder engine is the only exception which appears to be less significant than all the other engines.  
The 16 cylinder engine with their estimated mean emissions of 869.3888 is nearly double the emissions of a 2 cylinder engine.  
From the analysis above it is clear that engine CO2 emissions do not change by a constant amount with each unit change in the number of cylinders. This vindicates the initial decision not to represent the number of cylinders as a simple integer-valued variable.

#### Explore Project 6:
[Link to Project 6 Notebook](https://github.com/andrewcollodel/Lessons-learnt/blob/main/Template_02_Vehicles_Power_OLS_EngineDisplacement.ipynb)
___
