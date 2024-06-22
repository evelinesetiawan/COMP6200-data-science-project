# Analysis of Mobile Price Data

## Introduction

### Objectives
The objective of this analysis is to analyze mobile price data. This portfolio will train classification models to predict mobile phone prices and evaluate the strengths and weaknesses of these models. 

### Data Description
|Column|Meaning|
|:-----:|:-----:|
|battery power|Total energy a battery can store in one time measured in mAh|
|blue|Has bluetooth or not|
|clock speed|speed at which microprocessor executes instructions|
|dual sim|Has dual sim support or not|
|fc|Front Camera mega pixels|
|four g|Has 4G or not|
|int memory|Internal Memory in Gigabytes|
|m dep|Mobile Depth in cm|
|mobile wt|Weight of mobile phone|
|n cores|Number of cores of processor|
|pc|Primary Camera mega pixels|
|px height|Pixel Resolution Height|
|px width|Pixel Resolution Width|
|ram|Random Access Memory in Mega Bytes|
|sc h|Screen Height of mobile in cm|
|sc w|Screen Width of mobile in cm|
|talk time|longest time that a single battery charge will last when you are|
|three g|Has 3G or not|
|touch screen|Has touch screen or not|
|wifi|Has wifi or not|
|price range|This is the target variable with value of 0(low cost), 1(medium cost), 2(high cost) and 3(very high cost)|

## Data Processing
1. Explore the data
   Remove missing and null values.

2. Correlation between 'price range' with other features
   Choose certain helpful variable for predicting the price range.

3. Split the dataset (Training set : Test set = 8 : 2)
   Split dataset in selected features and target variable.

4. Train a logistic regression model and calculate the accuracy of the model
   train the model with logistic regression between price_range and 4 correlated variables

5. Train a KNN model

6. Tune the hyper-parameter K in KNN
   (Hints: GridsearchCV)

for visualization: You can use line chart to visualize K and mean accuracy scores on test set.

## Conclusion
After doing training and test accuracy using logistic regression, the results come out around 0,9, with 0,01 points lower of training accuracy than the test accuracy. To summarize, 0,97 result of test accuracy display the model rightly predict 97% of test dataset and it applies the same with training accuracy where the model forecast 95% justly of training dataset.

Based on description above, the numbers of training and test accuracy both shows that the model perform well because the model is not overfitting the training data and is capturing underlying pattern effectively.
