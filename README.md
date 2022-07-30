# Neural_Network
## Overview
Alphabet Soup is a buisness that provides funding for non-profit charities; Our task is to create a binary classifier that predicts whether an application will be successful or not. Using a dataset of 34,000 organizations train a neural network to create a linear combination of its most important features

### Purpose
Create a neural network capable of classifying successul Charity Startups using pythons' tensor flow libray

## Results

### Data Preprocessing
Our model predicts the IS_SUCCESSFUL column, using its [NAME,	APPLICATION_TYPE,	AFFILIATION,	CLASSIFICATION,	USE_CASE,	ORGANIZATION,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS,	ASK_AMT] columns as features. Before we can make this model we must first bin and encode any categorical data. The Name, Application Type and Classification columns were good candidates for binning since they have 19568, 17, and 71 categories respectively. The EIN should be dropped since this value is unique for each entry; Originally the name column was dropped, but it was discovered that many entries have the same name and it can influence the success of their charity. 

### Compiling, Training, and Evaluating the Model


How many neurons, layers, and activation functions did you select for your neural network model, and why?

Were you able to achieve the target model performance?

What steps did you take to try and increase model performance?


## Summary
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

There is a summary of the results (2 pt)
There is a recommendation on using a different model to solve the classification problem, and justification (3 pt)

### Further Improvement
We can handled this classification problems a couple of ways. Supervised Logistic regressions are limited because we would have to declare paired inputs and outputs, however this model has thousands of features. Unsupervised models would be helpful to cluster the charities, but it wouldn't necessarily help classify if they were successful or not.
