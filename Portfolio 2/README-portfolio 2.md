# Analysis of an e-commerce dataset part 2

## Introduction

### Objectives
The objectives of this portfolio are to train linear regression models to predict users' rating towards items. This involves a standard Data Science workflow: exploring data, building models, making predictions, and evaluating results. In this task, we will explore the impacts of feature selections and different sizes of training/testing data on the model performance. The dataset use in this portfolio is same as portfolio 1 and has been cleaned.

### Data Description
This dataset includes a wealth of information for each user. Details such as their profile, ID, gender, city of birth, product ratings (on a scale of 1-5), reviews, and the prices of the products they purchased are all included. Moreover, for each product rating, we have information about the product name, ID, price, and category, the rating score, the timestamp of the rating and review, and the average helpfulness of the rating given by others (on a scale of 1-5).
The dataset is from several data sources, and we have merged all the data into a single CSV file named 'A Combined E-commerce Dataset.csv'. The structure of this dataset is represented in the header shown below.

| userId | gender | rating | review| item | category | helpfulness | timestamp | item_id | item_price | user_city|

    | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |  ---- |  ---- |  

## Data Processing
1. Explore the Dataset
   Since dataset have cleaned, Use the methods, i.e., `head()` and `info()`, to have a rough picture about the data, e.g., how many columns, and the data types of each column.
   * As our goal is to predict ratings given other columns, we will get the correlations between certain variable. In this data we will use helpfulness/gender/category/review and rating by using the `corr()` method.
     *Hints: To get the correlations between different features, you may need to first convert the categorical features (i.e., gender, category and review) into numerial values. For doing this, you may need to import `OrdinalEncoder` from `sklearn.preprocessing` (refer to the useful examples [here](https://pbpython.com/categorical-encoding.html))*

2. Split Training and Testing Data
   Machine learning models are trained to help make predictions for the future. Normally, we need to randomly split the dataset into training and testing sets, where we use the training set to train the model, and then leverage the well-trained model to make predictions on the testing set.
   To further investigate whether the size of the training/testing data affects the model performance, please random split the data into training and testing sets with different sizes:
     * Case 1: training data containing 10% of the entire data;
     * Case 2: training data containing 90% of the entire data

3. Train Linear Regression Models with Feature Selection under Cases 1 & 2
   When training a machine learning model for prediction, we may need to select the most important/correlated input features for more accurate results.
   To investigate whether feature selection affects the model performance, please select two most correlated features and two least correlated features from **helpfulness/gender/category/review regarding rating**, respectively.

   Train four linear regression models by following the conditions:
    - (model-a) using the training/testing data in case 1 with two most correlated input features
    - (model-b) using the training/testing data in case 1 with two least correlated input features
    - (model-c) using the training/testing data in case 2 with two most correlated input features
    - (model-d) using the training/testing data in case 2 with two least correlated input features
    
   By doing this, we can verify the impacts of the size of traing/testing data on the model performance via comparing model-a and model-c (or model-b and model-d); meanwhile the impacts of feature selection can be validated via comparing model-a and model-b (or model-c and model-d). 

4. Evaluate Models
   Evaluate the performance of the four models with two metrics, including **MSE** and **Root MSE** and print the results of the four models regarding the two metrics

5. Visualize, Compare and Analyze the Results
   Visulize the results, and perform ___insightful analysis___ on the obtained results. For better visualization, you may need to carefully set the scale for the y-axis.

## Conclusion
Compared to model A and Model C, the numbers show that between these 2 model, model C prediction's are closer to the real value. As for model B and model D, figures display that model D has smaller value than model B, which again reflect better overall performance. To summarize, this training obtain the similar observation, by using the most correlated input variables into training data will produce the better results.
