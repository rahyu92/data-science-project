# Subreddit Classifier
---

## Problem Statement

Apple and Samsung have been each other's competitor for the longest time since the birth of smart phones was released. They release new products especially smart phones every year at a specific date and time to launch their products.

Tech magazines will then use this oppurtunity to review newly product launched and compare them based on their verdict and issues found. As a data science professional 
working for a tech magazine , they would like to know from reddit what products and trend topics are mostly talked about by users in a specific time.

This project is created with supervised learning models that is trained on existing data from each Subreddit.  The best model is selected with the best accuracy and can continue to train on new data for new posts to enhance its accuracy.

## Executive Summary 
Every year, apple and samsung released new products and have a specific date and time on their launch day. With being the top players for smart phones, competition is indeed fierce between them. Understanding the text through NLP of two subreddits are used as starting points for classification.

Data is scrapped by scrapping post from this two subreddits and then training the model on 75% of the data and subsequently the other 25% as the unseen test set to evaluate the model performance. Following models are being used:

- Logistic Regression
- Naive-Bayes Classifier
- Random Forest Classifier

After the training and testing, Random Forest performed the best in terms of the accuracy score. But in terms of the interpretability of the features and that it includes nearby words as well, Naive-Bayes Classifer is ultimately the model of choice for this classification problem.

## Data Dictionary
|Column Name| Type | Description |
| ---| ---| ---| 
|author| object| author of the post|
|selftext| object | Further description of the post |
|subreddit| object|  Category of the subreddit post|
|title| object | Title of the post |
# Conclusion 

|Model| Training Test    | Test Score |  ROC AUC Score |
| ----------- | ----------- | ----------- |   ----------- |
| Logisic Regression | 0.98    |       0.90     |   0.96 | 
|Naive-Bayes   | 0.90     |   0.89       |   0.96 |
|Random Forest|  1.0 |  0.91  |   0.97 |

### Best Model 
The best model in terms of test score will be the Logistic Random Forest with  ROC AUC score of 0.97 which is pretty close to the other models. In general, their misclassification class also does not differ much. 

However, the chosen and winner model will be Naive-Bayes model. Looking at the scores, despite having the lowest score, the test and train model scores only have a loss of 0.01 with still a goof ROC  score of 0.96 which shows it does not overfit and generalize well. It clearly specify the top features by the the subreddit and recognise the bigrams in each class that are rank higher in each category.

Despite Random forest having the best scores, it overfits with 0.09 loss and the words does not classify well which word belongs to which reddit. 

### Recommendations

Using naive bayes model can help to indicate what are the current trends and topic are posted by users at a specific time. However, it is not sufficient to indicate the sentiment of the post where it is positive or negative.

Additionally, extracting their sentiment will be good to know the post is based determined by the attitude or the emotion of the writer due to them being rivals, there will be tendency of users posting negatively about the other brand . 
