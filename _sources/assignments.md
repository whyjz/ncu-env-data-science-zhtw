# 作業

## 問題集 #1

1. 完成 Hsieh 書中的 Exercise 4.1。
2. 完成 Hsieh 書中的 Exercise 4.5。（資料來源：`SWE_Nino_Nina.csv`）
3. 完成 Hsieh 書中的 Exercise 4.6。（資料來源：`Nino1+2_anomalies.csv` & `Nino3.4_anomalies.csv`）
4. 針對 `SWE_Nino_Nina.csv` 中的 SWE 資料，使用自助重抽法計算其中位數的 95% 信賴區間。務必避免使用百分位數法 (percentile method)。
5. 重製「修課前 Quiz」第 3 題的圖表。（[圖表連結](https://drive.google.com/file/d/15WejYTcSHDGM3VNoX32WaD5r8l-BNNF-/view?usp=sharing)）*圖表來源：Nicolas P. Rougier (2021)*

## 問題集 #2

1. 完成 Hsieh 書中的 Exercise 5.7。（資料來源：`Milwaukee_wind_direction_ozone.csv`）
2. 把 `SWE_tele.csv` 的資料進行視覺化呈現，並提出幾個可以用此圖來證明或支持的論點。
3. 完成 Hsieh 書中的 Exercise 5.8。（資料來源：`SWE_tele.csv`）
4. 完成 Hsieh 書中的 Exercise 5.9。（資料來源：`SWE_tele.csv`）

## 問題集 #3

1. 完成 Hsieh 書中的 Exercise 6.5。請使用 MLP 或 ELM 模型，並使用交叉驗證來調校至少一個模型超參數。（資料來源：`SWE_tele.csv`）
2. 完成 Hsieh 書中的 Exercise 8.1。請調校 MLP 神經網路模型的學習率。為了方便比較結果，請使用我幫你生成的輸入資料來訓練與測試模型。資料可以從[此連結](https://drive.google.com/drive/folders/1_qCa8-g6zYXFj7Pz8RD1JEj3hgtImE5O?usp=sharing)下載（`data_noise-*.csv`）。
3. 將 Exercise 8.1 的迴歸結果視覺化，至少要呈現高斯雜訊為 $y_{\textrm{signal}}$ 的標準差 0.5 倍的情況。


<!-- ## 問題集 #4

1. 完成 Hsieh 書中的 Exercise 12.1。使用資料：`forest_testing.csv` & `forest_testing.csv`
2. 承上題，使用支持向量機（SVM）對同數據集中的森林類型進行分類。可以自由選擇「一對多」或「一對一」的方法，不過須註明你的選擇。使用前兩個預測變數進行訓練，並將本題與上題的結果進行比較。
3. 產生一個含有噪訊的合成訊號 $y = \sin x + 0.5 \times \mathcal{N}(0, 1)$，然後在 $x = [0, 4\pi]$ 的區間內產生 40 個資料點。使用 (a) 嶺迴歸、(b) 核嶺迴歸，以及 (c) 高斯過程迴歸來建構模型，並且在 $x = [0, 8\pi]$ 的區間內做出模型的預測。詳細描述並解釋你是怎麼決定或調整使用的核與其他超參數，有必要的話也可包含超參數調校的流程。最後，把結果盡可能地視覺化，並比較三種迴歸模型的結果。

## 問題集 #5

完成 Hsieh 書中的以下 Exercises，並按照指定要求進行：

1. Exercise 14.2，包括 (c)。
2. Exercise 12.5，但需開發兩個預測模型，而不是一個。其中一個模型必須是隨機森林或應用了提升法（Boosting method）的模型。
3. Exercise 14.4，包括 (b)。

使用資料：
- 14.2: `wilt_training.csv` & `wilt_testing.csv`
- 12.5: `SydneyAirport_weather.csv`
- 14.4: `YVR_prcp_training.csv` & `YVR_prcp_testing.csv` -->
