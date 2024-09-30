# Regression Models: Why is regularization so important?

**2024.03.12, 2024.03.19**

## Lecture outline

### Basics

Review of the simple linear regression:
- Model description and associated assumption
- Advantage of the "least square"
- Normal equations

The sum of squares: how much variability can be explained/modeled by a regression model?
- $SST = SSE + SSR$

Confidence interval vs. Prediction interval

When there is a serial correlation...
- Durbin--Watson statistic

### Multiple linear regression (MLR)

What does "linear" mean in a linear regression model?

Two equivalent expressions that are commonly seen in the environmental science studies: 
- $\textbf{y} = \textbf{X}\textbf{a} + \boldsymbol{\epsilon}$    (We'll use this at the class)
- $\textbf{d} = \textbf{G}\textbf{m}$    (Many geophysicists use this)

Least-squares solution:
- $\hat{\textbf{a}}=(\textbf{X}^\text{T}\textbf{X})^{-1}\textbf{X}^\text{T}\textbf{y}$

Gauss--Markov Theorem and BLUE

### Advanced topics for MLR

Circular and categorical Data: transform them so that we can use a linear model

Analysis of Variance (ANOVA)
- Sum of squares explained by each predictor
- F-test

#### Stepwise regression

When you have lots of potential predictors...
- The more, the better?
- The less, the better?
- When you have no choice but to keep all the predictors?

How do we do stepwise regression?

Criticism: Isn't this **cherry-picking**?

Rank-deficient (or ill-conditioned) problems and regularized least-squares (i.e., a family of shrinkage methods)

### Regularized least-squares models

Regularization tries to redesign the loss function by imposing an additional constraint.

What are its benefits?
- To keep all the predictors in the regression model
- To improve the solution by making the input towards full rank or better conditions.

#### Ridge regression

a.k.a. L-2 regularization or Tikhonov regression 

Two expressions of the ridge regression: Implicit (Lagrangian, check out Appendix B of the textbook) and Explicit

ridge regression solution:
- $\hat{\textbf{a}}=(\textbf{X}^\text{T}\textbf{X}+\lambda \textbf{I})^{-1}\textbf{X}^\text{T}\textbf{y}$

How to select $\lambda$?

#### Lasso

a.k.a. L-1 regularization

Lasso is typically solved numerically since its loss function is not differentiable.

The most distinct difference between Lasso and Ridge: predictor selection

### Generalized Least Squares

Exploring more ways to redesign the loss function!

Data covariance matrix and weighted least squares

## Group discussion & demo topics

1. Overview of the term project output: an example https://ucb-stat-159-s23.github.io/project-Group28/README.html 
2. Another example is this class webpage.