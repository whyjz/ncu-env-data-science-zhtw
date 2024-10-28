# 神經網路：越深的學習，成效越好嗎？

**2024.10.29, 2024.11.05**

## 大綱

神經網路 (NN)：源自生物學的發想，以及與資料科學的關聯

### 感知器 (Perceptrons)

神經網路的最基本結構！

**激勵函數**：
- Heaviside 階梯函數（單位階躍函數）
- 邏輯斯諦函數（或 $tanh$）
- 線性整流函式（ReLU）
- Softplus

感知器好用嗎？在非線性分類問題上遇到的阻礙

### 多層感知器 (Multi-layer Perceptrons; MLP)

最簡單且實用的神經網路。

**隱藏層**：將線性感知器轉變為非線性模型的關鍵！

MLP 的預測變數、參數與損失函數
- 觀測資料量 vs 參數數量

非線性最佳化的挑戰
- 維度詛咒？
- 潛在解方：集成方法 (ensemble approach)

說到底，MLP 有何優勢？
- 萬用逼近器 (Universal approximator)！？這算是優勢嗎...

### 極限學習機 (Extreme learning Machine; ELM)

開發集成方法的使用潛力，將非線性問題化為線性問題

ELM 有何優勢？
- 線性求解？

如何確定隱藏層的節點數 $L$？

跳躍連接

<!-- ### Radial Basis Functions (RBF)

This is another way to reduce the non-linearity of NN into a linear problem.

Why is it called "Radial Basis?" We'll revisit this during the kernel method section. -->

### 反向傳播 (Back-Propagation)

神經網路模型問題的救星！沒有它，根本沒辦法求解。

黑塞矩陣 (Hessian matrix, $\textbf{H}$) 與學習率 $\eta$

教科書摘錄：「Nowadays, the term ‘back-propagation’ is used somewhat ambiguously.」
- It could mean the original back-propagation algorithm (with inefficient gradient descent)
- or, more likely, it could mean using only the first part involving the backward error propagation to compute the gradient of J

### 超參數的調教與驗證

- 網格搜尋
- 隨機搜尋
- 驗證
- 交叉驗證
- 雙重交叉驗證

### 其他使用了集成方法的訓練技巧

幫助減少 Variance error（第 8.3 節）

- 裝袋法 (Bagging)
- 堆疊法 (Stacking)

## 小組討論 & 展示主題

1. 確認分組 & 期末專題主題的討論
2. 製作期末 html 檔案的簡單方法