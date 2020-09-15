# Feature Engineering for Credit Card Fraud Detection

**Background**

A credit card fraud detection algorithm consists in identifying those transactions with a high probability of being fraud, based on historical fraud patterns. The use of machine learning in fraud detection has been an interesting topic in recent years. Most of these studies compare their proposed algorithms with a benchmark algorithm and then make the comparison using a standard binary classification measure, such as misclassification error, receiver operating characteristic (ROC), Kolmogorov–Smirnov (KS), F1 Score (Bolton et al., 2002; Hand et al., 2007) or AUC statistics (Dal Pozzolo et al., 2014). Most of these measures are extracted by using a confusion matrix as shown below:
<img src="data visualization/confusion-matrix.png" alt="image" width="300"/>

where the prediction of the algorithm ci is a function of the k features of transaction i. However, the cost of false negative is 100 times higher than false positive. Besides, assuming constant cost for false negatives is unrealistic. In this case, example-dependent cost matrix is introduced. 

In summary, a single transaction information is not sufficient to detect a fraudulent transaction, the important information we want to capture is the consumer spending behavior, which is usually used by commercial fraud detection systems. This project aims to construct 20 features to capture customers' spending behaviour by transaction aggregation strategy. The aggregation features consists in grouping the transactions made during the last given number of hours, first by card or account number, then by transaction type, merchant group, country or other, followed by calculating the number of transactions or the total amount spent on those transactions. 

**Note**
In practice, when time passes, information lose their value, in the sense that a customer spending patterns are not expected to remain constant over the years. Whitrow et al. definea fixed time frame to be 24, 60 or 168 h. 

**data source**
https://data.ok.gov/dataset/purchase-card-pcard-fiscal-year-2014*

**Steps**
- EDA
- Create 20 features
- Data visualization by plotly


<img src="data visualization/fraud-alerts-lg.png" alt="image" width="700"/>
