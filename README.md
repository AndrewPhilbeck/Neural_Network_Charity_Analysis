# Neural Network Charity Analysis

## Overview

I used machine learning in order to try and create a binary classifier that is capable of predicting whether or not applicants funded by Alphabet Soup would be successful.

## Results of Analysis

### Preprocessing

* I chose the variable IS SUCCESSFUL to be the target of the model

* I chose to keep the following variables for the features of the model: APPLICATION TYPE, AFFILIATION, CLASSIFICATION, USE CASE, ORGANIZATION, STATUS, INCOME AMT, SPECIAL CONSIDERATIONS, ASK AMT (amount).

* I removed the variables EIN and NAME from the DataFrame. 

![DROPPED VARIBLES](https://user-images.githubusercontent.com/115502048/224857784-2ecb27ac-5d82-450d-8b74-b84e2f8ee68c.png)
	
### Compiling, Training and Evaluating the Model

* I chose two hidden layers, with the first having 80 neurons and the second having 30. I chose the activation “relu”. I thought this was a large amount to provide a good idea of if the model was going to be able make accurate predicitons. 

* I was not able to achieve the target of 75%. The first attempt gave only an accuracy score of 47%.

* I attempted to change the model five more times to see if I could improve the accuracy of the model. 

In the first attempt I dropped more features that I thought could be noisy.

![first attempt](https://user-images.githubusercontent.com/115502048/224857826-dfe71907-232c-4036-a4a9-05182815ed7c.png)

This model’s accuracy score was 62%

In the second attempt I added a third hidden layer with 30 additional neurons.

![second attempt](https://user-images.githubusercontent.com/115502048/224857864-4fdaf7f1-93fb-4662-87ed-cbdd4b5ff720.png)

This model’s accuracy score was 52%

In the third attempt I changed the second activation function from “relu” to “sigmoid”.

![third attempt](https://user-images.githubusercontent.com/115502048/224857912-713f9cd1-711a-4ab8-be13-cf43b80e5727.png)

This model’s accuracy score was 53%

In the fourth attempt I combined the previous three.

![fourth attempt 1](https://user-images.githubusercontent.com/115502048/224857938-5b8a4266-5d3c-42b6-b963-87fb2a9b5231.png)

![fourth attempt 2](https://user-images.githubusercontent.com/115502048/224857954-9089b833-e8e5-4159-94ce-93dbb317997e.png)

The model’s accuracy was 53%

In the fifth attempt I changed the activation from “relu” to “tanh”

![fifth attempt](https://user-images.githubusercontent.com/115502048/224857981-119ba694-707a-4345-b81e-0819c453083e.png)

The model’s accuracy was 46%

## Summary 

The results of the model were not acceptable. I was never able to have an accuracy score above 75% which was my goal. 

The highest accuracy score came simply by removing excess variables. My recommendation would be to look at the variables and trim them down to as few as possible. Once that is done if the results are still not met to begin a trial and error of adding hidden layers, increasing the number of neurons and adjusting the number of epochs run. 

