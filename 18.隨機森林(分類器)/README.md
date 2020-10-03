# 隨機森林 (分類器)
[![Yes](https://img.youtube.com/vi/Ix0UhijD4Ks/0.jpg)](https://www.youtube.com/watch?v=Ix0UhijD4Ks)


## 今日學習目標
- 隨機森林介紹
    - 隨機森林的樹是如何生成?隨機森林的優點?
- 實作隨機森林分類器
    - 比較隨機森林與決策樹兩者差別

隨機森林其實就是進階版的決策樹。隨機森林是使用 Bagging + 隨機特徵方法所產生出來的 Ensemble learning 演算法。

![](https://i.imgur.com/wvUpi6K.png)

## 隨機森林的優點
- 每棵樹會用到哪些訓練資料及特徵都是由隨機決定 • 採用多個決策樹的投票機制來改善決策樹
- 與決策樹相比，不容易過度擬合
- 隨機森林每一棵樹都是獨立的
- 訓練或是預測的階段每一棵樹都能平行化的運行



本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！