# Shopping Customers Segmentation & Clustering Analysis

## Problem Statment 
  Malls or shopping complexes are often indulged in the race to increase their customers and hence making huge profits. To achieve this task machine learning is being applied by many stores already.
  The main aim of this problem is to apply  the customer segmentation concepts, also known as market basket analysis, trying to understand customers and separate them in different groups according to their     
  preferences, and once the division is done, this information can be given to marketing team so they can plan the strategy accordingly.

## Context

* Client want to identify the most important shopping groups based on income, age and the mall shopping score.
* He wants the ideal number of groups with a label for each.

## The Approach

1. Perform some quick EDA
2. Use K-Means Clustering Algorithm to create segments.
3. Use Summery statistics on the cluster
4. Visualization

## Dataset
* [Mall dataset]('https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python/')
* ![data-preview]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/mallData.png')

Here we have the following features :
1. CustomerID: It is the unique ID given to a customer
2. Gender: Gender of the customer
3. Age: The age of the customer
4. Annual Income(k$): It is the annual income of the customer
5. Spending Score: It is the score(out of 100) given to a customer by the mall authorities, based on the money spent and the behavior of the customer.

## Tools
* numpy|pandas: Will help us treat and explore the data, and execute vector and matrix operations.
* matplotlib|seaborn: Will help us plot the information so we can visualize it in different ways and have a better understanding of it.
* sklearn: Will provide all necessary tools to train our models and test them afterwards.

## EDA

```
   df.info()
```

```
   df.isna().sum()
```

```
   df.duplicated().sum()
```

## Annual Income Distribution
![Annual Income Graph]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/AnnualIncome.png')
Most of the annual income falls between 50K to 85K.

## Age Distribution
![Age Distribution]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/Age.png')
There are customers of a wide variety of ages.

## Shopping Score Distribution
![Spending Score Graph]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/SpendingScore.png')
The maximum spending score is in the range of 40 to 60.

## Gender Analysis
![data-preview]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/GenderCount.png')
More female customers than male.


# Clustring

I will use the K-Means Clustering algorithm to cluster the data.To implement K-Means clustering, we need to look at the Elbow Method.
The Elbow method is a method of interpretation and validation of consistency within-cluster analysis designed to help to find the appropriate number of clusters in a dataset.

![Before Clustering]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/PreCluster.png')

## Income Cluster
![data-preview]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/IncomeCluster.png')




## Spending & Income Cluster
![data-preview]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/SpendingCluster.png')
* We are using the inertia as cost function in order to identify the sum of squared distances of samples to the nearest cluster centre.
* The elbow can be found, approximately, where the number of clusters is equal to 5. Therefore we are selecting 5 as the number of clusters to divide our data in.
![data-preview]('https://github.com/ImAnitaYadav07/Customer-Segmentation-Analysis/blob/4869f71e0ac6a14364eab4cccff38fcdb4fc6e41/postCluster.png')


# Analysis Summery
 * people in their thirties, forties and fifthies tend to earn more money annually than the ones younger than thirty or older than fifty years old. That is to say people whose age lays between thirty and fifty years old seem to get better jobs since they might be better prepared or be already more experienced than younglings or older people. In the graphic we can also see how males tend to earn a little bit more money than females, at least until fifty years old.
 ### **Target Cluster**

  1. Target group would be cluster1. Which has a high Spending Score and high income.
  2.  60 persent of cluster1 shoppers are women. We should look for ways to attract these customers using a marketing campaign targeting popular items in this cluster.
  3.  Cluster2 presents an interesting opportunity to market to the customers for sales event on popular items.
 * Young people tend to spend way more than older people
 * Observing the clustering graph, it can be clearly observed that the ones who spend more money in malls are young people. That is to say they are the main target when it comes to marketing, so doing deeper studies about what they are interested in may lead to higher profits.
 * Promoting discounts on some shops can be something of interest to those who don't actually spend a lot and they may end up spending more!



