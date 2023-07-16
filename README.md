# Predicting marketing campaign's potential clients for a bank
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


### A Prescriptive Tool on the best channel to contact a customer (call vs email)

The techniques here utilize the following paper:

Amram, M., Dunn, J. & Zhuo, Y.D. Optimal policy trees. Mach Learn 111, 2741–2768 (2022). https://doi.org/10.1007/s10994-022-06128-5


Our ultimate objective here is to decide the best medium to use for contacting a customer in order to maximize the number of people who make a deposit. To achieve that we utilize the feature “contact” which originally had the values “cellular” and “telephone” in a 2:1 ratio, and we just switch the “telephone” value to “email” in order to make our problem more realistic. Our objective now is to maximize the number of deposits by contacting the customer with the right medium. To achieve this objective, we utilize Optimal Prescriptive Policy Trees by IAI, assigning as outcome whether a customer made a deposit, as x the customer features and as treatment the medium used.

In prescription problems, it is complicated to evaluate the quality of a prescription policy because our data only contains the outcome for the treatment that was received. To resolve this, we utilize reward estimation, where so-called rewards are estimated for each treatment for each observation. These rewards indicate the relative credit a model should be given for prescribing each treatment to each observation, and thus can be used to evaluate the quality of the prescription policy.

## Key Findings

Our key findings can be decomposed across two different sections: the first outlines the promise that interpretable clustering offers in terms of building a cohesive understanding of customer segments and the second underscores the predictive power that modern classification techniques possess and how to harness them in efficient manners. Finally, we showcased how prescriptive approaches could lead to significant improvements on how business is conducted, leading to exceptionally better results.

Interpretable clustering through the use of optimal classification trees can be seen as a powerful tool in breaking down total user base into neatly defined business categories. By closely identifying the variables that determine the composition of each different cluster, we are able to provide actionable insights into how to plan marketing calls for each different segment. Tailoring the product pitch to each different cluster can ensure that marketing agents offer each customer the term deposit in a manner that maximizes their likelihood of conversion and hence leads to higher returns for each dollar spent on marketing.

In terms of prediction methods, we can better understand the likelihood of individual customers being converted. Our methods have shown that it is possible to predict this problem to high accuracy levels and hence we remain confident in utilizing such techniques to rethink customer targeting strategies. For example, from a business perspective, we could choose to rank prospective customers according to the likelihood of their conversion and as opposed to randomly calling users, we could focus in descending order on users that based on our model are more likely to convert. This not only means that we are able to convert low hanging fruit in the early phases but has crucial repercussions for cost savings in turbulent economic
environments: when banks are looking to curtail marketing expenses, we can offer comparable levels of conversion in terms of absolute number for lesser calls made. This remains conjecture at this point but based on the promise embodied by our models, we are confident that with the right execution, this hypothesis should hold true.

In terms of prescription methods, our focus is to answer another key question for banks, but ultimately for any company that utilizes direct marketing: is there an optimal medium through which we initiate contact with different user types? Through implementing optimal policy trees, we show a 50% improvement in average reward in predictions by optimally deciding whether to call a user or send them an email. This underlines in general business settings the power of understanding what channels of customer acquisition work best for different segments- an issue that issue modern tech businesses hinge on.


## Final Note

For a detailed overview of our methods and findings, please see the report found in the repo entitled Report.pdf or the slide deck entitled Presentation.pdf. Thanks!
