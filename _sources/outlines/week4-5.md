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

Rank-deficient problems and regularized least-squares (i.e., a family of shrinkage methods)

### Regularized least-squares models

TBD

#### Ridge regression

TBD

#### Lasso

TBD

### Generalized Least Squares

Weighted least squares

TBD

## Group discussion & demo topics

TBD

## Slides (Just for my convenience; will be removed after today's class due to copyright issues)

[Slides](https://docs.google.com/presentation/d/17eIMIMbfPACRaUueoTIXn2FfH2eFSqOPnURORtjEc3g/edit?usp=sharing)