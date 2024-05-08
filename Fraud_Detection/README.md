# Fraud Detection

In today's digital age, financial fraud has become a common problem that financial institutions struggle to cope with. Machine learning techniques can play a significant role in detecting fraudulent activities by learning from past transaction patterns.

The goal of our project is to build models that can predict whether a transaction is fraudulent or not. The project involves the use of three machine learning algorithms: Random Forest, SVM and a Neural Network for this task.

The data we are using is a simulated credit card transaction dataset, containing legitimate and fraudulent transactions.It was generated using the Sparkov Data Generation tool created by Brandon Harris, with both training and testing datasets provided.The simulation took place from 1st January 2019 to 31st December 2020, covering credit card transactions of 1000 customers with 800 merchants. Each instance in the dataset represents a transaction, with features like transaction amount, location, date and time of transaction, etc. The target variable we're trying to predict is a binary feature indicating whether the transaction is fraudulent or not.


## Summary

The goal of this project was to develop models that can predict the outcome of a binary event with high precision and recall. Three types of models were implemented: a Random Forest model, SVM model, a Deep Neural Network (DNN) model. All models were evaluated using various metrics including ROC AUC score, precision, recall, and the F1 score. In the context of detecting fraudulent transaction, recall(sensitivity) is particularly relevant because maximizing on identifying the fraudulent transcation is important.

From the results obtained, the Random Forest model performed exceptionally well with a training ROC AUC score of 0.944, a testing ROC AUC score of 0.990, and an average cross-validation score of 0.972. The precision for class 1 (minority class) was 0.46, and it had an impressive recall rate of 0.80. This indicates that the Random Forest model was able to predict the majority of the positive class instances correctly, though at the cost of a higher number of false positives .

On the other hand, the default DNN model, which contains one hidden layer with 50 neurons, had a testing ROC AUC score of 0.976. The precision for class 1 is 0.76 and the recall for class 1 is 0.56. The DNN model after hyperparameters optimization had a testing ROC AUC score of 0.88. The precision for the minority class in the DNN model was 0.26, with a recall of 0.46. It is surprising that the default DNN model performed better than the one after hyperparameter optimization. Compared to the Random Forest model, the default DNN model performed less efficiently in detecting the fraudulent transaction, but its predicted fraudulent transactions are likely to be true.

Support Vector Machine performs worse than other models. The training ROC AUC score of SVM is 0.94. The precision and the recall for class 1 are only 0.03 and 0.73. Altertively, the Stochastic Gradient Descent model is used for linear SVM. It had low precision of 0.06, but higher recall of 0.75. A potential resample for imbalanced data may help the model to improve. These scores are worse than both DNN and Random Forest.

In conclusion, the high recall score of the Random Forest model implies that it was able to correctly identify a high proportion of positive instances, making it the more reliable model for this particular binary classification task.