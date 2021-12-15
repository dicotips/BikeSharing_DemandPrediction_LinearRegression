# Bike Sharing Demand Prediction - Linear Regression

## Introduction 

In this programming assignment I built a multiple linear regression model to predict the demand of bikes by **BoomBikes**.
This repository contains the following files required by the assignment:

* Jupyter Notebook file with the Data Preparation and Model Building to predict the demand of bikes.
* PDF File with answers to the Subjective Questions.

## Contact:
* Jheser Guzman (@dicotips) - feel free to contact me!
### Methods Used
* Data Preparation
* Model Building

### Technologies
* Python
* Pandas
* SkitLearn
* Jupyter Notebooks

## Download and Setup
### Prerequisites

This project needs Anaconda installed in the computer.

For more details about the instalation, go to:  https://docs.anaconda.com/anaconda/install/index.html
### How to Run

You can download the source code cloning this repository using Git:

1. Open your favorite Terminal app (Unix, Linux or Macos), such as Terminal, Command, Console, iTerm2, so on.

2. Clone the repository

```
git clone https://github.com/dicotips/BikeSharing_DemandPrediction_LinearRegression
```

3. Open the ** *.ipynb** notebooy file in Anaconda.

```
jupyter notebook LinearRegressionAssignment.ipynb
```

## Problem Statement

**Source:** UpGrad Assignment description

*A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.*

*A US bike-sharing provider **BoomBikes** has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.*

*In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.*

*They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:*

* Which variables are significant in predicting the demand for shared bikes.
* How well those variables describe the bike demands

*Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.*

### Business Goal:

*You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.*

### Data Preparation:

1. *You can observe in the dataset that some of the variables like **'weathersit'** and **'season'** have values as 1, 2, 3, 4 which have specific labels associated with them (as can be seen in the data dictionary). These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case (Check the data dictionary and think why). So, it is advisable to convert such feature values into categorical string values before proceeding with model building. Please refer the data dictionary to get a better understanding of all the independent variables.*
 
2. *You might notice the column **'yr'** with two values 0 and 1 indicating the years 2018 and 2019 respectively. At the first instinct, you might think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. So think twice before dropping it.*

### Model Building

*In the dataset provided, you will notice that there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. **The model should be built taking this 'cnt' as the target variable.***

### Model Evaluation

*When you're done with model building and residual analysis and have made predictions on the test set, just make sure you use the following two lines of code to calculate the R-squared score on the test set.*
 
```
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```

* *where y_test is the test data set for the target variable, and **y_pred** is the variable containing the predicted values of the target variable on the test set. Please don't forget to perform this step as the R-squared score on the test set holds some marks. The variable names inside the 'r2_score' function can be different based on the variable names you have chosen.*

* *Please don't forget to perform this step as the R-squared score on the test set holds some marks. The variable names inside the 'r2_score' function can be different based on the variable names you have chosen.*

## Conclusions

* cnt is dependent on temp.
* cnt is highly correlated with yr as well.
* Number of bikes shared in 2019 increased from 2018.
* There is Negative correlation of Light Snow, Spring and windspeed.
* Weather conditions affect the bike sharing when it is snowy, or rainy. Same effect when windspeed is high.
