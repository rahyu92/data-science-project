# Executive Summary 

There has been a rise in the demand of online delivery in the metropolitan cities such as Bangalore in India. The question about why this increase in the demand has always been a lingering question. So a survey is conducted to know more the customers that used such services.

Following supervised machine learning models are created from this survey to predict the following
- whether customer will reorder again
- text classifier where customer do not reorder again 

# Data Dictionary

Dataset used can be found via [link](https://www.kaggle.com/benroshan/online-food-delivery-preferencesbangalore-region)

# Conclusion

**Churn Model**

Model|Accuracy|	AUC|Recall|	Prec.|F1|
--|--|--|--|--|--|
ExtraTreesClassifier(train)|0.9521|0.9356|	0.9863|	0.9556|	0.9706|
ExtraTreesClassifier(test)|0.9145|0.9405|	0.9643|	0.9205|	0.9419|
Random Forest(train)| 0.9410|0.9331|0.9908|	0.9391|	0.9641|
Random Forest(test)|0.8974	|0.9177|0.9643 |0.9000|	0.9310|	

**Text Classifier**

Model|Accuracy|AUC|R2|
--|--|--|--|
Logistic Regression(test)|0.83|0.85|0.82|
MultiNomial(test)|0.83| 0.82|0.82|0.82|  


After tuning model the best two models, ExtraTreesClassifier is still the best model as they have highest Accuracy + Recall rate and the log loss between train and test is smaller as compare to Random Forest. 

From the best churn model, seems like the following top 3 features: ease and convenient_disagree,time saving_disagree,more restaurant choices_disagree that customers will determine if they will reorder again from the vendor or not in the food delivery app. 

For text classifier, the results are very close and similar. However, logistic regression have lesser log loss between train and test as compared to multinomial thus it is a preferred model. Where output is == No, seems like customers top two comments are faster and poor perhaps to indicated that delivery should be faster and poor service.
