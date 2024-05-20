# Random Forests: When one model is not enough, make several?

**2024.05.14, 2024.05.21**

## Lecture outline

### Classification and Regression Trees (CART)

Split and fit using constant functions.

- Prune and regularization
- Choosing loss function for classification: Entropy or Gini index

### Randon Forest

- Bootstrap + CART + Ensemble
- Out-of-bag data for model validation ($p$ and $n_{min}$
- Extremely randomized trees: No bootstrap, and instead randomly selecting split points

### Boosting

No bootstrap as well; instead, updating the previous model with a focus on the part the previous model does not do well.

#### Gradient boosting

- Updating the previous model using gradient descent 
- XGBoost (regularized gradient boosting): adding more regularizations

## Group discussion & demo topics

I have made a [template](https://github.com/whyjz/ncu-env-data-science-template) for you to automatically publish your Jupyer notebook (or plain markdown files) using GitHub Pages. You can also find the deployed [HTML here](https://whyjz.github.io/ncu-env-data-science-template/project.html). 

## Slides (Just for my convenience; will be removed after today's class due to copyright issues)

[Slides](https://docs.google.com/presentation/d/17eIMIMbfPACRaUueoTIXn2FfH2eFSqOPnURORtjEc3g/edit?usp=sharing)