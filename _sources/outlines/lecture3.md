# 線性模型與正則化：什麼時候我們願意犧牲無偏性？

## 課程大綱

### 所有迴歸模型的共同組成要素

1. **架構**：輸入與輸出變數之間的連結關係
2. **損失函數**：需要被最佳化的目標。又稱為*成本函數*或*目標函數*
3. **求解器**：找到最佳解的演算法

### 簡單線性迴歸 (SLR)

**架構**：$y_i = \hat{y}_i + \epsilon_i = a_0 + a_1 x_i + \epsilon_i$

假設（問：這些假設是必要的嗎？）
- 只有 $\epsilon_i$ 是隨機變數，$\sim N(0, \sigma_i^2)$
- 所有 $\epsilon_i$ 都是獨立同分佈（*i.i.d.*）；當 $i \neq j$ 時，$\text{Cov}(\epsilon_i, \epsilon_j) = 0$。
- 對所有 $i$，$\sigma_i^2$ 都相同；$\sigma_i^2 = \sigma^2$

**損失函數**：普通最小平方 (OLS)；$ J = SSE = \sum_{i=1}^{N} \epsilon_i^2 $
- 使用此損失函數的優點是什麼？

**求解器**：解析法
- 正規方程式 (Normal equations)

#### SLR 的延伸內容

高斯-馬可夫定理與 **BLUE**（最佳線性無偏估計量）

平方和：迴歸模型可以解釋多少變異性？
- $SST = SSE + SSR$

$R^2$ 和 $r$ 之間的差異是什麼？

信賴區間 vs. 預測區間

當存在序列相關時...
- 杜賓-瓦森統計量

### 多元線性迴歸 (MLR)

線性迴歸模型中的「線性」是什麼意思？

#### 組成要素

**架構**：$\textbf{y} = \textbf{X}\textbf{a} + \boldsymbol{\epsilon}$（我們在課堂上使用這個表示法）

在環境科學研究中也常見其他等價表達式：$\textbf{d} = \textbf{G}\textbf{m}$（許多地球物理從業人員使用此表示法）

**損失函數**：OLS。$ J = SSE = \boldsymbol{\epsilon}^\text{T} \boldsymbol{\epsilon}$

**求解器**：解析法。
- 正規方程式是？
- 解：$\hat{\textbf{a}}=(\textbf{X}^\text{T}\textbf{X})^{-1}\textbf{X}^\text{T}\textbf{y}$

#### MLR 的延伸內容

循環與類別資料：需要接受轉換以利線性模型的使用

變異數分析 (ANOVA)
- 每個預測變數解釋的平方和
- F 檢定

#### 逐步迴歸

當你有大量潛在預測變數時...
- 應該納入越多越好嗎？
- 應該納入少越好嗎？
- 如果我們不得不保留所有預測變數時該怎麼辦？

逐步迴歸如何進行？

批評：這不是**採櫻桃謬誤** (Cherry picking) 嗎？

秩不足（或病態條件）問題與正則化最小平方法 -> 使用收縮方法的模型家族

### 正則化最小平方法模型

正則化就是透過加上額外的限制項來重新設計損失函數。

有那些好處呢？
- 在迴歸模型中保留所有預測變數。
- 讓迴歸模型的輸入滿秩或具有更佳的條件數，以改善解的不穩定度。

例子：小組練習題的 One-hot encoding 那一題

#### 嶺迴歸

又名脊迴歸、L-2 正則化，或是吉洪諾夫迴歸

**架構**：與 MLR 相同

**損失函數**：正則化 OLS。$ J = \boldsymbol{\epsilon}^\text{T} \boldsymbol{\epsilon} + \lambda\textbf{a}^\text{T}\textbf{a}$
- 這是使用拉格朗日乘數 $\lambda$ 的顯式表達式。
- 等價於約束條件 $\textbf{a}^\text{T}\textbf{a} \leq b$ 下的標準 OLS（$\boldsymbol{\epsilon}^\text{T} \boldsymbol{\epsilon}$）。詳細資訊請參見 Hsieh 的書中附錄 B。

**求解器**：解析法
- 解：$\hat{\textbf{a}}=(\textbf{X}^\text{T}\textbf{X}+\lambda \textbf{I})^{-1}\textbf{X}^\text{T}\textbf{y}$

如何選擇**超參數** $\lambda$？
- **驗證**（這是我們在本課程中第一次看到「驗證資料」這個術語！）
- **交叉驗證**（我們在神經網路的主題中會繼續討論）

#### Lasso

又名套索迴歸、拉索迴歸、L-1 正則化。Lasso 這個詞是「最小絕對收縮與選擇運算子」的首字略縮。

**架構**：與 MLR 相同

**損失函數**：正則化 OLS。$ J = \boldsymbol{\epsilon}^\text{T} \boldsymbol{\epsilon} + \lambda \sum_{j=1}^{m}|a_j|$
- 它的隱式表達式是什麼？

**求解器**：因為損失函數不可微，通常用數值方法求解。我們會在下一個主題中討論可能的方法。

LASSO 可以當作預測變數的選擇器。為什麼？
- 尋找嶺迴歸和 LASSO 的約束區域
- 這些區域的形狀是什麼？
- Lasso 可以找到「稀疏性」更高的解。

### 廣義最小平方法

又稱為加權最小平方法 (WLS)。探索更多重新設計損失函數的方法！

**架構**：與 MLR 相同

**損失函數**：WLS；$ J = \boldsymbol{\epsilon}^\text{T} \textbf{C}^{-1}\boldsymbol{\epsilon}$ 其中 $\textbf{C}$ 是殘差的共變異數矩陣。

**求解器**：解析法。

如果使用了這個模型，就意味著我們對於資料存在什麼假設？為什麼要使用馬哈拉諾比斯距離？

## 最後的問題

**什麼時候我們願意犧牲無偏性？**
- $\textbf{X}^\text{T}\textbf{X}$ 不可逆（即 $\textbf{X}$ 是秩不足矩陣）
- $\textbf{X}^\text{T}\textbf{X}$ 可逆，但 $\textbf{X}$ 的列之間高度相關（即 $\textbf{X}$ 是病態條件矩陣）
- 還有其他原因嗎？(1)
- 還有其他原因嗎？(2)

## 小組討論與示範

1. Jupyter Notebook / JupyterLab 簡介
2. 使用 Jupyter Notebook 載入練習資料集（由 [Google Colaboratory](https://colab.google/)、[Callysto Hub](https://www.callysto.ca/) 或你的本機提供計算資源）