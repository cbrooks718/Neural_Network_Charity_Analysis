# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis is to use machine learning and neural networks to help Alphabet Soup's business team create a binary classifier capable of predicting whether applicant will be successful if funded by Alphabet Soup. A CSV containing over 34,000 organizations was used to create the model. In order to do so, the following steps must be completed:
- Preprocessing the data
- Compile, train and evaluate the model
- Optimize

## Results

### Data Preprocessing 

In order to pre-process the data, the following steps were made in order to create the neural network. 
- Columns "EIN" and "NAME" were dropped as they were non-beneficial ID columns. 
- Columns "APPLICATION_TYPE" and "CLASSIFICATION" were subject to binning in order to reduce the # of unique values. The purpose of binning is to help our dataset from becoming too wide, making it easier for our model to fit the data. 
- Next, the categorical data is separated into a new data frame to be encoded using OneHotEncoder. Then, the encoded data frame is merged back with the original dataset. 
- Last, the data is split into training and testing variables and then scaled using StandardScaler. 

### Compiling, Training, and Evaluating the Model

In order to create a successful model, the following parameters were chosen:
- For the input layer, we used the # of features, 43, from the data. 
- For the hidden layers, two layers of 80 and 30 neurons was chosen. Given that our input layer has 43 neurons, the hidden layers should have a similar number of neurons. Therefore, for our two layers, one will have less than the input and the other will have more. 
- For the output layer, 1 neuron is used as this neural network is a binary classification model
- For the activation functions, ReLu was used for the hidden layers and Sigmoid was used for the output layer. 
- After compiling, training and evaluating the model, the model accuracy was roughly 72.9% accurate with a loss metric of 56.0%

### Optimization

Three attempts were made to optimize the model:
- Attempt 1: More neurons were added to both of the hidden layers. The model accuracy was 72.9% and the loss metric was 56.3%
- Attempt 2: An extra hidden layer was added. The third hidden layer had a total of 6 neurons. The model accuracy was 72.7% with a loss metric of 56%
- Attempt 3: The activation function of the hidden layers was changed to tanh and the # of epochs was reduced to 65. The model accuracy was 72.8% with a loss metric of 55.7%

## Summary

Overall, the model failed to reach the accuracy benchmark of 75%. One recommendation that can be applied to help improve the model is using kt-tuner to find what the optimal parameters are for the deep learning model. If it's discovered that the optimal parameters can't reach an accuracy score of 75%, then, a supervised machine learning model might be a better fit for creating a binary classifier. 

## Resources

1. Rob HyndmanRob Hyndman                    54.4k2727 gold badges136136 silver badges186186 bronze badges, R., dougdoug                    10.3k11 gold badge2424 silver badges2626 bronze badges, D., hobshobs                    2, hobshobs, RedomanRedoman                    96566 silver badges55 bronze badges, R., Dikran MarsupialDikran Marsupial                    51.4k66 gold badges132132 silver badges194194 bronze badges, D., prashanthprashanth                    3, prashanth, Vicente CartasVicente Cartas                    26911 silver badge33 bronze badges, V., Martin ThomaMartin Thoma                    1, M., user91213user91213                    2, user, chainDchainD                    13122 silver badges44 bronze badges, chaninD. D., Dan ErezDan Erez                    24122 silver badges66 bronze badges, D., &amp; sapysapy                    17722 silver badges33 bronze badges, sapysapy. (1957, April 1). How to choose the number of hidden layers and nodes in a feedforward neural network? Cross Validated. Retrieved April 24, 2023, from https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw 