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
## Grid Search 
We furthur optimised our results using Grid search. Grid searching is a technique employed to fine-tune the hyperparameters of machine learning models. It systematically explores a predefined hyperparameter space, evaluating each combination using cross-validation. By exhaustively searching through various hyperparameter configurations, grid searching aims to identify the optimal set of hyperparameters that maximize the model's performance on the validation data. This automated approach streamlines the hyperparameter tuning process, saving time and effort while enhancing the model's ability to generalize to unseen data. Once the best hyperparameters are determined, the model can be trained on the entire dataset, including the validation set, to ensure optimal performance when deployed in real-world scenarios.
## Results after Grid Searching
We used Grid Search on our Random forest algorithm and following are the results:
- **Best: 0.903879 using {'criterion': 'entropy', 'max_depth': 10, 'n_estimators': 80}**
- #8 0.877634 (0.015339) with: {'criterion': 'gini', 'max_depth': 5, 'n_estimators': 20}
- #6 0.880740 (0.014351) with: {'criterion': 'gini', 'max_depth': 5, 'n_estimators': 80}
- #4 0.898737 (0.018659) with: {'criterion': 'gini', 'max_depth': 10, 'n_estimators': 20}
- #2 0.902093 (0.015755) with: {'criterion': 'gini', 'max_depth': 10, 'n_estimators': 80}
- #7 0.879562 (0.015090) with: {'criterion': 'entropy', 'max_depth': 5, 'n_estimators': 20}
- #5 0.881205 (0.014811) with: {'criterion': 'entropy', 'max_depth': 5, 'n_estimators': 80}
- #3 0.901950 (0.016506) with: {'criterion': 'entropy', 'max_depth': 10, 'n_estimators': 20}
- #1 0.903879 (0.017617) with: {'criterion': 'entropy', 'max_depth': 10, 'n_estimators': 80}
