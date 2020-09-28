# SVM (分類器)
[![Yes](https://img.youtube.com/vi/wdeYo3fsT5U/0.jpg)](https://www.youtube.com/watch?v=wdeYo3fsT5U)

## 今日學習目標
- 了解 SVM 分類器
    - 何謂支持向量機 ? 非線性與線性?
- SVM 分類器手把手實作 
    - 藉由圖形化的邊界，來了解使用不同的 Kernel 及不同參數的意義。


一般在分類的問題我們就是要，找出在不同的資料類別中的分隔線。但在一般狀況下這個分隔線非常複雜且有很多種可能。然而SVM就是要在這很多種的可能當中找出最佳的解。SVM演算法的精神就是找出一條分隔線使所有在邊界上的點離得越遠越好，使模型抵抗雜訊的能力更佳。

![](https://i.imgur.com/cZVmI87.png)

SVM 能夠透過 C 來達到 weight regularization 來限制模型的複雜度，C越小表示對模型容錯空間過大。除了這點我們還能透過 SVM 的 Kernel trick 的方式將資料做非線性轉換，常見的 kernel 除了 linear 線性以外還有兩了非線性的Polynomial 高次方轉換以及 Radial Basis Function 高斯轉換。

![](https://i.imgur.com/z5iuMPO.png)


本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！