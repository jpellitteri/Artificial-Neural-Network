# Artificial-Neural-Network
# Task / Overview

Artificial Neural Network (ANN) is a machine learning method that has recently re-emerged as an effective method for creating complex models with large amounts of data.  ANN can be described as layers of linear models within one model, performed in multiple stages to better optimize the decision.  The first layer is the input layer or original features of the dataset.  The final layer is the output layer or the model’s decision.  In between the input layer and the output layer is one or more hidden layers.  The hidden layer is what makes ANN unique and more hidden layers is what gives the name Deep Learning. The hidden layer is made up of a chosen number of weighted nodes involved in the model decision.  The number of layers is chosen by the Data Scientist. 

A hidden layer is made up of nodes which often starts as the same number of nodes as the input features but is chosen and tuned by the Data Scientist.  Each node within the layer is connected with the input features or nodes and with the nodes in the output layer or next hidden layer.  The result is a series functions that reflect the connections between the input layer to the hidden layer(s) to the output layer.  A non-linear function (chosen by the Data Scientist) is applied to the result of each of these functions or perceptrons. 
	
After the initial run, the model then corrects itself based on the error of the result.  The process is reversed from the output layer back to the hidden layers.  Weights are adjusted for all the nodes to minimize the error.  This process is known as backpropagation.  The process is iterated enough times to get the minimum error of the model.  The number of iterations and rate at which the weights are changed (gradient) is also chosen by the Data Scientist.  The best results from ANN come from large datasets and time to adjust the parameters. 
# Algorithm Applied	
In this repository, the question is asked: Can an reliable Artificial Neural Netowrk model be created for the Red Wine dataset?  The dataset consists of 4,898 records and 12 columns.  The 11 predictor variables are fixed_acidity, citric_acid, residual_sugar, chlorides, free_sulfur_dioxide, total_sulfur_dioxide, density, ph, sulphates, and alchohol.  There are no missing values. All predictor variables are continuous.  The target variable is quality, ranging from values 3 to 9 and will be treated as categorical for classification.
  
In Python, 80% of the dataset is assigned to the training dataset, 20% to the test data.  The training and test data is scaled using the Standard Scaler z score with a mean of zero because ANN performs better with attributes of equal scale.  The Multi-layer Perceptron (MLP) algrithm is used for the analysis.  This is Python's equivalent to ANN, MLPClassifier from sklearn.
  
The MLPClassifier parameters: solver = stochastic gradient descent (sgd), this is how the model minimizes error through backpropagation.
  
max_iter = 3000, this is the maximum number of iterations or until the model reaches tolerance (tol) Default tol is set to .0001.  This is the minimum change in error from one iteration to the next the model must reach.  
				
hidden layers = 3 hidden layers with 50 nodes each.  
# Results				
Results: The model results in a 59% accuracy score for correctly classifying the quality value on the test data.  This is an increase from 56% after initially running the model with 3 hidden layers at 10 nodes each.  This would be a poor model to use for predicting quality labels.  Further tuning of the parameters can increase or decrease the accuracy score.  A larger dataset would most likely improve the model as well. 
