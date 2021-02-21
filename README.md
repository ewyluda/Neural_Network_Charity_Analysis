# Neural_Network_Charity_Analysis
Deep Learning Neural Networks (Week 19)

## Overview of the analysis: 
Using our knowledge of  machine learning and neural networks, we’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

Data was provided in .csv containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

The following steps will be taken:
  * first preprocess the data; includes (defining the target and features for our training set, droppping unnecessary columns, encoding categorical data using OneHotEncoder() method
  * split the preprocessed data into target and feature arrays
  * standardize the preprocessed data for training using StandardScaler()
  * Design a deep learning neural network model to analyze the data and find accuracy for determining if applicants funded by Alphabet Soup is successful.

Lastly we will optimize the model to increase accuracy and reach a target of 75% accurate.

## Results: 

### Data Preprocessing
#### What variable(s) are considered the target(s) for your model?
* targets = "IS_SUCCESSFUL"


#### What variable(s) are considered to be the features for your model?
* features = all other columns e.g. (AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT)
* 
#### What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME variables were determined to be neither targets, nor features and were dropped from the dataset.

### Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
Initially, we started with 2 hidden layers using "relu" activation funtions followed by one output function using "sigmoid". The first hidden layer had 80 neurons in our orginal model and the second hidden layer had 30 neurons.

To optimize the model, I changed the relu activation functions to tanh activation functions due to the negative values that were contained in our dataset, I figured that the tanh function would work best with those values.

I also increased epochs to 200, adjusted 'other' value cutoffs for binning APPLICATION_TYPE and CLASSIFICATION, changed them back because it made the model less accurate (tried increasing to 10000 and 2500 respectively), added 3rd layer, tried increasing hidden nodes to 100, 50 for two layers but it did not increase accuracy much.

### Were you able to achieve the target model performance?
No, I was not. The initial performance of the model was 70% accurate, I was able to achieve 73.5% accuracy with the changes I made above.

### What steps did you take to try and increase model performance?
*(from above):* To optimize the model, I changed the relu activation functions to tanh activation functions due to the negative values that were contained in our dataset, I figured that the tanh function would work best with those values.

I also increased epochs to 200, adjusted 'other' value cutoffs for binning APPLICATION_TYPE and CLASSIFICATION, changed them back because it made the model less accurate (tried increasing to 10000 and 2500 respectively), added 3rd layer, tried increasing hidden nodes to 100, 50 for two layers but it did not increase accuracy much.

