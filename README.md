# Churn Bank for the preliminary classification JOB23
--------

## Table of Contents

- [Repository Content](#repository-content)
- [Quick Start](#quick-start)
- [Description of the Task](#description-of-the-task)
- [Decision-making process](#decision-making-process)
    - [Data Pipeline](#data-pipeline)
- [Conclusions](#conclusions)



## Repository Content 

    - Predictions in json file
    - Jupyter Notebook with the script

#### [top](#table-of-contents)
--------
## Quick Start

This project was done in a Jupyter Notebook but the model training was done from google Colab since they offer free GPUs and TPUs[^1] in case you want to save some time :wink:.

* <a href="https://colab.research.google.com/github/Freegalado/Sport_Image_Classification_I/blob/main/Talent_Squad_Data_Science_II.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

if you want to open it in locally don't forget to have installed:

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/-Seaborn-blue?style=for-the-badge&logo=seaborn) 


#### [top](#table-of-contents)
--------



## Description of the task

We are a bank that has a database with a large amount of information about our customers. Our goal is to help analysts predict the churn rate of these customers in order to reduce it. The database includes demographic information such as age, gender, marital status and income category. It also contains information on card type, number of months in portfolio and inactive periods. In addition, it has key data on the spending behavior of customers approaching their cancellation decision. Among the latter information are the total renewable balance, the credit limit, the average open-to-buy rate and analyzable metrics such as the total amount of change from the fourth quarter to the first quarter or the average utilization rate.

Against this data set we can capture up-to-date information that can determine the long-term stability of the account or its imminent exit. The Attrition_Flag must be predicted.

**The evaluation objectives will be:**

    1. Increase of samples in the images. 

    2. Calculate the macro F1-score. 



  #### [top](#table-of-contents)
--------

 ## Decision-making process
  


Being able to predict which individual customers are likely to abandon the bank's services is quite important, as it can be more expensive to acquire a new customer than to keep old ones. The behavior of each customer at a given point in time can be used to predict how high the risk of losing them in the future might be.

If we know which customers are most at risk of dropping out, we can better target our rescue efforts. For example, we can target these customers with a marketing campaign, reminding them that they haven't bought from us in a while, or even offering them a benefit.

This is a binary classification problem that divides customers into two groups: those who are leaving and those who are not. You can use a supervised machine learning classification model, being careful because the churn is very low for most companies, so it is a problem with unbalanced data, also it is not enough to look at the accuracy of the churn model, so the type of metric to try to maximize is the F1 macro.



  #### [top](#table-of-contents)
--------
#### Data Pipeline

  
  ![Data-pipeline_bank](https://user-images.githubusercontent.com/91080406/231605394-ee2bb067-bf94-4e91-9b8c-59d12642d163.png)


To perform the task, different activities were carried out in 4 stages:

    - In the first stage, the libraries needed to perform the different tasks are loaded, the data are loaded and an exploratory analysis will be performed,  finally the data will be split before any preprocessing.

    - In the second stage, the categorical features are preprocessed, a data balancing procedure is performed on the target variable and a feature importance process is carried out to select those that are necessary to predict the customers that may abandon the bank's service.

    - In the third stage, the different models are trained and evaluated to understand their behavior, selecting the best model.

    - In the fourth stage, the model that has delivered the best F1-macro score is selected to subsequently classify new clients data.


#### [top](#table-of-contents)
--------
## Conclusions

![model_metrics](https://user-images.githubusercontent.com/91080406/232925525-c2941317-bf1c-4edc-a872-8ea628cf7739.png)




The RF and XGB model have almost the same f1 score, with the XGB being slightly higher (**0.937233**), but has a greater reduction of false negatives. 


![false_negatives](https://user-images.githubusercontent.com/91080406/232925216-e2977ea1-a4bd-4fbb-8074-1cdfed2610a6.png)

XGB is chosen because of its slight increase in f1 score but undoubtedly the reduction in false negatives is something of great importance as it represents customers that the model classifies as satisfied with the bank’s service but are really customers who are likely to cease using the bank’s services. 


#### [top](#table-of-contents)


[^1]: In order to offer computational resources at no cost, Colab needs to retain the flexibility to adjust usage limits and hardware availability at any time 
