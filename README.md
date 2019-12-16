# Machine Learning: Consumer Spending Analysis

<i>Authors:</i>
Berwin Gan,
Brian Shin,
Maria Jaramillo,
Tofunmi Kupoluyi

Data Source: www.bls.gov

### About the Project
One-quarter of American workers make less than $10 per hour. That creates an income below the federal poverty level. Individuals on top of the income bracket are constantly generating more wealth, as those on the lower income brackets are struggling to meet their ends. With recent political candidates putting forth the concept of Universal Basic Income (UBI) as an essential tool to improve people’s quality of life, our team aims to map consumer expenditure to income levels in order to identify the avenues of expenditure a UBI could facilitate for lower income levels.


### Model - Description of Methodology
We decided to analyze the data with both supervised and unsu- pervised learning. Generally, our aim was to observe what income classes (if any) our data could be separated into i.e. if it was possible to get a good classifier for our data. Particularly in the case of supervised learning we were also curious to see if a linear svm could be fitted to the data so the corresponding weights of features could be analyzed.

<b>Supervised Learning</b>

For supervised learning, we experimented with both binary and multi-class SVM using linear, rbf and polynomial kernels.

<b>Unsupervised Learning</b> 

For unsupervised learning, we experimented with k-means clustering over 1 to 5 clusters.

### Model - Explanation of Algorithm

<b>Supervised Learning – Determining Number of Income Group Division</b>

We repeated the following process over various divisions of income groups to see which resulted in the most generalizable model. We performed a grid search over various kernels and regularization parameters to obtain the optimal svm configuration.
With the optimal svm configuration attained, we then checked the accuracy of the model on our test set.
A model with high training and test precision and accuracy, indicated that the data could be separated correctly into our predefined groups.

<b>Supervised Learning – Analyzing Weights of the Linear SVM</b>

We performed a grid search over regularization constants from 1-100 to determine the optimal binary linear svm that could be fitted to our data. Since we standardized our data, we analyzed the weights of the features. The highest positive weights indicated which features were most correlated to the higher income earners while the most negative weights indicated the features most correlated to
lower income earners.

<b>Unsupervised Learning – KMeans</b>

We first ran k-means clustering over 1..5 clusters and graphed the distortion to determine the best number of clusters to split the data
(Elbow Method for K-Means).
We also performed k-means clustering over k=1..5 clusters and
tried to see if the average income in each cluster was representative of income groupings.
