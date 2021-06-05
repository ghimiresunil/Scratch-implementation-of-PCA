# PCA from scratch

## Short Introuction 

I would like to say a few things about Vignesh Natarajan's answer first:

The curse of dimensionality is not about having a large number of dimensions, is about having an algorithm that struggles in a large number of dimensions or in more general terms a bad combination of algorithm/dimensionality for whatever reason. Some algorithms perform very very well in millions of dimensions, like Perceptron and Linear SVM.

What Vignesh describes to reduce dimensionality is known as PCA (Principal Component Analysis) a technique that is exactly the same as computing the SVD (Singular value decomposition) of your data matrix. The clarification I want to make is that with PCA you don't discover the principal dimensions of your data, you discover the principal components. And each component is a linear combination of your dimensions. So you can't use PCA or SVD to know if your "age" column plays a higher role than "price" but you can use it to effectively reduce the number of dimensions in your data when you need it. Using PCA or SVD just because is not a good practice.

Vignesh is absolutely right about the importance of Eigenvectors and Eigenvalues as a way to change the dimensionality of your data. They are the key to SVD and PCA.

Just to add something to the original answer about eigenvectors and eigenvalues in Machine Learning they are also used in Spectral Clustering.

## Task what I have done 

* What is "Dimensionality Reduction Problem"? Why is it necessary in Machine Learning?
* What is PCA? Discuss few applications in Machine Learning
* Write Short notes on the following topics:
  - Variance & Covariance
  - Eigenvalues & Eigenvectors
  - Eigen-value decomposition
  - Why is eigendecomposition is useful?
  - Singular-value decomposition
  - EVD vs SVD
  - Orthogonal Projection
  - PCA vs LDA
* Mathematical Implementation of PCA
* Some Basic Theory
  - Orthogonal Projections
  - Why normalization is necessary in PCA?

## Steps I have performed

*  Step 1: Load the data & required libraries
*  Step 2: Data Visualization
*  Step 3: Data Pre-Processing
*  Step 4: Computaion of Eigen Values & Eigen Vectors
*  Checking each features has unit variance before applying PCA
*  Step 5: Singular Value Decomposition (SVD)
*  Step 6: Picking Principal Components Using the Explained Variance
*  Step 7: Project Data onto Lower Dimensional Linear Subspace

## Can we classify after dimensionality reduction?

 In the modern scientific era, increasing quantities of data are being produced and collected. How, in machine learning, too much data can be a bad thing. At a certain level, additional features or dimensions will decrease the precision of a model, because more data has to be generalized. Thus, this is recognized as the "Curse of dimensionality". 
 
Dimensionality Reduction is a way to reduce a model's difficulty and prevent overfitting. Feature Selection and Feature Extraction are two main types of dimensionality reduction. We choose a subset of the original features by selecting a feature, while in feature extraction we draw knowledge from the component set to create a new feature subspace. Extraction of features is not only used to improve storage space or the learning algorithm's computational efficiency, but can also improve predictive performance by reducing the dimensionality curse — especially if we are working with non-regularized models. Also Linear Discriminant Analysis (LDA) and Principal Component Analysis (PCA) are the two key dimensional reduction algorithms. 

Classification of high-dimensional data, such as photographs, data on gene expression and spectral data, presents an important challenge to machine learning as predictive models based on these data run the risk of over-fitting or the existence of a large number of redundant or strongly associated attributes will significantly degrade classification accuracy. The goal is therefore to use PCA algorithms to the high dimensional data and to boost the predictive efficiency of several well-known machine learning algorithms. In other words, PCA is a classic computational approach for converting dataset attributes into a new collection of uncorrelated attributes called Principal Components, which increases the efficiency of machine learning when processing high-dimensional data. In simple terms, what we can say is that, PCA finds a new, lower dimensional orthonormal base such that the largest variance of the original data is kept. In addition, these low errors have been achieved through PCA, despite a significant reduction in data from the original attributes to at least the minimum attributes. In addition, more than 20 PCs are expected to find the optimum data set because the efficiency of the majority classifiers is decreasing with a growing number of PCs.  The PCA was particularly suited to the proposed approach, since it does not require the generation of all PCs with a data matrix, in contrast to the widely used proprietary decomposition methods and the first-derived pre-processing technique followed by standardization, it improves the performance of the majority of the classification tasks in machine learning.Question may arise: what if we used data mining techniques for large dataset without PCA?

This is because smaller datasets are much easier to visualize and explore and analyze data for machine learning algorithms without extraneous variables to process. The premises underlying the PCA are causal, so the definition is only accurate if the assumptions are correct. PCA computation on nonlinear data or broad dataset would then have little significance, only decomposing to the dominant linear nodes a global linear representation of the distribution of data is given. 

### Question may arise: what if we used data mining techniques for large dataset without PCA?

This is because smaller datasets are much easier to visualize and explore and analyze data for machine learning algorithms without extraneous variables to process. The premises underlying the PCA are causal, so the definition is only accurate if the assumptions are correct. PCA computation on nonlinear data or broad dataset would then have little significance, only decomposing to the dominant linear nodes a global linear representation of the distribution of data is given.
