# Neural_Network_Charity_Analysis

## Overview

### Purpose

The purpose of this project was to analyze data for the nonprofit foundation, Alphabet Soup. The analysis focused on data about grant recipients, to attempt to create a neural network model that could identify which organizations would make good grant recipients. 

### Process

This project was completed using tensorflow in Google Colab notebooks.

## Results

### Data Preprocessing

- The model's target variable was whether or not the organization successfully used their grant funding.
- The model's feature variables were: type of application, sector of industry, government organization classification, use case for funding, organization type, active status, income classification, special considerations for application, and total ask amount. 
- The name and EIN of the organization were neither features nor targets, and were removed from the dataset during preprocessing.

### Compiling, Training, and Evaluating the Model

- After an initial model using two hidden layers with 80 and 30 neurons, and the "relu" activation, I attempted to increase the accuracy of the model by (1) increasing the first hidden layer from 80 to 90 neurons, (2) adding another hidden layer with 10 neurons, and (3) trying the "leakyReLU" activation. Because the dataset was so large, I believed additional layers and neurons might be useful for the model to train, and the leaky ReLu model to avoid the model being saturated at 0.
- I was not able to improve the model's accuracy.
  - Original model accuracy:
  ![Original Model Accuracy](https://github.com/ehalprin/Neural_Network_Charity_Analysis/blob/main/Original_Model_Accuracy.png)
  
  - Adjusted model accuracy:
  ![Adjusted Model Accuracy](https://github.com/ehalprin/Neural_Network_Charity_Analysis/blob/main/Adjusted_Model_Accuracy.png)

- Besides the above steps, I also tried to reduce the number of application types and tried taking out several different columns (including Status, Application Type, Classification Type, and Special Consideration) but removing these columns did not improve the model's accuracy at all.

## Summary

Overall, the deep learning model was able to predict whether an organization would be successful in using their grant funding by just over 70%. However, despite several attempts to improve the model, it was difficult to increase the model's accuracy, and the model took quite a long time to run through even 50 epochs. As a result, I would recommend trying a Random Forest model. The data is already tabular, which the Random Forest model can process. The Random Forest Model is also significantly faster in processing, which would allow for adjusting the data (i.e. dropping or binning columns) more easily.
