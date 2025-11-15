# 核方法：維度是詛咒還是祝福？

## 課程大綱

環境資料科學的大挑戰：**維度詛咒** (Curse of Dimensionality)。當輸入維度變多時：
- 資料點變得更稀疏
- 最佳化的計算處理量呈指數增加

### 分類問題與貝式定理

分類問題 vs 聚類分析

### 神經網絡 vs 核方法

都是把資料先**映射到更高的維度**！


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






#### 徑向基函數（RBF）

- 神經網絡模型可使用它來把非線性問題轉換為線性問題。
- 使用核方法的模型：可使用「核技巧」的一種特徵映射法！

### 核方法的數學原理

- OLS 模型的**原始解**與**對偶解**
- 嶺迴歸模型的原始解與對偶解
- 原始解與對偶解，哪一個快？

#### 核

- 特徵映射 (Feature map)
- 核技巧 (Kernel trick)
- 什麼函數能當核？ -- 正定函數 (positive semi-definite function)
- 核的種類
- 核方法的優缺點

### 核嶺迴歸

- 流程
- 模組化設計

### 支持向量機（SVM）
SVM 的原始形式並沒有核組件！

#### 線性可分的情況
- 支持向量
- 在對偶拉格朗日解中的模式暗示我們可以使用核技巧！

#### 非線性 SVM
$\textbf{x}_n^T\textbf{x}_j$ -> $K(\textbf{x}_n, \textbf{x}_j) \equiv \phi^T(\textbf{x}_n)\phi(\textbf{x}_j) $

### 高斯過程迴歸
- 地理統計學
- 使用共變異數進行空間內插
- 使用核技巧來評估共變異數矩陣

額外參考資料: [Görtler, et al., "A Visual Exploration of Gaussian Processes", Distill, 2019.](https://distill.pub/2019/visual-exploration-gaussian-processes/)

## 小組討論 & 展示主題

1. Github Pages: [從 0 到 1 的 GitHub Pages 教學手冊](https://hackmd.io/@YmcMgo-NSKOqgTGAjl_5tg/HJpJk8ABU/%2F%40Albertnotes%2FB1_iKcAwI)