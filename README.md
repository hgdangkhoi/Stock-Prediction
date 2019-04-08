# Stock-Prediction

## Summary

This is part of a project for Artificial Intelligent Class at California State University, Sacramento

Stock is an essential part of the economy, and it is crucial for a buyer to know how the stock market behaves in order to make the best purchases. The goal of this project is to predict the "Close" price of stock on the same day using the day's data, or predict the "Close" price of stock on the day based on the last 7 days' data. I also attempt to predict Google's stock for the next 3 days, or the next 7 days based on data on the previous 7 days. We take a look and compare the performance between fully-connected neural network model, CNN model, and the LSTM model, which is known to perform well on sequence data.


## Implementation
1. **Dataset**: The small dataset can be viewed in the csv files of this repo.

2. **Data Preprocessing**: The data used in this project is relatively small, around 4500 records. There are 7 columns in the original data: "Date", "Open", "High", "Low", "Close", "Adj_Close", and "Volume." I dropped the "Date" and "Adj_Close" columns because they are not relevant for the training and testing. The first 70% of the data is used for training, and the remaining 30% is used for testing. I did not use train_test_split in order not to introduce future data in the training set. As stock price is predicted using the data from the past, the training data should not contain data from the future, or the data from the period of time that we are trying to predict.


3. **Model**: The models used in this project include: CNN, fully-connected NN, and LSTM model. The data is split into training and testing set. I also use EarlyStopping and ModelCheckPoint to save the best model and avoid overfitting. The main framework of this project is Tensorflow and Keras. The RMSE score and lift chart of each model were used to compare the performances of all the models. 

## Result:
All 3 models performed relatively well when attempting to predict the stock price of the next day based on previous 7 days' data. However, for the task of predicting Google's stock for the next 3 or 7 days, the LSTM model still need a lot of improvement. The Google's stock is known to have one of the hardest stock to predict, and because I did not run my model on other companies' data, I was not able to compare the prediction between different companies. Future work should be done to improve the accuracy of the model before it is usable.  
