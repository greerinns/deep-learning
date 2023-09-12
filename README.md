# deep-learning
## Overview
The goal of this analysis was to create a binary classification model using deep learning techniques to predict whether organizations funded by Alphabet Soup will be successful in their ventures. We were provided with a dataset containing information on more than 34,000 organizations that have received funding from Alphabet Soup. The dataset includes data about each organization, such as application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and whether the money was used effectively.
<img width="1044" alt="Screenshot 2023-08-03 at 4 36 13 PM" src="https://github.com/greerinns/deep-learning-challenge/assets/47437697/66bcc837-0145-44b7-8557-65c970996fd0">

## Results
### Data Preprocessing
- The target variable for our model is "IS_SUCCESSFUL," which indicates whether the funding was used effectively (1 for successful and 0 for not successful).
- The features for our model include all other columns in the dataset except for "EIN" and "NAME," which are identification columns and do not contribute to the prediction
- Variables "EIN" and "NAME" were removed from the input data during preprocessing

  <img width="904" alt="Screenshot 2023-08-03 at 4 38 11 PM" src="https://github.com/greerinns/deep-learning-challenge/assets/47437697/7d176896-ff1f-4dcc-9caa-dae9b738aaa2">

### Compiling, Training, and Evaluating the Model
For the neural network model, we started with two hidden layers with 60 and 15 neurons, respectively. We used the ReLU activation function for the hidden layers to introduce non-linearity and improve the model's ability to learn complex patterns. The output layer had a single neuron with the sigmoid activation function, which is suitable for binary classification problems, as it provides a probability-like output. The model was trained for 100 epochs.
After the initial training, the model achieved an accuracy of around 73%, which was below the target of 75%.

<img width="529" alt="Screenshot 2023-08-03 at 4 45 16 PM" src="https://github.com/greerinns/deep-learning-challenge/assets/47437697/f2b60c96-6587-4eff-8acc-69e96878ad72">


<img width="586" alt="Screenshot 2023-08-03 at 4 44 21 PM" src="https://github.com/greerinns/deep-learning-challenge/assets/47437697/f6845f71-5fbc-479f-8905-bfd44955368c">

To improve the model's performance, several optimization strategies, including:
- dropping three columns (undid this as it made the model worse)
- increasing the "other" bin for the application type binning (undid this as it made the model worse)
- binned the asking amount column into two categories, 5000 and >5000
- added a third hidden layer
- increased the neurons in the second hidden layer from 15 to 35

<img width="571" alt="Screenshot 2023-08-03 at 4 44 47 PM" src="https://github.com/greerinns/deep-learning-challenge/assets/47437697/b8ddbbfd-1946-466b-9a11-58ae4f7fcd93">

### Summary
The deep learning model we created was unable to achieve the target predictive accuracy of more than 75%, but was close with around 73% and had several attempts at increasing this. 

My recommendation for further improving the model's performance is to explore more advanced neural networks beyond this simple model, as if the current neural network model is insufficient accuracy-wise, there is unlikely to be a more rudimentary supervised learning solution.
