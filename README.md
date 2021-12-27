# Neural_Network_Charity_Analysis
## Overview of the analysis
The purpose of this project is to help Beks to predict whether applicants will be successful if funded by Alphabet Soup using machine learning and neural networks.
## Results
### Data Preprocessing
The dataset provided had the columns that captures metadata about each organization, such as the following: EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, 
ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, IS_SUCCESSFUL.

- The columns EIN, NAME are neither targets nor features, and were removed from the input data before compiling. They were dropped since they are identification columns and the model would not learn anything predictive from it.
- The variables APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT were considered as targets for the model. 
- The variable IS_SUCCESSFUL was considered to be the feature for the model.

### Compiling, Training, and Evaluating the Model
- For the model, 1 layer was defined. The input layer comprised of 20 neurons, 15 neurons for the hidden layer and 1 for the output layer *(Fig 1)*. Sigmoid activation fuction was selected for the output layer since the ouput had values between 0 and 1. For the other layers, relu activation function was selected.

![layers1](https://github.com/chinzjay/Neural_Network_Charity_Analysis/blob/main/layers1.PNG)
|:--:|
|Fig 1. Code snippet for hidden layers|

- The target model performance of 75% was not achieved. The model had an accuracy score of 68%.
- Inorder to optimize the performance of the model, the following were performed in subsequent optimizations.
  * Noisy variables were removed from features.
  * Additional hidden layers were added.
  * Additional neurons were added to the hidden layers.
  * The activation function of the hidden layers were changed.
- Even after the above optimizations, the accuracy of the model could not be improved. The reason for the low accuracy score could be as follows.
  * Noisy data.
  * Less data available to train and evaluate the model.

## Summary
The deep learning model performed had a very low accuracy rate. Even after multiple optimizations, the accuracy score (53%) could not be improved.
In my opinion the following models can be used for this classification problem.
 -  Support Vector Machine (SVM) since the amount of code required to build and train less than the comparable deep learning model.
 -  Random Forest Model since it requires less code and has faster performance.
 -  In addition PCA can be performed on the encoded dataset to remove noisy data and improve performance.
