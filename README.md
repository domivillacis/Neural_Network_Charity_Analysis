# Neural Network Charity Analysis

## Overview of the loan prediction risk analysis

In this project I'm going to help Alphabet Soup, a non-profit foundation that helps organisations that protect the environment and improve the well-being of people around the world. Over the past 20 years, Alphabet Soup has donated more than $10 billion to a variety of causes and the company's President recently asked the analytics team to help predict which organisations are worth donating to to ensure the money of the foundation is used effectively.

We're going to create and train a deep learning neural network that will evaluate the input data and allow us to interpret a large and complex dataset. To create and test these models we'll use the python TensorFlow library. 

The results will help us making a final decision on which organisations should receive donations from Alphabet Soup.

## Results:

### Data Preprocessing

- What variable(s) are considered the target(s) for your model? 

The variable considered the target is: IS_SUCCESSFUL

- What variable(s) are considered to be the features for your model? 

The variables that are the features of our model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

<img width="1087" alt="Screenshot 2023-02-13 at 00 38 42" src="https://user-images.githubusercontent.com/112814924/218388690-93f5d8a3-5dec-4860-a477-4b679b57c55a.png">

- What variable(s) are neither targets nor features, and should be removed from the input data?

The variables that were not considered relevant for our first model are: EIN and NAME. 

However, to optimise the model in order to achieve a target predictive accuracy higher than 75%, we decided to remove 2 more irrelevant features: ORGANIZATION and SPECIAL_CONSIDERATIONS

<img width="853" alt="Screenshot 2023-02-13 at 00 41 36" src="https://user-images.githubusercontent.com/112814924/218388732-20d021fa-5bb9-4f3e-89f5-6d518586db5c.png">

### - Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

For this model we used 2 hidden layers with 80 and 30 neurons per hidden layer respectively. As per activation functions, for the hidden layers we used relu because it's an advanced function and speeds the process, and sigmoid for the output layer as it's more efficient and accurate for this model.

First hidden layer = 80 units, activation = relu

Second hidden layer = 30 units, activation = relu

Output = 1 unit, activation = sigmoid

<img width="839" alt="Screenshot 2023-02-12 at 23 48 57" src="https://user-images.githubusercontent.com/112814924/218388769-ec1a12bb-5634-4090-baa4-07c99d69429b.png">

- Were you able to achieve the target model performance?

We were not able to achieve the target model performance (75%). The accuracy of the model was 73%, which is not enough to make a decision.

<img width="623" alt="Screenshot 2023-02-13 at 01 07 37" src="https://user-images.githubusercontent.com/112814924/218388837-726d40fa-7e81-4847-92c2-ddae681a2fc7.png">

- What steps did you take to try and increase model performance?

We created 3 different attempts to make sure the model reaches the target performance.

1. In attempt # 1, we increased the number of neurons on both hidden layers. However, the accuracy of this attempt was 72%

<img width="849" alt="Screenshot 2023-02-13 at 01 12 06" src="https://user-images.githubusercontent.com/112814924/218388870-82bfe81f-fb9b-4402-8853-356336a1660f.png">

<img width="598" alt="Screenshot 2023-02-13 at 01 12 22" src="https://user-images.githubusercontent.com/112814924/218388894-a77e5f77-64d1-466d-a070-f0136dc9ae92.png">

2. In attempt # 2, we added a third hidden layer and changed the number of neurons per layer. The accuracy of this attempt was 72%.

<img width="855" alt="Screenshot 2023-02-13 at 01 12 35" src="https://user-images.githubusercontent.com/112814924/218388918-bce47d8b-917d-4a0f-aa74-20a32bacd9c0.png">

<img width="577" alt="Screenshot 2023-02-13 at 01 12 51" src="https://user-images.githubusercontent.com/112814924/218388933-e82364b6-b41f-43fe-a237-13b532c077ca.png">

3. In attemp # 3, we added a fourth hidden layer, and changed the activation function of the hidden layers and output layer to sigmoid. The accuracy of this attempt was 72%

<img width="765" alt="Screenshot 2023-02-13 at 01 16 38" src="https://user-images.githubusercontent.com/112814924/218388975-da43abc0-5e63-4c4c-9b05-11c1ece95b7b.png">

<img width="574" alt="Screenshot 2023-02-13 at 01 16 54" src="https://user-images.githubusercontent.com/112814924/218388992-ab3d3f60-a693-47e3-bd1e-302203ce9967.png">

## Summary:

The deep learning neural network model we created and trained didn't reach the target model performance (75%). An accuracy of 75% is not high enough to help us predict what organisations shouldn't receive donations and most likely we'll need to create, train and test a more accurate model.

My recommendation for Alphabet Soup, especially because of how important and critical this matter is, is to create a new prediction machine learning model using Random Forest Classifier, as it will allow us to create decision trees for a more accurate prediction, it's easy to interpret and we can use it to solve classification problems.
