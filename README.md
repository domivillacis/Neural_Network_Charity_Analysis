# Neural Network Charity Analysis

## Overview of the loan prediction risk analysis:

In this project I'm going to help Alphabet Soup, a non-profit foundation that helps organisations that protect the environment and improve the well-being of people around the world. Over the past 20 years, Alphabet Soup has donated more than $10 billion to a variety of causes and the company's President recently asked the analytics team to help predict which organisations are worth donating to to ensure the money of the foundation is used effectively.

We're going to create and train a deep learning neural network that will evaluate the input data and allow us to interpret a large and complex dataset. To create and test these models we'll use the python TensorFlow library. 

The results will help us making a final decision on which organisations should receive donations from Alphabet Soup.

## Results:

### Data Preprocessing

- What variable(s) are considered the target(s) for your model? 

The variable considered the target is: IS_SUCCESSFUL

- What variable(s) are considered to be the features for your model? 

The variables that are the features of our model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

![Alt text](../../Screenshot%202023-02-13%20at%2000.38.42.png)

- What variable(s) are neither targets nor features, and should be removed from the input data?

The variables that were not considered relevant for our first model are: EIN and NAME. 

However, to optimise the model in order to achieve a target predictive accuracy higher than 75%, we decided to remove 2 more irrelevant features: ORGANIZATION and SPECIAL_CONSIDERATIONS

![Alt text](../../Screenshot%202023-02-13%20at%2000.41.36.png)


### - Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

For this model we used 2 hidden layers with 80 and 30 neurons per hidden layer respectively. As per activation functions, for the hidden layers we used relu because it's an advanced function and speeds the process, and sigmoid for the output layer as it's more efficient and accurate for this model.

First hidden layer = 80 units, activation = relu
Second hidden layer = 30 units, activation = relu
Output = 1 unit, activation = sigmoid

![Alt text](../../Screenshot%202023-02-12%20at%2023.48.57.png)

- Were you able to achieve the target model performance?

We were not able to achieve the target model performance (75%). The accuracy of the model was 73%, which is not enough to make a decision.

![Alt text](../../Screenshot%202023-02-13%20at%2001.07.37.png)

- What steps did you take to try and increase model performance?

We created 3 different attempts to make sure the model reaches the target performance.

1. In attempt # 1, we increased the number of neurons on both hidden layers. However, the accuracy of this attempt was 72%

![Alt text](../../Screenshot%202023-02-13%20at%2001.12.06.png)

![Alt text](../../Screenshot%202023-02-13%20at%2001.12.22.png)

2. In attempt # 2, we added a third hidden layer and changed the number of neurons per layer. The accuracy of this attempt was 72%.

![Alt text](../../Screenshot%202023-02-13%20at%2001.12.35.png)

![Alt text](../../Screenshot%202023-02-13%20at%2001.12.51.png)

3. In attemp # 3, we added a fourth hidden layer, and changed the activation function of the hidden layers and output layer to sigmoid. The accuracy of this attempt was 72%

![Alt text](../../Screenshot%202023-02-13%20at%2001.16.38.png)

![Alt text](../../Screenshot%202023-02-13%20at%2001.16.54.png)


## Summary:

The deep learning neural network model we created and trained didn't reach the target model performance (75%). An accuracy of 75% is not high enough to help us predict what organisations shouldn't receive donations and most likely we'll need to create, train and test a more accurate model.

My recommendation for Alphabet Soup, especially because of how important and critical this matter is, is to create a new prediction machine learning model using Random Forest Classifier, as it will allow us to create decision trees for a more accurate prediction, it's easy to interpret and it can handle outliers.