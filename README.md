# Predicting-the-Driving-style
Predicting the Driving style using machine learning
Predicting the “Driving Style”
Abstract: In today's life, every human is in hurry to reach their destination like home, office, college, shopping mall, restaurant, etc. as quickly as possible. To reach their destination quickly people use vehicles on road use and drive them in faster mode which results in road accidents. And it is a common belief that if a person behavior is being monitored, it would be relatively safer. Driver behavior is a major cause for the road accidents. To address this problem, drive behavior analysis and prediction models need to be developed.


INTRODUCTION
Road safety rules and regulations are designed to prevent the citizens from fatal incidents. Although policies are in place, we observe negligent behavior of the drivers which lead to serious injuries or death crashes. It is of utmost interest of the authorities to understand and analyze human behavior to take necessary corrective and preventive actions
To design a driving assistance system there is a need to get an understanding of the data on the driving patterns and broadly distinguish bad drivers from good ones. In this dataset, we going to determine the driving pattern of the driver using the vehicle data, Trip data and weather information. 



METHODOLOGY
Dataset consists of Train and Test files containing information regarding Vehicle data, trip data and weather data information. Train data has 162566 rows, 20 predictors and a response variable. Test data has 61671 rows and 20 columns.
 An overview of the method is provided below. We first preprocess the data and using this preprocessed data we build models for predicting DrivingStyle of the drivers and defining the associated rule.


Preprocessing: Prior to performing any analysis we processed the data in the following way. 
First, I checked for’ NA’ values in the dataset and imputed the missing values in columns of train and Test data of trip data and weather data. diagnosis features with the mean for numerical data and mode for the feature that is categorical
Merging all Vehicle data, Trip data and Weather data of Train and Test together into train_final and test_final. Deleting the ID and date column. Performed VIF for Feature selection. After preprocessing, merging and dropping few columns we are left with 21 features and 162566 records in our training set and 20 features and 61671 records in the test data.


Classification: Identification of DrivingStyle of driver is posed as the problem of classifying of whether a DrivingStyle would be ‘Aggressive’, ‘Vague’ and ‘Normal’. Prior to training the classification algorithms, we randomly split our train dataset into two distinct sets - the training and the validation set. The training and validation set consisted of 80% and 20% of the data. We performed our classification with many models using cross validation, under sampling and over sampling the data. The most popular models were Decision Trees and Random Forest as they were showing a good result when we under-sample the data.
Associative Rule Mining (ARM): Along with the predictive modelling the main theme is to identify the DrivingStyle and help avoid accidents. One of the objectives is to assist the and researchers in getting more insights to understand and factors leading to it, hence indirectly increasing the efficiency of the diagnosis to prevent further readmissions. Groups of consistently occurring factors that influence DrivingStyle of the driver can be revealed by associative rule mining. The models we used, can give us helpful of utmost information useful for authorities to understand and analyze human behavior to take necessary corrective and preventive actions. Insight of the rules or consistently occurring factors. The rules with the highest fraction of DrivingStyle patterns indicate the factors that are strong predictors of risk of DrivingStyle.
Evaluation Criteria: A system for predicting high-risk patients is only useful, if a large fraction of patients at high-risk are correctly identified (i.e. high recall) without raising many false alarms (i.e. high precision). 
Precision (P): is defined as the fraction of ground truth positives among all the examples that are predicted to be positive.	 Precision = T P/(T P + F P)
Where, TP, FP stand for True Positives and False Positives respectively


CONCLUSION AND FUTURE WORK
In this work we presented a scheme to classify whether the DrivingStyle is going to be Aggressive or Normal or Vague. We found that random forests were optimal for this task. The dataset of readmissions is often skewed which causes problem while predicting. We also tried using Grid-Search and 5/10 fold Cross Validation, however we were not able to see any significant changes. Many conditions including traffic, altitude variations, psychological conditions, etc are not considered for the project. This can be further extension.
