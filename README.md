
# Microsoft : Classifying Cybersecurity Incidents with Machine Learning

This repository contains a machine learning-based project to classify cybersecurity incidents. The goal is to use machine learning algorithms to identify and categorize different types of security events, helping organizations to detect and respond to threats more efficiently.

### Tech stack
- python
- Machine learning algorithms


## Data Exploration 

Initial data Exploration has been done to analyse the size and structure of the dataset. 


## Data Features 

- OrgId
- IncidentId
- AlertId
- DetectorId
- AlertTitle
- Category
- EntityType
- EvidenceRole
- DeviceId
- IpAddress
- Url
- DeviceName
- NetworkMessageId
- RegistryKey
- OAuthApplicationId
- ResourceIdName
- Day
- Month

## Target 
- IncidentGrade [TruePositive , FalsePositive , BenignPositive]

## EDA(Exploratory Data Analysis) 

EDA(Exploratory Data Analysis) shows that there is some imbalance in the target data. SMOTE(Synthetic Minority Over-sampling Technique) is done to treat the imbalance which will improve the model prediction accuracy. imbalance in data will result in a baised prediction and inaccurate output.

## Feature scaling 

Encoding technique has been done to convert categorical values to numerical values using an sklearn library called Labelencoder. This helps the model to understand the dataset.

## Train Test Split 
The dataset has been divided into a **4:1** ratio, with X as the features and Y as the target, to prevent overfitting and underfitting.

## Models 
On running multiple models with this dataset the model **accuracy score , f1 score , recall score , Precision score** and predictions were recorded , to select the best fit for this dataset.
    
#### LogisticRegression   
- Accuracy : 50.36        
- Recall : 50.36       
- Precision : 51.16         
- f1 score : 48.82
#### DecisionTree       
- Accuracy : 94.71        
- Recall : 94.71       
- Precision : 94.72         
- f1 score : 94.70
#### RandomForest      
- Accuracy : 94.62        
- Recall : 94.62       
- Precision : 94.64         
- f1 score : 94.62
#### GradientBoosting       
- Accuracy : 79.96        
- Recall : 79.96       
- Precision : 81.03         
- f1 score : 80.06

### Hyperparametric Tunning 
Hyperparametric tunning has been done to imporvise the model accuracy and predictions using **RandomizedSearchCV** an inbuilt sklearn library used to fine tune the models.
#### DecisionTree  
- Accuracy : 92.00        
- Recall : 92.00       
- Precision : 92.03       
- f1 score : 92.00
#### RandomForest  
- Accuracy : 86.66        
- Recall : 86.66       
- Precision : 87.21       
- f1 score : 86.72
#### XGBClassifier  
- Accuracy : 95.69        
- Recall : 95.69       
- Precision : 95.69       
- f1 score : 95.69
#### why this project?
The main goal of this project is to identify different types of security events with machine learning algorithms to help organization detect threats and malicious activity and prevent them from cyberattacks.
#### why these features?
After thoroughly analyzing the dataset, the features above show a stronger correlation with each other.
#### Why XGBClassifier model? 
The XGBClassifier demonstrates enhanced accuracy after hyperparameter tuning and produces fewer errors compared to other models.



