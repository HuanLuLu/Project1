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
