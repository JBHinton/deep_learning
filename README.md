### Deep_Learning_Challenge 
# Charity Funding Predictor

## Overview
### The goal of this project is to create an algorithm using machine learning and neural networks to predict whether applicants will be successful if funded by the fictional non-profit foundation, Alphabet Soup.
----------------------------
## Process

I was provided with a CSV file, which I imported into Pandas for data analysis. This file contained over 34,000 organizations that received funding from a fictional foundation, along with several metadata columns for each organization.

## Preprocessing:

I started by removing non-beneficial columns.
Next, I examined the distribution of data points for columns with more than 10 unique values, namely APPLICATION_TYPE and CLASSIFICATION.
For handling rare categorical values, I applied a cutoff point of 600 and 300, respectively, and grouped them into a new category labeled "Other."
Utilizing pd.get_dummies(), I converted categorical data into numerical format.
Following this, I divided the data into a target array (IS_SUCCESSFUL) and feature arrays.
To create a training and testing dataset, I employed the train_test_split method.
Finally, I standardized the training and testing sets using StandardScaler.
As a result, the data comprised 44 features, with the target variable (y) being IS_SUCCESSFUL. The dataset was split into training and test subsets.

## Model Compilation, Training, and Evaluation:

The objective was to achieve a predictive accuracy higher than 75%.
I conducted three official attempts using machine learning and neural networks.
Unfortunately, all attempts yielded a similar accuracy rate, ranging from 72.57% to 72.75%.
Despite not reaching the target accuracy of 75%, I am optimistic that with the addition of more layers, we can attain the desired 75% accuracy level.
Results from each model attempt:

ATTEMPT 1<br>
The first attempt (Models/AlphabetSoupCharity1.h5) resulted in an <b>accuracy score of 72.57%.</b> This means that 72.57% of the model’s predicted values align with the dataset’s true values.

The parameters used were:
* layers = 2
  * layer1 = 9 neurons : activation function = ‘relu’
  * layer2 = 18 neurons : activation function = ‘relu'
* epochs = 100

   

ATTEMPT 2<br>
For my second attempt (Models/AlphabetSoupCharity2.h5) I added another layer. This attempt resulted in an <b>accuracy score of 72.58%.</b> This means that 72.58% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
* layers = 3
  * layer1 = 9 neurons : activation function = ‘relu’
  * layer2 = 18 neurons : activation function = ‘relu’
  * layer3 = 27 neurons : activation function = ‘relu’
* epochs = 100


ATTEMPT 3<br>
For my third and final attempt (Resources/AlphabetSoupCharity3.h5) Iadded an additonal layer, and changed the activation functions. This attempt resulted in an <b>accuracy score of 72.75%.</b> This means that 72.75% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
* layers = 4
  * layer1 = 9 neurons : activation function = ‘relu’
  * layer2 = 18 neurons : activation function = ‘tanh’
  * layer3 = 27 neurons : activation function = ‘tanh’
  * layer4 = 36 neurons : activation function = ‘sigmoid’
* epochs = 100



## Summary
After three attempts, the model couldn't surpass 72.8% accuracy, even with hyperparameter tuning. It might be worth exploring a different classification model to improve predictions on whether applicants will succeed with funding from Alphabet Soup.
