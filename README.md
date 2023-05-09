# deep-learning-challenge

In this analysis, we develop a model that will be used to predict the success of ventures that apply for funding from a nonprofit foundation.

We have 34,000 past results available. The ventures are described by their name, afilliation, organization type, use case, income amount and ask amount, among other characteristics. The ventures have all been described as either successful or failures. 

# Data Preprocessing

We will use the success/ failure binary, in the "IS_SUCCESSFUL" column, as our target.

The features we will use are afilliation, organization type, use case, income amount, ask amount, status, application type, classification type, and special considerations. 

Two variables will be removed before we begin, Name, and EIN as these are neither useful features nor the target.

# Compiling, Training, and Evaluating the Model

For the initial model, I selected a total of 27 neurons in 2 hidden layers, because we have 9 features, and I wanted to stick to having 3x the number of neurons. I chose the relu activation function for the hidden layers, and sigmoid for the output because it is ideal for a binary classification dataset.

The model did not perform to target, with an accuracy of only 72.3% over 100 epochs. 

In order to improve the model's performance, I first dropped one of the features and simplified another one through binning. Then, in the model design I added one more hidden layer, and changed the inner layer's activation function to tanh instead of relu.

Unfortunately, while the model's performance did improve to 72.5%, it still fell short of the target.

# Summary

The deep learning model failed to meet our threshold for accuracy, with a score of only 72.5%.

We could approach this binary classification problem with a simpler model, such as a logistic regression. In fact, we could create a for loop to try multiple different models, and then compare the results. If none of those had a higher accuracy score than our deep learning model we should go out and try to find more data.
