# KNN (迴歸器)
[![Yes](https://img.youtube.com/vi/ZQC_gYiOzHI/0.jpg)](https://www.youtube.com/watch?v=ZQC_gYiOzHI)

## 今日學習目標
- KNN 迴歸
    - 學習 KNN 方法如何處理連續性輸出
- 實作 KNN 迴歸器 
    - 查看KNN方法在簡單線性迴歸和非線性迴歸表現

![](https://i.imgur.com/LRFsybz.png)

在 sklearn 中 KNN 提供迴歸(Regression)演算法。輸出的結果是一個連續性數值，該值是其k個最近鄰居的值的平均值。k-近鄰演算法的缺點是對資料的局部結構非常敏感。本演算法與K-平均(K means)演算法沒有任何關係，請勿與之混淆。

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！