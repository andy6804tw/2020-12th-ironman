# Stacking

## 今日學習目標
- 了解 Stacking 方法
    - 堆疊法的學習機制為何 ?
- 利用 Stacking 實作分類器
    - 透過 Stacking Classifier 訓練一個森於預測分類器


![](https://i.imgur.com/4D2TeiV.png)
Stacking 中文稱為堆疊法，首先產生出 m 個 base learners(模型)彼此間並互相無關連，例如第一個 learner 為 KNN 第二個為決策樹。訓練完 m 個模型後，我們要把這m個模型合併在一起。合併的方式是我們另外再訓練一個模型，這個模型把 ｍ 個 base learner 的輸出當成新的模型的輸入因此我們會根據這 m 個特徵利用集成式學習其中的演算法來學習一個模型並預測最終結果。最後的 Ensemble model 可以使用線性回歸或是深度神經網路來做學習。總之 Ensemble model 的目的是把每一個 base learners 的輸出當成線索，並把這些線索想辦法做整合來得到最終的答案。另外在進行 Stacking 的時候要注意的是在訓練 m 個 base learners 的訓練資料和訓練 Ensemble model 的資料兩者的訓練資料要不同。

![](https://i.imgur.com/CZZqso5.png)


本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！