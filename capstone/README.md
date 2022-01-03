# Executive Summary

Big industry players that provided cloud computing services such as Amazon and Google have been releasing Machine Learning as a service(MLaaS) where machine learning models can be created by few clicks away. With such technology and services available, this disrupts the industry as less manpower is needed to analyse provide predictions. 
Currently, the company is the midst in expanding their infrastructure and department is interested in looking whether it is worth to include such services to reduce workload.

With a provided sample data from the previous year, the management would like the following outcome to further expedite their decision:
1.   Supervised classification model in classifying the accident severity and compare the outcome together with a codeless AI platform 
2.   Explore the related services provided that can be used by the analytics department and if its beneficial to the team

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
DataStudio is one of the free services that Google provided that enables users to create customizable informative reports and dashboards.
This dashboards can be created using various data source such as via file upload, Google Sheets, BigQuery, etc. <br/>
This various options shows that this service does not fully depend on specific type of document or services used by Google.<br/>
This service definitely helps the department to access the created dahsboard with just a link at anytime and also allow users to collaborate concurrently.<br/>
To access and interact with the dashboard, please click on  [link](https://datastudio.google.com/reporting/7ad8ff1d-6f16-401f-ad59-c178c760a0d0)

# Conclusion

Google cloud platform provide many services that allows users to perform many business activities just by clicks away with data that can be retrieved remotely. Users in any department can make business decisions from creating visualizations dashboard for analytics ,machine learning models, storing of documents and database all using the same services.

Model| Precision Score| F1 Score| ROC AUC|
--|--|--|--|
Light Gradient Boosting Machine(Train)|	62.94%|	0.3388	|0.7085|	0.6954	|
Light Gradient Boosting Machine(Test)	0.6588	|0.3389|	0.7455|	0.6899	|
Vertex AI| 78.5% | 78.4%91%| 91% |

Based on this experiment, Vertex AI have provided better outcomes having Precision 78.5% Recall, F1 Score 78.4%91% and 91% ROC AUC as compared to best model from pycaret 

However, there seems to be limitations in using Vertex AI, a MLaaS provided by Google. Using AutoML model have limited selection in creating pipeline and there is no transparency and visibility what was in the process and consideration of the model to provide the outcome. Even if the outcome is good, it may not always be accurate or fit the objective of the experiment. They also have different price point per node for different model type  [(Link for pricing of Vertex AI)](https://cloud.google.com/vertex-ai/pricing#video-data). This price does not include other related services such as Kubernetes where users can used to also deploy customize pipeline and to test prediction models online . If not careful on the hours,number of nodes concurrently used and usage of other related services, it is possible that the department will spend too much money just on using such services.


To enable such selection, a custom model is required to be deployed in a container that consist of existing python training application using libraries such as tensorflow.

As using python libraries such as PyCaret allows to save model which saves the entire transformation pipeline, the suggestion will be to still use a python library to create a data science model and  load this model in a kubernetes container in using provided service by google or other cloud computing services so online prediction can be made from many users and also use this loaded model for custom training. This also allows data scientist and analyst to have transparency and control in what goes to the model.

Creating machine learning models from Python libraries allow data scientist to enhance their experiment by knowing what was done and parameters selected comparing to a codeless machine that shows only outcomes of the model and have limited selection. Still, cloud services are beneficial to the team as many users can collaborate and work together with resources provided online with all this services availale.

