# 隨機森林：每隻「螞蟻」需要是一樣的嗎？

## 課程大綱

### 集成方法的訓練技巧

幫助減少 Variance error（第 8.3 節）

- 裝袋法 (Bagging)
- 堆疊法 (Stacking) 

### 分類與迴歸樹（CART）

使用階梯函數 ($f(\textbf{x}) = c_1 or c_2$) 來分割或擬合資料。

- 剪枝與正則化
- 為分類問題選擇損失函數：熵（Entropy）或吉尼指數（Gini Index）

### 隨機森林

- 自助重抽法 + CART + 集成
- 使用袋外（Out-of-Bag, OOB）數據進行模型驗證 ($p$ 和 $n_{min}$)
- 極端隨機樹（Extremely randomized trees）：不使用自助重抽，改為隨機選擇分割點

### 提升法（Boosting）

同樣不使用自助重抽法，而是一直不斷更新先前模型，並把改進的重點放在先前模型表現不佳的部分。

#### 梯度提升

使用梯度下降法更新先前模型
XGBoost（正則化梯度提升）：增加更多正則化項

## 小組討論 & 展示主題

我已經弄了一個[模板 Jupyter Notebook](https://github.com/whyjz/ncu-env-data-science-zhtw/blob/main/docs/project.ipynb)，你可以在這個模板之上撰寫你的期末專題，寫好後再把 Notebook 匯出成 HTML (`nbconvert`)，就可以利用 GitHub Pages 來發布你的作品。可以從[這裡](https://whyjz.github.io/ncu-env-data-science-zhtw/project.html)看看部署完成的 HTML 會長怎樣。