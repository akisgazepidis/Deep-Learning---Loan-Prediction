Loan Prediction Project
=======================

Overview
--------

The Loan Prediction project aims to develop a machine learning model that predicts whether a customer will take a loan or not based on various features provided in the dataset. The project utilizes a dataset named "Bank\_Personal\_Loan\_Modelling.csv" and employs a binary classification approach to classify customers into two categories: those likely to take a loan and those not likely to take a loan.

Prerequisites
-------------

Before running the code, ensure that you have the necessary Python packages installed. You can install them using the following command:

bashCopy code

`pip install pandas numpy matplotlib seaborn klib scikit-learn imbalanced-learn tensorflow shap`

Dataset
-------

The dataset used in this project is "Bank\_Personal\_Loan\_Modelling.csv," containing information about customers and whether they accepted a personal loan offer or not. The dataset is loaded into a Pandas DataFrame for further processing.

Data Preparation
----------------

The dataset is prepared for classification by splitting it into training, validation, and test sets. To address class imbalance in the training set, the ADASYN oversampling technique is applied. Additionally, features are scaled using MinMaxScaler, as the dataset does not contain negative values.

Neural Network Model
--------------------

The machine learning model is implemented using TensorFlow and Keras. The neural network architecture includes an input layer, two dense layers with dropout for regularization, and an output layer with a sigmoid activation function for binary classification. The model is compiled with binary crossentropy loss and the Adam optimizer.

Training and Evaluation
-----------------------

The model is trained on the oversampled training data and validated on a separate validation set. Training includes reducing the learning rate on plateaus. The model's performance is evaluated on the test set, and accuracy metrics are reported.

Model Performance Visualization
-------------------------------

The project includes visualizations to assess the model's performance. A plot of accuracy over epochs is generated, and a confusion matrix heatmap is plotted to visualize the correct and wrong classifications. Additionally, the feature importance analysis using SHAP (SHapley Additive exPlanations) is visualized with a summary plot.


Results
-------

The project outputs the accuracy of the model on the test set and provides visualizations for performance assessment. The confusion matrix heatmap and SHAP summary plot help interpret the model's predictions and feature importance.