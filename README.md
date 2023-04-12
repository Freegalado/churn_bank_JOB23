# Churn Bank for the preliminary classification JOB23
--------

## Table of Contents

- [Repository Content](#repository-content)
- [Quick Start](#quick-start)
- [Description of the Task](#description-of-the-task)
- [Decision-making process](#decision-making-process)
    - [Data Pipeline](#data-pipeline)

- [Final Thoughts](#final-thoughts)



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

  ![Data-pipeline](https://user-images.githubusercontent.com/91080406/191982034-bd65086b-8e39-4e3c-a59d-986e32251e3c.png)


To perform the task, different activities were carried out in 4 stages:

- In the first stage, the libraries needed to perform the different tasks are loaded, the images (files) are loaded and an exploratory analysis will be performed on these, then they will be transformed to data suitable for the task in this case a matrix, finally some kind of pre-processing will be performed.

- In the second stage, different CNN models are built, a pre-trained model is loaded to perform a model with learning transfer, the error function to be used in both types of models is defined.

- In the third stage, the different models are trained and evaluated to understand their behavior.

- In the fourth stage, the model that has delivered the best F1-macro score is selected to subsequently classify the images.


#### [top](#table-of-contents)
---------
## Final Thoughts

It is my first time to make an image classification model, which helped me to learn a lot about the subject, there are processes to improve. It is the first time that I use the Google Colab platform, I usually work on my laptop, which already needs a replacement, but this time I had to look for another alternative to carry out the project. The models are not complex models but the difference in training time between local and cloud-based service is noticeable.

This is my fisrt time to participate the [NUWE](https://nuwe.io/dev/challenges) platform and I think I will become a regular user of its mini-projects (challenges) in order to keep improving my skills.

#### [top](#table-of-contents)
 

[^1]: In order to offer computational resources at no cost, Colab needs to retain the flexibility to adjust usage limits and hardware availability at any time 
