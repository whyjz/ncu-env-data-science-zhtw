# 主成分分析：什麼時候要用無監督學習？

## 課程大綱

主成分分析 (Principal Component Analysis; PCA)，又叫做經驗正交函數 (Empirical Orthogonal Function; EOF) 分析

### 無監督學習與 PCA

當變數一多，在進行迴歸模型之前就有許多工作要做：

- 定義預測變數（這隱含著誤差模型）
- 考慮到過擬合或維度詛咒的情況，選擇適當的迴歸模型
- 指定資料點和維度（見下節）

不管是線性模型還是非線性模型，這都是無法避免的，會花很多時間。

有沒有純粹用於探索目的算法，在不預設前提之下，能以簡單的方法搜索變數之間的關聯？如果能讓之後的迴歸模型變簡單，那就更好了。

#### 資料點與維度

有些環境科學的資料，可以用不同的方式去定義「資料點」和「維度」。

例子：某區域所有 AQI 測站的時序資料。有多種定義方式？

#### PCA 的簡單理解

指定資料點和維度（座標軸）後，嘗試旋轉座標軸，使得資料點盡可能沿著座標軸的軸線散佈。

### 數學表述

在旋轉之後，在新的某一座標軸投影的座標值，變異數需要最大化。

$\arg \min_{\textbf{e}_1} \text{var}(z_1) = \arg \min_{\textbf{e}_1} \textbf{e}^\textbf{T}_1\textbf{C}\textbf{e}_1$ subject to $\textbf{e}^\textbf{T}_1\textbf{e}_1 - 1 = 0$

$\textbf{C}\textbf{e}_1 - \lambda \textbf{e}_1 = 0$

$a_j(t) = \textbf{e}^\textbf{T}_j (\textbf{x} - \bar{\textbf{x}})$

#### 特徵值與特徵向量

### 主成分、特徵向量與模式


### 奇異值降解

Singular Value Decomposition

### 旋轉 PCA

#### Varimax

A-frame
E-frame

<!-- Neural Network (NN): its biological origin and how it relates to data science

### Perceptrons



This is the most basic structure of a neural network!

**Architecture**: For a model with only a single output variable $y$: $\hat{y} = f\Big(\sum_i w_i x_i + b\Big)$
- **Activation function** $f$:
  - Heaviside step function
  - logistic function (or $tanh$)
  - Rectified linear unit (ReLU)
  - Softplus

Limitation on non-linear separation: only works for the *linearly separable* cases.

### Multi-layer Perceptrons (MLP)

The simplest NN that has a practical use!

**Architecture**: For a model with only a single output variable $y$: $h_j = f\Big(\sum_i^{m_1} w_{ji} x_i + b_j\Big),\quad \hat{y} = g\Big(\sum_j^{m_2} \tilde{w}_{kj} h_j + \tilde{b}_k\Big)$
- **Hidden layer**: transform the linear perceptron model into a non-linear model.
  - number of model parameters. In NN, model parameters are also called **weights.**
  - **Hyperparameters** parameters related to the architecture. Examples: number of hidden nodes.

**Loss function**: The most common selection is the mean squared error (MSE). 

**Solver**: Must be solved numerically. (see below)

If the number of nodes is sufficiently large, we can achieve universal approximation even with only one hidden layer!

### Optimizing a non-quadratic loss function

Now the loss function $J(\textbf{w})$ can have many local minima in the parameter space. An analytical solution is no longer possible.

#### Newton's method

This method involves the calculation of the Hessian matrix $\textbf{H}_0$, which contains all the second order derivatives of $J$ assessed at $\textbf{w}_0$. One iteration can be expressed as

$\textbf{w}_{k+1} = \textbf{w}_k - \textbf{H}_k^{-1} \nabla J(\textbf{w}_k)$

#### Gradient descent method 

This method replaces the Hessian matrix $\textbf{H}_0$ with a fixed or a flexible step size $\eta$, which is typically called a **learning rate**:

$\textbf{w}_{k+1} = \textbf{w}_k - \eta \nabla J(\textbf{w}_k)$

### Optimizing an MLP NN

The structure of an MLP NN makes the calculation of $\nabla J(\textbf{w})$ difficult, but the good thing is that we have the *back-propagation* algorithm, which just needs one data point to derive $\nabla J(\textbf{w})$ based on model errors ($\hat{y} - y$). The term "back-propagation" means it starts by finding the gradient for the weights in the output layer, then uses those numbers to find the gradient for the weights in the previous hidden layer (i.e., propagation), and so on.

#### Back-Propagation

From the textbook: "Nowadays, the term ‘back-propagation’ is used somewhat ambiguously."
- It could mean the original back-propagation algorithm (with inefficient gradient descent)
- or, more likely, it could mean using only the first part involving the backward error propagation to compute the $\nabla J(\textbf{w})$.

As it is based on the gradient descent method, the back-propagation needs a pre-defined **learning rate** to initialize.

For the weights connecting the hidden and output layers:

$\Delta \tilde{w}_{kj}=-\eta\frac{\partial J}{\partial \tilde{w}_{kj}} = \eta(y_k-\hat{y}_k)g'(\tilde{s}_k)h_j$

For the weights connecting the input and hidden layers:

$\Delta w_{ji}=-\eta\frac{\partial J}{\partial w_{ji}} = \eta \sum_k (y_k-\hat{y}_k)g'(\tilde{s}_k) \tilde{w}_{kj}f'(s_j)x_i$

#### Using Back-Propagation

Since you only need **one data point** to calculate $\nabla J(\textbf{w})$, there are different styles to apply the back-propagation algorithm:

- Sequential training: Updating weights using one data point
- Batch training: Updating weights using all data points (using average $\nabla J(\textbf{w})$)

**Epoch**: The time when all data points are visited (used) once.

And this procedure can be performed as many times as you want until arbitrary stopping criteria. For example:

- When the model error (e.g., RMSE) starts to stabilize or even increase
- When the prediction error of the validation data set starts to stabilize or even increase (**early stopping**)


### General issues for non-linear fitting

<!-- - Curse of dimensionality? -->

<!-- Do you have ideas for addressing these challenges?

- The optimization process falls into a local minimum depending on the initial weight selections.
- Lots of weights result in potential overfitting.
- Lots of hyperparameters to tune. (What are they?)
- When an MLP with a single hidden layer grows, it adds lots of nodes, and the processing time increases like crazy due to the curse of dimensionality. -->

<!-- How to address these challenges? Ensembles? Regularizations? -->

<!-- Regularizations? Dropout? ...

### Extreme Learning Machine (ELM)

This is one proposed solution to the challenges above. The idea of using ensembles transforms a non-linear problem back to a linear problem.

**Architecture**: Same as MLP; however, two rules are used to transform it into a linear problem.
1. The weights applied to the input layer are randomly assigned for each ensemble member.
2. The activation function of the hidden layer is an identical function.

**Loss function**: Same as MLP.

**Solver**: the problem is analytically solved for each ensemble member. -->



<!-- How to determine the number of hidden layer nodes $L$? -->

<!-- ### Radial Basis Functions (RBF)

This is another way to reduce the non-linearity of NN into a linear problem.

Why is it called "Radial Basis?" We'll revisit this during the kernel method section. -->

<!-- ### Tuning hyperparameters (Model validation)

Multiple ways to assign validation data:
- Find an independent validation data set. Or reserve some data from training for later use for validation.
- Cross-validation: using all training data to validate the model by segmenting the data and repeated validations.
- Double cross-validation: an advanced cross-validation scheme to avoid issues caused by serial correlation of the input data.

Multiple ways to search within the hyperparameter space:
- Grid search
- Random search

### Ensemble technique

The ensemble technique helps reduce the variance error without sacrificing bias error (Section 8.3).

- Bagging: bootstrapping; creating different (sub-)input data sets
- Stacking: combining totally different non-linear models.  -->