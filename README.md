# Data-Science-Training-Project-1
This project is completed as part of the Data Science training at Orange Jordan. This is the first part of the project where we were given the data, analyzed it, cleaned it, applied operations to it, visualized it,  and made it ML model-ready.

# Dataset
The given dataset is the "Credit Score" dataset that involves information about bank customers including occupation, interest rate, etc. as input features which are then used to predict whether this customer has a "Good," "Poor," or "Standard" credit score.

# Files Break down

# Modifications_1
-	Importing the first version of the data.
-	Checking for null values and duplicates
-	Dropping meaningless columns (ID, Name, SSN)
-	Encoding the “Occupation” column
-	Manual Feature Extraction of the “Type_of_Loans” column

# Modifications_2
-	Importing the modified dataset from the previous file.
-	Encoding the remaining string features 
(“Credit_Mix”, “Payment_of_Min_Amount”, “Payment_Behaviour”, and “Credit_Score”).
-	All pre-encoded columns are dropped.

# Data_visualizations
-	Import the encoded data from the previous file.

Categorical Features:
-	Plotting categorical features against the target feature “Credit_Score” using FacetGrid plots.
-	In the plotting codes, categorical data is mapped to values to plot. However, in the end, mapped columns are dropped to not mix encoded columns and not encoded ones (Bivariate analysis).
-	Plotting each categorical feature against itself to find count, top feature and its frequency, and unique entries (Univariate analysis).
-	Categorical features heatmap using Cramer’s v_values.
  
Continuous Features:
-	Plot each continuous feature against itself to find count, mean, std, min/max entry, Q1, Q2, Q3, skewness, distribution type, and the number of outliers (Univariate analysis).
-	Plot each continuous feature against other continuous features to find the correlation in numbers, and the p_value (Bivariate analysis)
-	Continuous features’ Heatmap

Target Feature: 
- Plotting the target column (“Credit_Score”) in a pie chart to figure out the statistics of each entry.

# Pandas_Analysis
-	Importing both the modified and pre-modified datasets. Modified dataset = the dataset with the dropped Categorical/Continuous features decided in the previous file.
-	Used general Pandas library functions including “.describe”, “.groupby”, and “.pivot_table”

# Hypotheses on Data
- Conducting different hypotheses on data and using suitable statistical testing methods based on the columns selected for the hypothesis

# Outliers
- Finding the outliers on modified and pre-modified data using isolation forest
-	Using Z-score to find outliers between the features of the modified data and the target variable “Credit_Score”.
-	Plotting the Z-score outlier test output.

# Recursive Feature Elimination (RFE)
-	Building an RFE model paired with a random forest classifier. 
-	Eliminating the features until the 5 most important features are left across 5 folds.
-	Finding the permutation/ Feature importance for the 5 remaining features resulting from the recursive elimination and plotting the results.
-	This is performed on the pre-modified data

# Modified data and pre-modified data
- Modified data:
- Data where we dropped one of two features with high correlation. Name = “After_dropping_corr_features2”
  
- Pre-modified data:
- Data without the dropped columns. Name = “data_encoded”






