
## Background

The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With machine learning and neural networks, used the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
Data set contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

**Overview of the analysis:** 
The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. Using machine learning and neural networks, the features in the provided dataset is used to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
This analysis includes Jupyter Notebook files that build, train, test, and optimize a deep neural network that models charity success. TensorFlow Keras Sequential model with Dense hidden layers are used to get the target model performance.

**What steps did you take to try and increase model performance?**

Made 3 attempts to optimize the model, but all the 3 optimizations did not help in increasing the performance.

**Trial 1:**

For trial 1, changed the number of epochs to 50 and units for hidden layer 1 changed to 3 times the input features.

**Trial 2:**

For trial 2 tried following changes:
changing Cut off value for APPLICATION_TYPE from 500 to 1000
changing Cut off value for CLASSIFICATION from 1000 to 2000
Additional hidden layer is added.

**Trial 3:**

For trial 3 the activation function of output layer is changed to tanh for optimization and epochs from 50 to 100.

**3.Summary:** 

The deep neural network classification model used here predicts with 74% accuracy. This does not meet the 75% accuracy target, and the optimization methods employed here have not caused significant improvement.
Random Forest Classifier could be used as an alternative model. It might perform better as it is more accurate with categorical data.
