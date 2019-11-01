File Name: Phase_Two.ipynb
======================

# Phase Two 

Phase two of this project aims to develop a machine learning based prediction model for predicting the falling rate in the cancer patients 

## Installation 

Use the package manager (pip) or anaconda’s condo method to install the packages required for the environment to successfully run the code in the file above

```bash
pip3 install Python3
pip3 install jupyter
pip3 install pandas
pip3 install numpy
pip3 install meatplotlib
pip3 install seaborn
pip3 install sklearn
pip3 install imblearn
pip3 install csv
pip3 install difflib
```

Instruction for running the codes

## Load Packages

###First Section: Load and Clean the Data (Print out the statistics of data/ data imbalance/ Differentiate categorical features from numeric features/ Dealing with missing values)

In [2] : Use pandas to read input csv data 
In [3] : Print the number of columns contained in the dataset
In [4]: Select the common columns of both GAP and COACH dataset
In [5]: Print the number of both control patient and falling patient in the dataset  
In [6]: Select the features with a #missing value of <15 to form a new data frame 
In [7]: 	Print the statistics of different features
In [8] : Plot the demographic data for the patients in the dataset
In [9] : Print the number of numeric value in the data frame
In [10]: Print the name of features that are non-numeric
In [11]: Plot the number of levels for the categorical data insurance plan 
In [12]: Merge the less frequently occurring levels into the same class
In [13]: Number of levels in insurance plan features after merging
In [14]: Convert the numeric variables like Age/Feel/KPS into categorical variables.
In [15]: Mapping other categorical variables 
In[16]: Fill all missing value with 0
In[17]: Show value with more than 2 missing and use mean or median to substitute
In [18]: Fill the missing value with median (Categorical Variable) and mean (Numerical Variables) respectively
In [20]: Dropping Nan for less than 2 missing values


### Second Section (Feature Selection)

In[21]: Import the package for feature selections (Sklearn)
In[22]: Split the at a set at a 0.2:0.8 ratio.
In[23] : Return the most important 22 features based on RFECV 
In[24]: Plot the figure using number of features vs. crossvaligdation scores on training dataset 
In[25]: Print the rank of features and their contribution to the model

During the session 2, we selected the features required for training the model in the following steps.

### Third Section (Model Development)

To install the imblearn packages, you might need to install it under the Conda environment. 

To change your export environment path to use Conda function in the terminal 

Please use: PATH=/Users/~/anaconda3/bin:$PATH

To install the imblearn package, Conda install imblearn can sometimes not work on some computers

If that’s the case, try:

sudo conda install -c glemaitre imbalanced-learn

In[26] Import the sklearn package and under sampling packages

In[27] apply the under sampling techniques on the training data set only

In[29] Fit the logistic regression model on the under sampled training set. Report Model Performance and Confusion Matrix

In [30] Fit the random forest model on the under sampled training set. Report Model Performance and Confusion Matrix

In [31]: Fit the MLP model on the under sampled training set.Report Model Performance and Confusion Matrix


### Forth Section

*** It is important for you to import recall_score using:

From sklearn.metrices import recall_score

Run each logistic regression model, random forest model and MLP model for 100 times respectively and report the average recall rate for each model after 100 times’ iteration

Next, plot the statistics for the recall rate for 100 times and plot a marplot to represent how the performances of three models differ.

### Fifth Section

Import LogisticRegressionCV from the sklearn.linear_model

Logistic RegressionCV used stratified k folder cross validation to make the evaluation of model performance to be more accurate.

Also, there is a output list that represented the confidence interval of probability predicted by the logistic regression model on each test data point.
