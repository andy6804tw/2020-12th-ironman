[![Yes](https://img.youtube.com/vi/P42GqxCXkY8/0.jpg)](https://www.youtube.com/watch?v=P42GqxCXkY8)

# 資料清理&前處理
## 今日學習目標
- 資料如何清理
    - 什麼是資料清理？
- 資料前處理的方式
    - 為什麼資料要前處理呢？前處裡有何好處？
- 學習 sklearn 中四種不同資料前處理方式
    - StandardScaler (平均值和標準差)
    - MinMaxScaler(最小最大值標準化)
    - MaxAbsScaler（絕對值最大標準化）
    - RobustScaler

## 前言
很多演算法對數據範圍非常的敏感。因此為了要讓模型訓練的更強大，通常的做法是對特徵進行調節，使得數據更適合這些演算法。一般來說，我們在做機器學習時往往會做特徵的縮放。

很推薦這篇文章講關於特徵工程: https://www.itread01.com/content/1542164169.html

## Standardization 平均&變異數標準化
將所有特徵標準化，也就是高斯分佈。使得數據的平均值為0，方差為1。
適合的使用時機於當有些特徵的方差過大時，使用標準化能夠有效地讓模型快速收斂。

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler().fit(X)
X_scaled = scaler.transform(X)
```

![](https://i.imgur.com/2jFW8C8.png)

## MinMaxScaler 最小最大值標準化
在MinMaxScaler中是給定了一個明確的最大值與最小值。每個特徵中的最小值變成了0，最大值變成了1。數據會縮放到到[0,1]之間。

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler(feature_range=(0, 1)).fit(X)
X_scaled = scaler.transform(X)
```

![](https://i.imgur.com/vvNAYMv.png)

## MaxAbsScaler 絕對值最大標準化
MaxAbsScaler 與 MinMaxScaler 類似，所有數據都會除以該列絕對值後的最大值。
數據會縮放到到[-1,1]之間。

```python
from sklearn.preprocessing import MaxAbsScaler

scaler = MaxAbsScaler().fit(X)
X_scaled = scaler.transform(X)
```

![](https://i.imgur.com/LnjE3OC.png)

## RobustScaler 中位數和四分位數標準化
可以有效的縮放帶有outlier的數據，透過Robust如果數據中含有異常值在縮放中會捨去。

```python
from sklearn.preprocessing import RobustScaler

scaler = RobustScaler().fit(X)
X_scaled = scaler.transform(X)
```

![](https://i.imgur.com/jTS0y01.png)



本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！