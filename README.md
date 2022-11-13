# 醫病資料去識別化 Aicup 2020
本實驗使用nlp套件 kashigari 來做NER的任務。
實驗結果:約為71%

![](https://i.imgur.com/93M0fwh.jpg)

## 概述
本程式由兩個程式所組成，一個是訓練model的Ai_Cup_R1，
另一個是預測所使用的predict_biLSTM_CRF。
先利用Ai_Cup_R1訓練出模型儲存後，再利用predict_biLSTM_CRF讀test.txt來輸出結果。
![](https://i.imgur.com/eZys0jy.png)


## Ai_Cup_R1
![](https://i.imgur.com/xnnpn4G.png)
將讀進的train2切成上圖的形式，才能再丟進kashigari內訓練。

## predict_biLSTM_CRF
讀進test.txt，利用訓練完的model來進行NER並把結果輸出成tsv檔
