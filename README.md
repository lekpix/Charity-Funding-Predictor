
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

**2.Results: 
Data Preprocessing **
**What variable(s) are considered the target(s) for your model?**

IS_SUCCESSFUL

**What variable(s) are considered to be the features for your model?**

'STATUS', 'ASK_AMT', 'APPLICATION_TYPE_Other',
       'APPLICATION_TYPE_T10', 'APPLICATION_TYPE_T19', 'APPLICATION_TYPE_T3',
       'APPLICATION_TYPE_T4', 'APPLICATION_TYPE_T5', 'APPLICATION_TYPE_T6',
       'APPLICATION_TYPE_T7', 'APPLICATION_TYPE_T8',
       'AFFILIATION_CompanySponsored', 'AFFILIATION_Family/Parent',
       'AFFILIATION_Independent', 'AFFILIATION_National', 'AFFILIATION_Other',
       'AFFILIATION_Regional', 'CLASSIFICATION_C1000', 'CLASSIFICATION_C1200',
       'CLASSIFICATION_C2000', 'CLASSIFICATION_C2100', 'CLASSIFICATION_C3000',
       'CLASSIFICATION_Other', 'USE_CASE_CommunityServ', 'USE_CASE_Heathcare',
       'USE_CASE_Other', 'USE_CASE_Preservation', 'USE_CASE_ProductDev',
       'ORGANIZATION_Association', 'ORGANIZATION_Co-operative',
       'ORGANIZATION_Corporation', 'ORGANIZATION_Trust', 'INCOME_AMT_0',
       'INCOME_AMT_1-9999', 'INCOME_AMT_10000-24999',
       'INCOME_AMT_100000-499999', 'INCOME_AMT_10M-50M', 'INCOME_AMT_1M-5M',
       'INCOME_AMT_25000-99999', 'INCOME_AMT_50M+', 'INCOME_AMT_5M-10M',
       'SPECIAL_CONSIDERATIONS_N', 'SPECIAL_CONSIDERATIONS_Y'**


**What variable(s) are neither targets nor features, and should be removed from the input data?**

'EIN','NAME'

**Compiling, Training, and Evaluating the Model**

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**

For this analysis 2 hidden layers has been used. First hidden layer has twice the number of input features which is considered ideal and second layer has 1/4 th of the input features of hidden_layer_1. and activation functions used are relu and sigmoid.
If data is less complex and is having fewer dimensions or features then neural networks with 1 to 2 hidden layers would give the optimum results. 

**Were you able to achieve the target model performance?**

Using this model the target performance of 75% was not achieved, but got an Accuracy of  0.7415743470191956 and Loss of 0.5560470819473267 .

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
