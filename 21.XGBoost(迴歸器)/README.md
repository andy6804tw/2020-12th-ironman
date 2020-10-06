# XGBoost (迴歸器)
[![Yes](https://img.youtube.com/vi/xOQNBeB0Eqo/0.jpg)](https://www.youtube.com/watch?v=xOQNBeB0Eqo)

## 今日學習目標
- 了解 XGBoost Regression
    - Boosting vs Decision tree & Bagging vs. Boosting
- 實作 XGBoost 迴歸器
    - 查看 XGBoost 在簡單線性迴歸和非線性回歸表現


XGBoost是boosting算法的其中一種，它除了可以做分類也能進行回歸連續性數值的預測，而且效果通常都不差。Boosting演算法的思想是將許多弱分類器集成在一起形成一個強分類器。

![](https://i.imgur.com/vkQPGKl.png)

## Boosting vs Decision tree
- 決策樹通常為一棵複雜的樹
- Boosting 是產生非常多棵的樹但是每一棵的樹都很簡單

> 目標把多個簡單的樹合再一起才能當最後的預測

## Bagging vs. Boosting
一般來說 Boosting 的模型會比 Bagging 來的精準。

- Bagging 透過抽樣的方式生成樹，每棵樹彼此獨立
- Boosting 透過序列的方式生成樹，後面生成的樹會與前一棵樹相關

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！