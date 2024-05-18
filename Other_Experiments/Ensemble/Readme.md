# Introduction
This Readme aims to provide a summary of our approach using a combination of technical analysis and machine learning algorithms. The approach utilizes various supervised learning models to predict signals based on historical price data and technical indicators.
## Signal Generation
We implemented a moving average crossover strategy, wherein a signal of 1 is generated when the short-term moving average surpasses the long-term moving average, and 0 otherwise.
## Models Used
The following machine learning models are employed in this forecasting project:

- **Logistic Regression (LR)**- A statistical method for binary classification tasks modeling the probability of outcomes using a logistic function.
- **Linear Discriminant Analysis (LDA)**- A technique for dimensionality reduction and classification aiming to maximize class separability while minimizing within-class variance.
- **Decision Tree Classifier (CART)**-A non-parametric algorithm partitioning data into subsets based on feature values, creating a tree-like structure for classification tasks.
- **Gaussian Naive Bayes (NB)**- A probabilistic classifier assuming independence between features, often used for text classification and high-dimensional data.
 -**Multi-layer Perceptron Classifier (NN)**- A neural network with multiple layers of nodes, capable of learning complex patterns for classification tasks.
- **AdaBoost Classifier (AB)**-AdaBoost algorithm, short for Adaptive Boosting, is a Boosting technique used as an Ensemble Method in Machine Learning. It is called Adaptive Boosting as the weights are re-assigned to each instance, with higher weights assigned to incorrectly classified instances.
- **Gradient Boosting Classifier (GBM)**- Gradient Boosting is a powerful boosting algorithm that combines several weak learners into strong learners, in which each new model is trained to minimize the loss function such as mean squared error or cross-entropy of the previous model using gradient descent
- **Random Forest Classifier (RF)**- An ensemble method constructing multiple decision trees and aggregating predictions for robust classification.
