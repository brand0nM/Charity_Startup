# Charity Startup
## Overview
Alphabet Soup is a business that provides funding for non-profit charities; Our task is to create a binary classifier that predicts whether an application will be successful or not

### Purpose
Train a neural network to classify successful Charity Startups with pythons' tensor flow library

## Results
### Data Preprocessing
Our model predicts the IS_SUCCESSFUL column, using its [NAME,	APPLICATION_TYPE,	AFFILIATION,	CLASSIFICATION,	USE_CASE,	ORGANIZATION,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS,	ASK_AMT] columns as features. Before we can make this model we must first bin and encode all categorical data. The Name, Application Type, and Classification columns were good candidates for binning since they have 19568, 17, and 71 categories respectively. The EIN should be dropped since this value is unique for each entry; Originally the name column was dropped, but it was discovered that many entries have the same name and it can influence the success of their charity

### Compiling, Training, and Evaluating the Model

<img width="528" alt="Screen Shot 2022-07-30 at 11 16 29 AM" src="https://user-images.githubusercontent.com/79609464/181934503-6f764f92-1046-4368-a187-248b862439c2.png"><br/>

Three hidden layers of cascading neuron amounts were chosen to model this data. The first two hidden layers have activation functions relu then tanh; these were chosen after evaluating the models' loss and accuracy against similar functions like linear and sigmoid. The third hidden layer doesn't add much dimensionally- since it uses the same relu activation function; however, it does reduce the number of important features and subsequently the amount of noise in the model. This model was able to achieve an accuracy of 79.25% with a loss of 44.65%; we were able to get an overfitted model with 80.2% accuracy, however, the loss was greater than 1. The biggest factor in this model's accuracy was how you choose to bin categorical data<br /><br/>
<img width="445" alt="Screen Shot 2022-07-30 at 11 15 13 AM" src="https://user-images.githubusercontent.com/79609464/181934465-58879c40-73f8-467d-91b3-8b9d9261bc16.png">

## Summary
Using Tensorflows' library we created a successful-charity neural network classifier with an accuracy of 79.25%, but there are a couple of ways to handle this problem. Supervised Logistic regressions are limited because we would have to declare paired inputs and outputs, however, this model has thousands of features. Unsupervised models would be helpful to cluster charities, but it wouldn't necessarily help classify if they were successful or not; We could force the KMeans algorithm to fit 2 clusters, however, this process would most likely miss classifying data- since we can not assume the ideal number of clusters is 2. To create a more accurate model we could use unsupervised learning to determine the data's principle components, then pass these components through a Logistic Classifier; This would avoid overfitting the data to less important components like the neural network may have done
