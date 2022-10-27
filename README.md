# Neural_Network_Charity_Analysis
## Overview of the Analysis:
  Alphabet Soup is a nonprofit fundation offering research funds for more than 34,000 organizations. The purpose of this project is to design and train the deep machine learning and neural network models using the Python TensorFlow library to test and optimize the models, and to predict whether applicants will be successful if funded by Alphabet Soup. So the models will help Alphabet Soup to determine which organizations should receive donations.

## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
  "IS_SUCCESSFUL" is the target variable for my model because it indicates if the money was used effectively. 

* What variable(s) are considered to be the features for your model?
  "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT". The nine variables are the features for the model.

* What variable(s) are neither targets nor features, and should be removed from the input data?
  "EIN" and "NAME" are two variables neither targets nor features, and should be removed from the input data. 

### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  The neural network model has 2 hidden layers, 80 neurons for the first layer, and 30 neurons for the second layer. 
    * Generally, many complex interactions can be characteried by 2-3 hidden layers, so 2 layers is a reasonable choice to start for the model. 
    * Also, since 80 is about double amount of the 43 input features, and 30 is about 2/3 of the input features, that meets the rule of thumb for the amount of neurons. 
    * I use ReLU activation function to identify nonlinear characteristics from the input values, and use sigmoid activation function for the output layer to predict the probability.

* Were you able to achieve the target model performance?
  No, my three optimization attempts acheived the predictive accuracy at 72.49%, 72.57%, 72.62%, respectively, all of which are below the target model performance of 75%.

* What steps did you take to try and increase model performance? 
    * Additional neurons are added to hidden layers.
    * Additional hidden layers are added.
    * The activation function of hidden layers is changed from renu to tanh for optimization.

## Summary
The initial neural network deep learning model achieved an accuracy score of 72.36%, and my three optimized models all achieved a predictive accuracy around 72.5% to predict if an Alphabet Soup-funded organization will be successful. There was no significant improvement in accuracy score. Since the neural network deep learning models are prone to overfitting and could not help meet the target standard of 75% accuracy, random forest classifiers are recommended to solve the classification problem. This is because that random forest classifiers are a type of ensemble learning model which is more robust and accurate, and they can easily handle outliers and nonlinear data to avoid overfitting. 