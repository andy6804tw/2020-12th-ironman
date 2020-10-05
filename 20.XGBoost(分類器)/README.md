# XGBoost (分類器)
[![Yes](https://img.youtube.com/vi/kPvw-b6V-G4/0.jpg)](https://www.youtube.com/watch?v=kPvw-b6V-G4)

## 今日學習目標
- XGBoost 介紹
    - XGBoost 是什麼?為什麼它那麼強大?
- Bagging vs. Boosting
    - 比較兩種集成式學習架構差異
- 實作 XGBoost 分類器 
    - 比較 Bagging 與 Boosting 兩者差別

XGBoost 是由華盛頓大學博士生陳天奇所開發，是目前 Kaggle 競賽中最常見到的算法。

![](https://i.imgur.com/JpINBDL.png)

## Bagging vs. Boosting
- Bagging 透過抽樣的方式生成樹，每棵樹彼此獨立
- Boosting 透過序列的方式生成樹，後面生成的樹會與前一棵樹相關

![](https://i.imgur.com/KHXQpdk.png)

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！