# Executive Summary

Big industry players that provide cloud computing services such as Amazon and Google have been releasing Machine Learning as a service(MLaaS) where machine learning models can be created by few clicks away. With such technology and services available, this disrupts the industry as less manpower is needed to analyse provide predictions. 
Currently, the company is the midst in expanding their infrastructure and department is interested in looking whether it is worth to include such services to reduce workload.

With a provided sample data from the previous year, the management would like the following outcome to further expedite their decision:
1.   Supervised classification model in classifying the accident severity and compare the outcome together with a codeless AI platform 
2.   Explore other related services provided that can be used by the analytics department and if its beneficial to the team

# Data Dictionary

Data dictionary can be found via [link](https://github.com/rahyu92/data-science-project/blob/main/capstone/data/road-safety-lookups.csv).
Following new features are added:

Column Name| Type| Description|
--|--|--|
Season| Object| Describe the season weather based on day of the year|
Hour| Integer | Hour based on time|
Month| Integer | Month based on calendar|
Coords | Object| Coordinates from latitude and longitude|

# Dashboard created with Data Studio

![alt text](https://github.com/rahyu92/data-science-project/blob/main/capstone/code/dashboard_image.PNG)
DataStudio is one of the free services by Google that enables users to create customizable informative reports and dashboards.
This dashboards can be created using various data source such as via file upload, Google Sheets, BigQuery, etc. <br/>
This various options shows that this service does not fully depend on specific type of document or services only used by Google.<br/>
This tool definitely helps the department to access the created dahsboard with just a link at anytime and also allow users to collaborate concurrently.<br/>
To access and interact with the dashboard, please click on  [link](https://datastudio.google.com/reporting/7ad8ff1d-6f16-401f-ad59-c178c760a0d0)

# Conclusion

Google cloud platform provide many services that allows users to perform many business activities just by clicks away with data that can be retrieved remotely. Users in any department can make business decisions from creating visualizations dashboard for analytics ,machine learning models, storing of documents and database all using the same services.

Model|  ROC AUC| Recall|  Precision | F1 Score|
--|--|--|--|--|
Light Gradient Boosting Machine(Train)|	62.94%|	33.8%|70.8%|	69.5%	|
Light Gradient Boosting Machine(Test)	| 65.9%	|33.9%|	74.5%|	68.9%	|
Vertex AI| 91%| 38.4% | 78.5%| 78.4%|

Based on this experiment, Vertex AI have provided better outcomes having Precision 78.5% Recall, F1 Score 78.4%91% and 91% ROC AUC as compared to best model from pycaret where the training model is only at 70.8% for Precision and 69.5% F1 score at their best. 

However, there seems to be limitations in using Vertex AI, a MLaaS provided by Google. Using AutoML model have limited selection in creating pipeline and there is no transparency and visibility what was in the process and consideration of the model to provide the outcome. Even if the outcome is good, it may not always be accurate or fit the objective of the experiment. They also have different price point per node for different model type  [(Link for pricing of Vertex AI)](https://cloud.google.com/vertex-ai/pricing#video-data). This price does not include other related services such as Kubernetes needed where users can can deploy exisitng model to allow prediction models online . If not careful on the hours,number of nodes concurrently used and usage of other related services, it is possible that the department will spend too much money just on using such services.

# Next Step and Recommendations

As this project is limilited to only using AutoML option, the next step is to deploy the saved model in a container and create a custom training model using the pre built containers to further explore and compare results from AutoML to further justify if using this MLaaS from Google or other similar providers are indeed worth the investment with the consideration of price.

Creating machine learning models from Python libraries allow data scientist and analyst to enhance their experiment by knowing what was done to the model and parameters selected comparing to a codeless machine that shows only outcomes of the model and have limited selection. Still, related cloud services like containers and visualization tools are beneficial and should be considered  as many users in the team can collaborate,view and work together with resources provided online . 
