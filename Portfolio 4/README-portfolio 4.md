# Analysis of Obesity Level based on Eating Habits and Physical Conditions

## Introduction

### Objectives
The objective of this analysis is to know the factors that contribute to the obesity level status the most and analyze the cluster based on the obesity level.

### Data Description

|Variable|Meaning|Category|
|:-----:|:-----:|:-----:|
|Gender|Female and Male|Other|
|Age|Age of Individual|Other|
|Height|Height of Individual (metres)|Other|
|Weight|Weight of Individual (kilograms)|Other|
|family_history_with_overweight|A family member has suffered or suffers from overweight|Other|
|FAVC|Frequent consumption of high caloric food|Eating habits|
|FCVC|Frequency of consumption of vegetables|Eating habits|
|NCP|Number of main meals|Eating habits|
|CAEC|Consumption of food between meals|Eating habits|
|SMOKE|cigarette users|Other
|CH2O|Consumption of water daily|Eating habits|
|SCC|Calories consumption monitoring|Physical condition|
|FAF|Physical activity frequency|Physical condition|
|TUE|Time using technology devices|Physical condition|
|CALC|Consumption of alcohol|Eating habits|
|MTRANS|Transportation used|Physical condition|
|NObeyesdad|Obesity level|Other

## Data Processing - describe in detail how the processing data and the tools / techniques we use
1. Data Exploration
    - Import dataset and tools such as panda, seaborn, numpy, matplotlib.
    - Check if there is any outlier and missing value, but dataset already cleaned.
    - Label encoding for text variable into binary variable.
      
2. Correlation
    - Correlation Analysis with 'NObeyesdad' as Target Variable
      
3. KMeans Clustering
    - The provided visualizations from the K-means clustering analysis show distinct lifestyle clusters within the dataset. Also analyse through elbow method to find the right number of clusters.

4. Logistic Regression
    - This regression is used for binary or categorical target variables where the outcome falls into discrete classes. In the context of obesity, logistic regression would be used if the target variable is categorical, such as predicting whether an individual is obese or not based on a binary classification. Because the target variable we are using in this model is **"NObeyesdad"** is a categorical data, so logistic regression is chosen for the analysis of this model.

5. KNN model
    - I decided to use KNN model to do model comparison that will allows to compare their performance on the same dataset. Logistic Regression might perform better when the decision boundary is linear, while KNN might excel when the decision boundary is non-linear. Aside from that logistic regression can help understand which features are significant predictors of the outcome, whereas KNN can capture interactions between features that Logistic Regression might miss.

6. RFE
    - This feature selection technique in Python used to select the most significant features in a dataset for predictive modeling. It recursively fits a model and removes the least important features until the specified number of features is reached. This process helps improve the model's performance by reducing overfitting and enhancing generalization.

## Conclusion

The training and test accuracy of logistic regression for the model are quite promising and suggest that the model performs well. However, when logistic regression data compared to KNN model, it reveals that logistic regression appears more stable and generalizable under the current setup.
Nonetheless, in correlation analysis shown that "Weight", "CAEC", "family_history_with_overweight" and "Age" has the strongest correlation with the obesity level, but after running RFE analysis, it shown that "Weight", "Height", "Gender" and "FCVC" are the top features that impacted the obesity level.
