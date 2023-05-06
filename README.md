# HandwritingPrediction

Introduction

This project aims at working on a dataset that has multiple pixel values as predictor variables and 1 target variable - “label” which is the digit. To understand this, we can think of the digit as what we predict after looking at all the pixel values that we have. If a machine can identify the digit given all the features accurately it can be used for multiple problems. For example, in this project, if our model works well we will use it to test the handwriting of students in order to machine learning model to understand which students may need to work on their motor skills at a young age. For this purpose, we will be building a simple KNN algorithm and Neural Networks and then use multiple benchmarking metrics to compare and contrast both models.
Analysis


Modeling

The dataset has pixel values ranging from 0 to 255. We planned on working with KNN and Neural networks. Both of these algorithms work better if the data is scaled. Feature scaling is essential for machine learning algorithms that calculate distances between data. If not scale, the feature with a higher value range starts dominating when calculating distances. For better performance and accuracy we scale the data by using standard scaler method form python’s sklearn library. Now, we will be performing KNN and Neural Network after separating the predcitir variables and target variables. The dataset is split between train and test sets using sklearn’s train_test_split library. 70% data is used for training and 30% for testing purposes.

KNN Classifier

We build a KNN classifier to predict the digit. The classes are from 0 to 9. We use the scaled data as KNN requires scaling of data because KNN uses the Euclidean distance between two data points to find nearest neighbors. Euclidean distance is sensitive to magnitudes. The features with high magnitudes will weight more than features with low magnitudes. On keeping the neighbours as 7 we get an accuracy of 64%. The average recall and precision is 64%. It can be said that our model can accurately predict almost 64% of the times.

Neural Network

We built a Neural Network to predict the digit and used scaled data as gradient descent converge much faster with feature scaling than without it. To get the better result, we tuned a few
 
parameters and tried different combinations. The model worked better with adam solver as it works well with large datasets. Also, by increasing the maximum iterations to 15000, the model provided a better accuracy that is 68% and also a precision and recall of 68%.

Comparison of the models

The F1 score is calculated using both precision and recall. The best score is 1.0 and the worst is

0.0. As a rule of thumb, the weighted average of F1 should be used to compare classifier models.


Model	            Accuracy	Precision	Recall	F1 Score
KNN	                64%	      63%	     64%	   0.63
Neural Networks	    68%	      69%	     68%	   0.68
 
Conclusion

In this project, we built two models to predict the correct label - KNN and Neural Network. KNN is much simpler in terms of complexity than Neural Networks.

The accuracy achieved with Neural Network is higher but it also takes a lot of time for execution.

Both the models did not perform too well nor were they too bad.KNN is not suitable for large dimensional data.

It is known that Neural Networks require large amount of data to work well and in this project we had fairly large data. However, the trade off with Neural Networks is that it is computationally too expensive.

The models could rightly identify the labels almost 65% of the times but with our business case we should not completely rely on it as it is about a students motor skills. I think this model can be sued for initial screening however, the final results should not be evaluated from these models.
