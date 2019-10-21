# Customer Segmentation Analysis

## Executive Summary
The purpose of this project is to develop a working understanding of clustering and unsupervised learning. I do this with the UCI Machine Learning Dataset (Online Retail II) with a K-Means algorithm. I attempt to cluster the customers in order to develop a rough segmentation to provide value for whichever (hypothetical or not) online retailer provided this data.

## Outline
1. Data Set Description
2. Methodology
3. Results and Conclustion

## 1. Data Set Description
The dataset was rather easy to obtain you can find it [here](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II).
I picked this dataset for my analysis because it provides the core requirements for a business to be able to cluster their customers, their purchases. The data comes in one flat file with each observation containing variables like a CustomerID, ProductID, Time of Purchase, Quantity, Price, InvoiceNo and Country.

## 2. Methodology

### i. Data Wrangling and Cleaning
There was a good bit of cleaning needed before the analysis which I cover in the [EDA Notebook](https://github.com/AbinavKumar/CustomerAnalysis/blob/master/EDA.ipynb). The primary difference between the original table and the wrangled table is that the index is no longer the invoice This section uses pandas.

### ii. Explotory Data Analysis
This can conveniently be found in the [EDA Notebook](https://github.com/AbinavKumar/CustomerAnalysis/blob/master/EDA.ipynb). I primarily just look at the composition of orders by country. This section uses pandas and matplotlib.

### iii. Data Preprocessing
There are two sections of preprocessing. The first in the [EDA Notebook](https://github.com/AbinavKumar/CustomerAnalysis/blob/master/EDA.ipynb) the second in the [Data Analysis Notebook] (https://github.com/AbinavKumar/CustomerAnalysis/blob/master/Data%20Analysis.ipynb). This section uses pandas and sklearn's MinMaxScaler to scale the data.

### iv. Feature Selection
I experimented with keeping all the purchase data in the dataset, and even using PCA on the purchase data to reduce the dimensions. I found that, with so many dimensions, the clustering becomes meaningless and there is no clear number of clusters to select. I ended up only keeping the customer KPIs in the model. 

### v. Model Tuning/Selection
I use both an elbow plot and silhouette scores to determine the optimal number of clusters. This section uses sklearn and matplotlib.

### 3. Results and Conclusion
There is no clear metric that I can minimize or maximize to determine if what I have done is best. This is the nature of supervised learning. I did find that the customers are reasonably clustered into 3 clusters of "lower-spenders", 2 cluster of "mid-spenders" and 1 cluster of "big-spenders". With some additional data, marketing surveys, focus groups, psychological profiling these clusters would allow for some additional tweaking of the clusters and provide more insight into what the significance of clusters are. Understanding segmentation would have likely have significant results on customer retention, profits, and marketing efficacy.

After this analysis a few more questions came to my mind:
- Is it possible to psychologically profile customers and supplement that data with purchase data?
- What is the profitability of the customers in the cluster?
- Can you analyze the movement of customers between clusters?
- Can customers be "nudged" into other clusters?
- Can we develop a prediction function to acquire new customers we determine to fit into a certian cluster?
- What is

In the context of an actual business these questions would serve as a good starting point to collect additional data to better segment and target customers. 
