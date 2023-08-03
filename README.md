# deep-learning-challenge
## Overview
The goal of this analysis was to create a binary classification model using deep learning techniques to predict whether organizations funded by Alphabet Soup will be successful in their ventures. We were provided with a dataset containing information on more than 34,000 organizations that have received funding from Alphabet Soup. The dataset includes various features that capture metadata about each organization, such as application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and whether the money was used effectively.

## Results
### Data Preprocessing
The target variable for our model is "IS_SUCCESSFUL," which indicates whether the funding was used effectively (1 for successful and 0 for not successful).
The features for our model include all other columns in the dataset except for "EIN" and "NAME," which are identification columns and do not contribute to the prediction.
The variables "EIN" and "NAME" were removed from the input data during preprocessing because they are neither targets nor features.
### Compiling, Training, and Evaluating the Model
For the neural network model, we started with two hidden layers with 80 and 30 neurons, respectively. We used the ReLU activation function for the hidden layers to introduce non-linearity and improve the model's ability to learn complex patterns. The output layer had a single neuron with the sigmoid activation function, which is suitable for binary classification problems, as it provides a probability-like output.
During the initial training, we used the Adam optimizer and binary cross-entropy loss function. The model was trained for 100 epochs with a batch size of 128. We also implemented a callback to save the model's weights every five epochs.
After the initial training, the model achieved an accuracy of around 73%, which was below the target of 75%.
To improve the model's performance, we attempted several optimization strategies, including:
Dropping some columns that contained redundant or irrelevant information.
Binning rare occurrences in columns to reduce the number of unique values and avoid overfitting.
Adjusting the number of neurons and layers in the neural network to increase its complexity and learning capacity.
Trying different activation functions to see if they result in better convergence or performance.
Increasing the number of epochs during training to allow the model more time to learn from the data.
After several iterations, we were able to achieve a predictive accuracy of over 75%.
### Summary
The deep learning model we created was able to achieve the target predictive accuracy of more than 75%. We successfully preprocessed the data, identified the target and feature variables, and trained the model to make accurate predictions on whether an organization funded by Alphabet Soup would be successful.

Our recommendation for further improving the model's performance is to explore more advanced neural network architectures, such as convolutional neural networks (CNNs) or recurrent neural networks (RNNs), depending on the nature of the data and the specific problem. These architectures can capture more complex patterns and dependencies in the data and may result in even better predictive performance.

Overall, the successful implementation of the deep learning model provides Alphabet Soup with a valuable tool to identify applicants with the best chance of success in their ventures, ultimately leading to more effective allocation of funds and positive social impact.