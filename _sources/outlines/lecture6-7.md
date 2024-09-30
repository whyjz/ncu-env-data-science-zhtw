# Neural Networks: How can you trust deep models that seem like black boxes?

**2024.03.26, 2024.04.02, 2024.04.09**

## Lecture outline

Neural Network (NN): it's biological origin and how it relates to data science

### Perceptrons

The basic structure of a neural network!

**Activation function**:
- Heaviside step function
- logistic function (or $tanh$)
- Rectified linear unit (ReLU)
- Softplus

Limitation on non-linear separation

### Multi-layer Perceptrons (MLP)

The simplest NN that has practical use!

Hidden layer: transform the linear perceptron model into a non-linear model.

Predictors, parameters, and loss function of MLP
- number of observations vs parameters

Challenges of a non-linear optimization
- curse of dimensionality? 
- potential solution: Ensembles

What's the advantage?

MLP: a Universal approximator!

### Extreme learning Machine (ELM)

The idea of using ensembles -> transform a non-linear problem back to a linear problem

What's the advantage?

How to determine the number of hidden layer nodes $L$?

Skip connection

### Radial Basis Functions (RBF)

This is another way to reduce the non-linearity of NN into a linear problem.

Why is it called "Radial Basis?" We'll revisit this during the kernel method section.

### Back-Propagation

The life save of the MLP problem!

Learning rate $\eta$

From the textbook: "Nowadays, the term ‘back-propagation’ is used somewhat ambiguously."
- It could mean the original back-propagation algorithm (with inefficient gradient descent)
- or, more likely, it could mean using only the first part involving the backward error propagation to compute the gradient of J

### Tuning and validation

Grid search, random search, validation, cross-validation, and double cross-validation

### Other Emsemble methods

Help reduce the variance error (Section 8.3)

- Bagging
- Stacking
