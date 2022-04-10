# Project1 Real World Refinery Product Prediction
Analyze real-world refinery product data, Compare four Classifiers and choose one as our module to predict the quality of our product.
## Table of Contents

## Background
In this project, we are given 21983 copies of data of real-world refinery project data with 14 features. Our goal is to predict the quality of a product. More specifically, we want our model helps us find what inputs could make high-quality products. 

The names of features in the dataset are not shown due to privacy reasons. Nevertheless, we know that high-quality products have a corresponding y value of less than 2; otherwise, the product is low-quality.

## Findings
### Output distribution
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

