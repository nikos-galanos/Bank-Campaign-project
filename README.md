# Bank-Campaign-project
This project was completed by Nikos Galanos and Ahmad Hussain, two Master of Business Analytics candidates from MIT, for the course 15.095 - Machine Learning through a Modern Optimization Lens with Dr. Dimitris Bertsimas.

## Introduction

With the advent of digital banking, traditional banking channels like branches and ATMs are fast becoming obsolete, and customers are now more demanding and dissatisfied than ever before. The financial disruptions due to the COVID-19 pandemic created unique opportunities and challenges for economic inclusion, some of which may be temporary, while others may be longer lasting. According to a 2021 FDIC survey the use of new digital products offered by banks has inclined and this gives the opportunity to banks to compete not only on interest rates but on other offerings and bundles. To achieve the best results, the banks should carefully design their marketing campaigns and pick their target audience.

## Problem Summary
The goal of our project is to predict whether a customer will convert after being targeted by a telephone marketing campaign from a banking institution offering a bank term deposit. Our problem could easily be generalized to other organizations and for other ways of approaching the customer. Given the goal of minimizing the resources in terms of money, time and personnel that each institution utilizes in their attempt to maximize profits, we believe that the problem of identifying the customers that are more prone to a new offering and
targeting them is of crucial significance.

## Data
For our project we will use a dataset hosted at UCI Machine Learning Repository with data related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The dataset provided consists of 41,188 rows, with each row corresponding to a call with a customer. For each call we have 21 features related not only to customer and campaign characteristics but also with some market indexes such as the Euribor index and the Consumer Price Index. The variable (FinalOutcome) to predict is whether a customer will subscribe to a term deposit, making our problem a classification problem.

## Further Methods

### Interpretable Clustering

In addition to predicting the outcome of the campaign for each individual customer, Interpretable clustering techniques are applied utilizing KMeans and Optimal Classification Trees as described in the following paper:

Bertsimas, D., Orfanoudaki, A. and Wiberg, H. (2020) ‘Interpretable clustering: An optimization approach’, Machine Learning, 110(1), pp. 89–138. doi:10.1007/s10994-020-05896-2. 

The clustering approach can give us an overview of our customer database, separating our customers in different segments. The bank (or each organization applying similar techniques) can utilize these findings to identify the different types of customers on their customer database and pursue different marketing and sales initiatives in order to increase their conversion rates.

In our case, we could characterize the identified clusters as:

1) Individuals with university degrees who are currently active in their jobs
2) Individuals without any level of education
3) Individuals with high school education who are active in their jobs
4) Retired individuals with university degree or high school education
5) Individuals with only a basic 6 years education
6) Individuals who are currently working without a university degree but with a professional course

Banks can unlock strategic advantages by designing tailored products per market segment. For example, cluster 6 identifies freelances as a particular target group.


### Prescriptive Tool on channel to contact (




For a detailed overview of our methods and findings, please see the report found in the repo entitled Report.pdf or the slide deck entitled Presentation.pdf. Thanks!
