# deep-learning-challenge

## Overview of Analysis
    
* The intent of this analysis is to predict whether grant applicants will be successful if funded by Alphabet Soup. A dataset with over 34,000 organizations and their characteristics were provided to assist with the prediction model.

## Results

* Data Preprocessing
    * The target variable for the model is "IS_SUCCESSFUL" saved as "y".
    * The features for the model are all the remaining columns excluding "EIN" and "NAME". These features are saved as "X".
    * "EIN" and "NAME" were removed from the input data as they did not qualify as targets or features.
* Compiling, Training, and Evaluating the Model
    * The model had two hidden layers with 80 and 30 neurons respectively. There was also an output layer with one neuron. I used two activation functions: "tanh" for the two hidden layers and "sigmoid" for the output layer. The number of neurons for the first hidden layer is approximately double the features of the data. The number of neurons for the second hidden layer is about 2/3 of the features. Only one output is required for the model. In an attempt to increase the accuracy, the number of neurons was doubled with little change so it was reverted back to the original numbers.
    * The required 75% accuracy was not achieved within the model. 
    * Multiple changes were made to attempt to increase the percentage including increasing the number of neurons, adding dropout layers, adjusting the learning_rate, and changing the number of epochs. In addition, different activation functions were used, including "relu" and "leaky_relu", which had little impact on the final accuracy percentage. There was an increase with the changes from 0.7243 (72.4%) in the initial model to 0.7277 (72.8%) in the optimized model.

## Summary
    
    * Using the Keras model within Tensorflow, the prediction was returned with approximately 72.8% accuracy. The goal was 75% so the model fell just short of the optimal result. Though multiple adjustments of the layers and epochs, the percentage was able to achieve the requisite score. Two hidden layers were used to attempt to strengthen the successes and minimize the loss. The model was trained through first 100 then 150 epochs. The results showed little change with the increased number of epochs. 
    * As an additional option instead of using a Keras model, the data could have been modeled using K-Nearest Neighbors. This model also provides an accuracy model based on multiple features by sorting true and false positives and negatives hrough a confusion matrix. 
