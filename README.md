# Overview of the analysis

The purpose of the analysis was to utilize the provided dataset (csv with >34K organizations) to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  

To do this, we created a neural network model and then attempted to optimize the model to increase performance.  

# Results

## Data Preprocessing

What variable(s) are considered the target(s) for your model?

-	IS_SUCCESSFUL

What variable(s) are considered to be the features for your model?

-	APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT 

What variable(s) are neither targets nor features, and should be removed from the input data?

-	EIN, NAME

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
-	See details regarding neurons, layers and activations functions below. 

Were you able to achieve the target model performance?
-	No, I was not able to achieve the target model performance of >75%. 

What steps did you take to try and increase model performance?
-	Attempt 1 : Increase epochs from 50 to 100.  

-	Attempt 2 : Adjust number of hidden nodes. Hidden nodes layer 1 : 80  80.  Hidden nodes layer 1 : 30  50

-	Attempt 3 : Change model from ReLU to sigmoid. 

-	Attempt 4 : Change model from ReLU to Leaky ReLU  

-	Attempt 5 : Remove noisy variables from the features, specifically “SPECIAL_CONSIDERATIONS”.  This feature is a binary feature with options of “yes” or “no”.  The frequency of “yes” within the dataset was considerably small.  

-	Attempt 6 : Added additional hidden layer, specifically hidden layer three (hidden_nodes_layer3 = 20).

# Summary

## Results

Below are the results of the deep learning model.  Despite 4 attempts to increase performance of the model, the model did not yield an accuracy of > 75%.  

Attempt 1 yielded a model with an accuracy of 72.64% and a loss of 0.5531.

Attempt 2 yielded a model with an accuracy of 72.67% and a loss of 0.5526.

Attempt 3 yielded a model with an accuracy of 72.79% and a loss of 0.5501.

Attempt 4 yielded a model with an accuracy of 72.72% and a loss of 0.5509.

Attempt 5 yielded a model with an accuracy of 72.64% and a loss of 0.5536.

Attempt 6 yielded a model with an accuracy of 72.68% and a loss of 0.5538.

## Recommendations

I recommend using a random forest model for the purpose of this analysis.  The random forest model combines multiple smaller models into a more accurate and robust model.  
