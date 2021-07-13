# NLP Case Study - Amazon Fine Foods Review (Text Vectorization/Featurization Techniques)

Efficient sentence encoding and vectorization techniques with customer reviews on a product page of the popular E-Commerce website, Amazon using proven NLP techniques for the purpose of sentiment analysis. The resulting sentence vectors can be easily used with any popular linear/non-linear classification techniques, decision-tree based methods, ensemble methods or neural networks. 

**This is just an implementation of the state-of-the-art text featurization techniques.**

## Objective

Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

Since the product rating out of 5 is also given, we can use this score to deduce the posivity/negativity for ground truth. A rating of 4 or 5 could be cosnidered a positive review. A review of 1 or 2 could be considered negative. A review of 3 is nuetral and ignored. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

## Dataset

[Dataset Link](https://www.kaggle.com/snap/amazon-fine-food-reviews)

The dataset is available in two forms 
1. .csv file 
2. SQLite Database

In order to load the data, We have used the SQLITE dataset as it easier to query the data and visualise the data efficiently.
Here as we only want to get the global sentiment of the recommendations (positive or negative), we will purposefully ignore all Scores equal to 3. If the score id above 3, then the recommendation wil be set to "positive". Otherwise, it will be set to "negative".

### Dataset Details 

[Basic EDA Reference Blog](https://nycdatascience.com/blog/student-works/amazon-fine-foods-visualization/) 

The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.

**Number of reviews:** 568,454
**Number of users:** 256,059
**Number of products:** 74,258
**Timespan:** Oct 1999 - Oct 2012
**Number of Attributes/Columns in data:** 10 

#### Attribute Information:

1. Id
2. ProductId - unique identifier for the product
3. UserId - unqiue identifier for the user
4. ProfileName
5. HelpfulnessNumerator - number of users who found the review helpful
6. HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not
7. Score - rating between 1 and 5
8. Time - timestamp for the review
9. Summary - brief summary of the review
10. Text - text of the review
