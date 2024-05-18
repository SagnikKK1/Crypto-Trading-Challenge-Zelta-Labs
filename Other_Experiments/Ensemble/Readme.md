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

## Training and Testing
We utilize k-fold cross-validation to evaluate the performance of each machine learning model in our ensemble. This approach ensures robustness by partitioning the training data into k subsets (or folds), training the model k times on different combinations of training and validation sets, and averaging the results.

For each model in our list, we perform k-fold cross-validation using the KFold function from scikit-learn, specifying the number of splits (n_splits). We then compute the evaluation metric (e.g., accuracy, precision, recall) for each fold using the cross_val_score function.

The results and standard deviation of the evaluation metric across all folds are stored in the results list. Additionally, the names of the models are stored in the names list for reference.

Finally, we print the mean and standard deviation of the evaluation metric for each model using a formatted message, indicating the average performance and its variability across folds. This provides insights into the model's generalization performance and helps in selecting the most suitable model for our forecasting task.
## Initial Results
Metric used here was "accuracy".
- Sample-> Name : Accuracy (Standard Deviation)
- LR: 0.985289 (0.007221)
- LDA: 0.897271 (0.017575)
- CART: 0.879491 (0.015983)
- NB: 0.783258 (0.045853)
- NN: 0.810535 (0.112958)
- AB: 0.901379 (0.014738)
- GBM: 0.912769 (0.014071)
- RF: 0.908449 (0.015287)
