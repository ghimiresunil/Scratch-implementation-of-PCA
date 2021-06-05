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
-- Variance & Covariance
