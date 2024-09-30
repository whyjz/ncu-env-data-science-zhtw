# Kernel Methods: Is dimensionality a curse or a blessing?

**2024.04.23, 2024.04.30**

## Lecture outline

### Quick overview of the classification problem and the Bayes theory 

Classification vs cluster analysis

### NN vs Kernel Methods

Higher dimension!

### Timing a regression problem

- Primal and Dual Solutions: which one is faster?
- Primal and Dual Solutions for ridge regression

### Kernels

- Feature map
- kernel trick
- Mercer theorem vs positive semi-definite kernel function
- Differernt kernels
- advantages and disadvantages

### Kernel ridge regression

- Procedure
- Modularized design

### Support Vector Machine (SVM)

The original form of SVM does not have a kernel component!

#### Linearly separable case
- Support vectors
- The pattern in the dual Lagrangian solution implied that we can slip in the kernel trick!

#### Non-linear SVM

$\textbf{x}_n^T\textbf{x}_j$ -> $K(\textbf{x}_n, \textbf{x}_j) \equiv \phi^T(\textbf{x}_n)\phi(\textbf{x}_j) $

### Gaussian process regression

- Geostatistics
- Covariance-based interpolation where kernels are used for evaluating the (believed) covariance matrix

Resources: [Görtler, et al., "A Visual Exploration of Gaussian Processes", Distill, 2019.](https://distill.pub/2019/visual-exploration-gaussian-processes/)