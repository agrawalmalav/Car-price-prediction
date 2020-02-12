# Car-price-prediction



Problem statement: Given dataset consist 3390  used cars data that were put for auctions. 18 columns present describing the features of cars on which car price depends. The aim of the model is to predict the prices of the cars

Since we need to predict the car prices values which falls in continuous range, we adopt Linear regression model to predict the car prices.
The dataset doesn’t contain any null values. Datasets consists of 7 parameters of object datatype.
Since the datasets consists of only one type of car company dropping the parameter shouldn’t affect our model.
4 parameters, namely modelID, car_paint_color, car_type and fuel are encoded using one hot encoding.
8 unknown features were of Boolean type and handled by binary classification of true and false (true =1 and false=0)
The registration data parameter of the format mm-dd-yyyy had same months and hence only year and day of registration data were considered. Year extracted from the registration date by subtracting the oldest year from each registration year and a separate parameter of registration day was created. Similar approach was adopted for the sold_date parameter 
Variance of the various parameters of the datasets was calculated and was normalized/standardized (min max scaling) to reduce the variance.
Correlation amongst different features showed that feature7 has very little correlation with the car price. Scatter plot of different parameters against car price revealed the various outliers and hence were removed from the dataset.

Dataset was split to form the corresponding test and train sets. Model was observed to perform the best on a 74 :26 (Train: Test) split ratio.
The model was trained and predicted the values of car prices of test data
Mode was evaluated using r_2 square metric.
The model performed with 84+ percentage of reliability.
