# Project1 Real World Refinery Product Prediction
Analyze real-world refinery product data, Compare four Classifiers and choose one as our module to predict the quality of our product.
## Table of Contents
* [Background](#background)

* [Findings](#findings)

  * [Output distribution](#output-distribution)

  * [Data Visulization](#data-visulization)

  * [Feature Correlation](#feature-correlation)

  * [Imbalanced Data Handling](#imbalanced-data-handling)

  * [Test Results Comparison](#test-results-comparison)

* [Conclusion](#conclusion)

## Background
In this project, we are given 21983 copies of data of real-world refinery project data with 14 features. Our goal is to predict the quality of a product. More specifically, we want our model helps us find what inputs could make high-quality products. So we will consdier presicion as our main metrics.

The names of features in the dataset are not shown due to privacy reasons. Nevertheless, we know that high-quality products have a corresponding y value of less than 2; otherwise, the product is low-quality.

## Findings
### Output Distribution
As seen below, the output y value distribution is right-skewed with moderately imbalanced. We will compare the prediction result without and with handling the imbalance.

![](images/Output%20Distribution.png)

### Data Visulization
Here, we use the t-SNE algorithm to visualize the data. As shown in the 2D graph, high-quality product data tend to be clustered at the bottom of the graph.

![](images/2D%20visualization.png)

The cluster is more visible in 3D coordinates.

![](images/3D%20visualization.png)

### Feature Correlation

The dataset with highly correlated features will cause a " Multicollinearity " issue. Although correlation cannot be explained as causation, we still need to check the data and gain insights. We can observe that features x1 and x5 are almost perfectly positively correlated based on the correlation matrix. Features x7 and x8 are highly positively correlated too.

![](images/Feature%20Correlation.png)

### Imbalanced Data Handling

Resampling, including oversampling and undersampling, is the common solution. However, we want our model to learn as many features of high-quality products as possible in our case. Therefore, instead of undersampling data in the majority class, we will apply SMOTE, Synthetic Minority Over-Sampling Technique, to synthesize new examples from the minority class, the low-quality products. The result is shown as follows. 

![](images/Cluster%20comparison.png)

### Test Results Comparison
First, we applied four different machine learning algorithms on the unbalanced data(Original data) and balanced data(after applying SMOTE) separately, and compared the precision. The Decision Tree has the best precision(95.8%), meanwhile the Logistic Regression is only slightly lower(95.2%).

Then we compared other metrics, like accurace, recall and f1 score, between Logistic Regression and Decision Tree. Logistic Regression has better performance overall. So we will choose the Logistic Regression model.

![](images/Prediction%20comparison.png)

## Conclusion

After comparing four different types of classifiers in this project, we found the Logistic Regression algorithm has the best performance. Meanwhile, by adding new minority class data points in our training data, our classifiers are pushed to focus more on class 1 data and increase the precision in our results.
