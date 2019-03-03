# Unsupervised Learning: Gaussian Mixture Model - Customer Segmentation

In this project I analyzed a wholesale customers dataset containing data on various customers' annual spending amounts (reported in monetary units) in diverse product categories for customer segmentation. One goal of this project is to best describe the variation in the types of customers the distributor interacts with and this provides the distributor with insights such as how to best structure delivery service to meet the needs of customers.

The dataset for this project can be found on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers). For the purposes of this project, the features 'Channel' and 'Region' are excluded in the analysis — with focus instead on the six product categories recorded for customers.

## Tools Required
The general requirements for this project are as follows:
- numpy
- pandas
- matplotlib
- seaborn
- sci-kit learn

## Contents

- **Data Visualization and Exploration**
- **Data Preprocessing** -In this section, the data is processed to create a better representation of customers. this involved
    - **Feature Scaling** - If the data provided is not normally distributed, especially if the mean and median vary significantly (indicating a large skew), it is most often appropriate to apply a non-linear scaling — particularly for financial data. One way to achieve this scaling is by using a Box-Cox test, which calculates the best power transformation of the data that reduces skewness. A simpler approach which can work in most cases would be applying the natural logarithm
    - **Outlier Detection** - The presence of outliers can often skew results. Here,the Tukey's Method for identfying outliers is used: An outlier step is calculated as 1.5 times the interquartile range (IQR). A data point with a feature that is beyond an outlier step outside of the IQR for that feature is considered abnormal. However, removing all outliers would result in losing a lot of information; as a result, only outliers that occur for more than one feature are removed.
    - **Feature Transformation using PCA** - In this section PCA is used to draw conclusions about the underlying structure of the wholesale customer data. Since using PCA on a dataset calculates the dimensions which best maximize variance, we will find which compound combinations of features best describe customers.
    - **Dimensionality Reduction using PCA & Visualization** - When using principal component analysis, one of the main goals is to reduce the dimensionality of the data — in effect, reducing the complexity of the problem. However, dimensionality reduction comes at a cost, fewer dimensionality can lower the variance reflected in the data; hence, the robstness of the model. Careful analysis should be performed during dimension reduction.
- **Clustering Model** - Gaussian Mixture Model
- **Conclusion and Implications: How to use this knowledge?**
