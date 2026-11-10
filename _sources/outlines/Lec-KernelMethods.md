# 核方法：維度是詛咒還是祝福？

## 課程大綱

### 維度詛咒

環境資料科學的大挑戰：**維度詛咒** (Curse of Dimensionality)。當輸入維度變多時：
- 資料點變得更稀疏
- 最佳化的計算處理量呈指數增加

我們在 PCA 一節中看到了把高維度資料降維的方法，以應對維度詛咒。然而，高維度的資料真的這麼不好嗎？

如果我們執意逆向而行，會得到什麼？其實我們也早就看過了：雖然出發點不同，不過神經網路就是把低維度資料升維後再進行處理。那麼有沒有辦法以「升維」為中心思想，做出能夠用於資料分析的模型？

核方法（Kernel methods）就是基於此中心思想而設計的模型。這類模型需要找個數學方法，把增加維度後一併提昇的運算複雜度變簡單才行。

### 迴歸問題的計時賽：原始解與對偶解

- 原始解與對偶解 (Primal and Dual Solutions)：哪個比較快？
- 嶺迴歸的原始解與對偶解
- 對偶解、升維運算、內積之間的關係

對 MLS 來說，架構 $\textbf{y} = \textbf{X}\textbf{w} $ 的解為 $\textbf{w} =(\textbf{X}^\text{T}\textbf{X})^{-1}\textbf{X}^\text{T}\textbf{y}$（**原始解**）。如果設

$\textbf{w} = \textbf{X}^\textbf{T}\textbf{\alpha}$

那麼 $\textbf{y} = \textbf{X}\textbf{X}^\textbf{T}\textbf{\alpha}$，$\textbf{\alpha} = (\textbf{X}\textbf{X}^\textbf{T})^{-1}\textbf{y}$。

對於領迴歸來說，解為 $\textbf{\alpha} = (\textbf{X}\textbf{X}^\textbf{T} + \lambda\textbf{I})^{-1}\textbf{y}$（**對偶解**）。

格拉姆矩陣（Gram matrix）：$\textbf{G} \equiv \textbf{X}\textbf{X^T}$

### 核

- **特徵映射** (Feature map)
- 核技巧 (Kernel trick)
- Mercer 定理與正定函數 (positive semi-definite function)
- 核的種類
- 核方法的優缺點

### 核嶺迴歸

- 流程
- 模組化設計

### 分類問題與貝式定理

分類問題 vs 聚類分析

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

## 最後的問題

**維度是詛咒還是祝福？**
- 是詛咒？維度一多，處理時間呈指數增長
- 是祝福？核方法可以把低維空間的非線性模型轉換成高維空間內的線性模型
- 仍然是詛咒？核方法天生沒有辦法處理很多資料點
- 還有其他觀點嗎？

## 小組討論與示範

1. Github Pages: [從 0 到 1 的 GitHub Pages 教學手冊](https://hackmd.io/@YmcMgo-NSKOqgTGAjl_5tg/HJpJk8ABU/%2F%40Albertnotes%2FB1_iKcAwI)

<!-- #### 徑向基函數（RBF）

- 神經網絡模型可使用它來把非線性問題轉換為線性問題。
- 使用核方法的模型：可使用「核技巧」的一種特徵映射法！ -->