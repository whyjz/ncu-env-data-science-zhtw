# 作業

## 問題集 #1

完成 Hsieh 書中的 Exercises 4.2、4.3、4.5 和 4.6。

使用資料：
- 4.2: `Winnipeg_DJF_temp.csv`
- 4.5: `SWE_Nino_Nina.csv`
- 4.6: `nino34_long_anom.csv` & `nino12_long_anom.csv`

## 問題集 #2

完成 Hsieh 書中的 Exercises 5.2、5.6、5.7 和 5.9。

使用資料：
- 5.2: `Old_Faithful_geyser.csv`
- 5.6: `Vanc_Tor_Temp_tele.csv`
- 5.7: `Milwaukee_wind_direction_ozone.csv`
- 5.9: `SWE_tele.csv`

## 問題集 #3

完成 Hsieh 書中的 Exercises 6.5、6.6 和 8.1。

使用資料：
- 6.5: `SWE_tele.csv`
- 6.6: `YVR_prcp_training.csv` & `YVR_prcp_testing.csv`

## 問題集 #4

1. 完成 Hsieh 書中的 Exercise 12.1。使用資料：`forest_testing.csv` & `forest_testing.csv`
2. 承上題，使用支持向量機（SVM）對同數據集中的森林類型進行分類。可以自由選擇「一對多」或「一對一」的方法，不過須註明你的選擇。使用前兩個預測變數進行訓練，並將本題與上題的結果進行比較。
3. 產生一個含有噪訊的合成訊號 $y = \sin x + 0.5 \times \mathcal{N}(0, 1)$，然後在 $x = [0, 4\pi]$ 的區間內產生 40 個資料點。使用 (a) 嶺迴歸、(b) 核嶺迴歸，以及 (c) 高斯過程迴歸來建構模型，並且在 $x = [0, 8\pi]$ 的區間內做出模型的預測。詳細描述並解釋你是怎麼決定或調整使用的核與其他超參數，有必要的話也可包含超參數調校的流程。最後，把結果盡可能地視覺化，並比較三種迴歸模型的結果。

<!-- ## Problem set #5

Complete the following exercises in Hsieh's book with the specified requirements:

1. Exercise 14.2, including (c)
2. Exercise 12.5, but develop two prediction models instead of one. One of the models must be a random forest or a boosting model.
3. Exercise 14.4, including (b) -->