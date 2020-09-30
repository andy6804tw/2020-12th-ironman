# 決策樹 (分類器)
[![Yes](https://img.youtube.com/vi/1epy1EKVDkc/0.jpg)](https://www.youtube.com/watch?v=1epy1EKVDkc)


## 今日學習目標
- 決策樹演算法介紹
    - 決策樹如何生成?如何處理分類問題?
- 實作決策樹分類器
    - 觀察決策樹是如何生成的

決策樹會根據訓練資料產生一棵樹，依據訓練出來的規則來對新樣本進行預測。決策樹演算法可以使用不同的方式來評估分枝的好壞(亂度)，例如像是Information gain、Gain ratio、Gini index。
從訓練資料找出規則，讓每一個決策能夠使訊息增益最大化，叫好比我們評估今天比賽是否舉行，天氣因子可能站比較大的因素，而Co2的濃度高低可能站的因子程度較低。

![](https://i.imgur.com/LoX8eZZ.png)

![](https://i.imgur.com/ycCaJ8A.png)


本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！