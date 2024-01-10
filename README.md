# Data-preprocessing
This is the section 3 of Machine learning A - Z, where we first obtain the data and preprocess it to our liking.

# What is Data preprocessing?
Data preprocessing is a crucial step in the data analysis and machine learning pipeline. It involves cleaning, transforming, and organizing raw data into a format that is suitable for analysis or model training. 

# Pre-processing Steps:

## Missing Data
1.When we have a item from our analized file missing we tend to replace it with a new value: 

2.Used with the help of the sklearn librabry, more specific, the SimpleImputer, that replaces the itens with new values through a strategy, in which those new values are calculated, most of the times, with the mean formula.

3.After that, we use thee fit function, that trains the model to identify the itens missing.

4.When thee training is done, we use the function transform, to replace the missing values with the data's mean formula.

5. OPTIONAL STEP: We can also replace steps 3 and 4 with imputer.fit_transform that does the those steps at the same time.

## Encoding categorical data

### Enconding the independent variable
This step has the objective to standardize the values in the data, so we remove data that might have names, cities or yes/no and replace them with numbers, in the steps below:
1. First we import the function ColumnTransformer from the sklearn.compose library which gives us the ability to change a whole subset of columns and combine it to a singlee transformer. It takes a list of tuples, where each tuple contains three elements: a name for the transformer, a transformer (e.g., OneHotEncoder) and a list of column indices to which the transformer should be applied.
   
2. We then also import OneHotEncoder from sklearn.preprocessing, which converts the data into a binary matrix

3. After that, we call a instance of the function ColumnTransformer and makee the changes as necessary.
   
4. At last, we deefine X as the new numpy array of the instance ct (here we use fit_transform to train and already modify the values all at the same time).

### Enconding the dependent variable
In this case, the dependent variable is a case of categorical data of two options, yes or no, so we transform it to a new binary matrix:
1. First of all we import LabelEncoder from sklearn.preprocessing.

2. We then create a new instance of the LabelEncoder object, which don't require us to inform any variables inside
3. now we just give y the new atribuition of the trained and already written new values of the data.

## Splitting the dataset into the Training set and Test set
In this step, we need to understand that when training a machine learning model, we need to split the database into two: the training set, which are the values that we will inform thee model to learn, and the test set which were we let the model make predictions of the supposed values.
