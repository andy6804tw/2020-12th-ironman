# 儲存訓練好的模型
[![Yes](https://img.youtube.com/vi/w2zMaPu1fbw/0.jpg)](https://www.youtube.com/watch?v=w2zMaPu1fbw)

## 今日學習目標
- 使用 pickle + gzip 儲存模型
    - 將訓練好的模型打包並儲存
- 載入儲存的模型
    - 讀取打包好的模型，並預測

我們訓練好了一個模型以後需要保存並讓下一次直接預測。常見的兩種保存Model的模塊有 pickle 與 joblib，範例使用 pickle 。由於 pickle 儲存模型後容量可能會有好幾百MB因此建議可以透過 gzip 來壓縮模型並儲存。

![](https://i.imgur.com/55IeJSo.png)

![](https://i.imgur.com/gjhT0FQ.png)

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！