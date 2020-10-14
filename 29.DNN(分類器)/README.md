# DNN (分類器)


## 今日學習目標
- 深度神經網路 DNN 
    - 揭開神秘的黑盒子
- 六步驟建立深度學習模型
    - 如何選擇隱藏層、激發函數、損失函數以及優化器
- 實作 DNN 分類器 
    - 使用DNN訓練一個手寫數字辨識分類器

![](https://i.imgur.com/u9ypBHR.png)

![](https://i.imgur.com/aauR3pS.png)

## 六步驟建立深度學習模型
1. 決定隱藏層 (hidden layers) 的深度 (層數) 和寬度 (神經元數)
2. 決定每層使用的激發函數 (activation function)
3. 決定模型的損失函數 (loss function)
4. 決定優化器 (optimizer)，及超參數
5. 編譯模型 (compile model)
6. 開始訓練 (fit model)

## 如何選擇 Loss function?
- 分類問題 (Classification)
    - cross-entropy
    - 搭配 softmax 作為輸出層的激發函數
- 迴歸問題 (Regression)
    - mean squared error (MSE)
    - mean absolute error (MAE)
    - 搭配線性函數作為輸出層的激發函數


本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！