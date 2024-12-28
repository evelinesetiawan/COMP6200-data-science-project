# Analysis of an e-commerce dataset
## Introduction
In this dataset, each user has the ability to post a rating and review for the products they purchased. Additionally, other users can evaluate the initial rating and review by expressing their trust or distrust.

### Objectives
The objectives of the analysis in this portfolio is to apply the knowledge that have been learned such as descriptive statistics, plotting, correlation and outliers detection.

### Data Description
This dataset includes a wealth of information for each user. Details such as their profile, ID, gender, city of birth, product ratings (on a scale of 1-5), reviews, and the prices of the products they purchased are all included. Moreover, for each product rating, we have information about the product name, ID, price, and category, the rating score, the timestamp of the rating and review, and the average helpfulness of the rating given by others (on a scale of 1-5).
The dataset is from several data sources, and we have merged all the data into a single CSV file named 'A Combined E-commerce Dataset.csv'. The structure of this dataset is represented in the header shown below.

| userId | gender | rating | review| item | category | helpfulness | timestamp | item_id | item_price | user_city|

    | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |  ---- |  ---- |  
    

## Data Processing
1. Removing missing data
    - will remove the data if there is one or more data that is not complete
2. Descriptive statistics
    - doing the calculation of descriptive statistics with the predetermined variables 
3. Plotting
    - explore the correlation between gender/helpfulness/category and ratings and visualize with graph/plot.
4. Outliers detection

## Conclusion
The dataset contains 20.000 data which in each row contain unique information from userId to user_city. After removing missing data and rows that do not have reviews, the number of data decreased to 19.916 data. Based on those numbers, I found 8.562 unique users, 19.459 unique reviews, 89 unique items, and 9 unique categories. Further, I calculated descriptive analytics of rating records and found the average rating was around 3,7. As per gender calculation, it was shown that men tend to give more reviews than women.
Overall the observations of rating and other variables did not give the users much significant impact, since the results shown in the boxplot were constant and quite similar between variables.
