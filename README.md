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
