# ***Multivariate Techniques: Principal Component Analysis.***


## **Principal Component Analysis**

Principal component analysis (PCA) is a technique for reducing the dimensionality of large datasets, increasing interpretability but at the same time minimizing information loss. It does so by creating new uncorrelated variables that successively maximize variance.

It is a data reduction technique, which means it’s a way of capturing the variance in many variables in a smaller, easier-to-work-with set of variables. When dealing with a dataset with many variables, in order to interpret the data in a more meaningful form, it is necessary to reduce the number of variables to a few, interpretable linear combinations of the data. Each linear combination will correspond to a principal component.

**Principal components** are new variables constructed as a linear combination of the initial variables. The components are uncorrelated and most of the explained variance in the data is found in the first principal component. They represent the direction of the data that explain the maximal amount of variance in the data.

## **How to compute the principal components**

### Standardization.
Since PCA is very sensitive to the variance in the variables, you need to first standardize the range of initial continuous variables so that each contributes equally to the analysis.

### Covariance Matrix Computation.
If the variables in a dataset are highly correlated, it shows that there’s is redundant information in the dataset. We use the covariance matrix to check the correlation between the variables. The entries of the covariance matrix show how the variables are are varying from the mean with respect to each other. If the sign of the covariance is positive, in meant that the variables are correlated, if negative, they are inversely correlated.

### Compute Eigenvectors and Eigenvalues.
**Eigenvectors and eigenvalues** are the linear algebra concepts that we need to compute from the covariance matrix in order to determine the principal components of the data.  

Principal components are new variables that are constructed as linear combinations or mixtures of the initial variables. As there are as many principal components as there are variables in the data, principal components are constructed in such a manner that the first principal component accounts for the largest possible variance in the data set. PCA tries to put maximum possible information (variance)  in the first component, then maximum remaining information in the second, and so on. Geometrically speaking, principal components represent the directions of the data that explain a maximal amount of variance, i.e the lines that capture most information of the data.

Eigenvectors and eigenvalues always come in pairs, so every eigenvector has an eigenvalue, and their number is equal to the number of dimensions of the data. Eigenvectors of the covariance matrix are the directions of the axes where there is the most variance and eigenvalues are the coefficients attached to eigenvectors, which give the amount of variance carried in each Principal Component.

To compute the percentage of variance accounted for by each component, divide the eigenvalue of each component by the sum of eigenvalues. By ranking your eigenvectors in order of their eigenvalues, highest to lowest, you get the principal components in order of significance.


### **Feature vector.**

A feature vector is a matrix that has as columns the eigenvectors of the components that you decide to keep.
Recast the data along the principal component axis.
Use the feature vector formed to reorient the data from the original axes to the ones represented by the principal components. This is done by multiplying the transpose of the feature vector with the transpose of the original dataset.

## **When to use PCA:** 
  * when you want to reduce the number of features, 
  * when our dataset is too large to be handled, or 
  * when visualizing the data in lower dimensions.


