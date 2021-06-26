---
title: "KeyDetect - Detection of anomalies and user based on Keystroke Dynamics"
date: 2021-03-21T03:04:12+05:30
description: "Keystroke Dynamics can be a promising two-step verify for authorizing sign-in."
tags: [projects]
---
# Abstract
Cyber attacks has always been of a great concern. Websites and services with poor security layers are the most vulnerable to such cyber attacks. The attackers can easily access sensitive data like credit card details and social security number from such vulnerable services. Currently to stop cyber attacks, various different methods are opted from using two-step verification methods like One-Time Password and push notification services to using high-end biometric devices like finger print reader and iris scanner are used as security layers. These current security measures carry a lot of cons and the worst is that user always need to carry the authentication device on them to access their data. To overcome this, we are proposing a technique of using keystroke dynamics (typing pattern) of a user to authenticate the genuine user. In the method, we are taking a dataset of 51 users typing a password in 8 sessions done on alternatedays to record mood fluctuations of the user. Developedand implemented anomaly-detection algorithm basedon distance metrics and machine learning algorithms like Artificial Neural networks (ANN) and convolutional neural network (CNN) to classify the users. In ANN, we implemented multi-class classification using 1-D convolution as the data was correlated and multi-class classification with negative class which was used to classify anomaly based on all users put together. We were able to achieve an accuracy of 95.05% using ANN with Negative Class. From the results achieved, we can say that the model works perfectly and can be bought into the market as a security layer and a good alternative to two-step verification using external devices. This technique will enable users to have two-step security layer without worrying about carry an authentication device.

# Results

Confusion matrix with negative class is shown below.


<img src="https://github.com/abhishekbamotra/abhib/blob/master/assets/images/keystroke-confusion.jpg" alt="Confusion matrix with negative class" align='center' height="400"/>


Table showcasing the results for different models attempted.

| Multi-Class Classification 	| Accuracy % 	|
|----------------------------	|------------	|
| ANN (With Negative Class)  	| 95.05      	|
| ANN (1-D Conv.)            	| 94.6       	|
| Random Forest              	| 93.66      	|
| ANN (Fully Connected)      	| 92.2       	|
| Support Vector Machine     	| 75.6       	|

# Everything in detail
I have uploaded everthing related to the project on 
[Github repository](https://github.com/abhishekbamotra/machinelearning24787)
