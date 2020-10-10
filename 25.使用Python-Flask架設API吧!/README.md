# 使用Python Flask架設API吧!
[![Yes](https://img.youtube.com/vi/FUj88Q_L62k/0.jpg)](https://www.youtube.com/watch?v=FUj88Q_L62k)

這系列的 AI 文章快進入尾聲了，因此打算利用剩下來時間講解應用端的部分。同時也趁這幾次連假規劃了一些教學，希望接下來的內容能幫助到大家～

## 今日學習目標
- API 觀念講解
    - 什麼是 API? RESTful API? HTTP Request 方法?
- 手把手實作一個花朵分類器 API 
    - 透過 Python Flask 建置一個後端預測模型 API

很多人可能會有疑問模型訓練好然後呢?  昨天已經教各位如何儲存並匯出自己的模型了，今天就來教各位使用 Python Flask 架設一個鳶尾花朵分類器的 API 吧！

所謂的 API 就是屬於客戶端與伺服端的溝通橋樑，它提供一個端口能夠做資料交換。透過網路協定 HTTP Request 不同的方法，可以實現不同的資料交換請求方式。

![](https://i.imgur.com/CyKqRx7.png)

另外各位可能也有聽過一個名詞叫做 RESTful API。這邊就不細講了，有興趣的朋友可以參考我在2018 iT 邦幫忙鐵人賽的`從無到有，打造一個漂亮乾淨俐落的 RESTful API` 的系列文章 [[Day-7] RESTful API與MVC名詞介紹](https://ithelp.ithome.com.tw/articles/10191925) 同時那個系列是用 `Node.js` 建置一個後端 API 教學。

![](https://i.imgur.com/rdVzyoi.png)


![](https://i.imgur.com/sXNMUjO.png)

## 測試API的好工具Postman
當你寫好一支 API 時要馬上測試看看你寫的程式邏輯是否正確，就可以使用 Postman 這個軟體來做 API 測試。詳細內容可以參考之前的鐵人賽文章[[Day-20] 測試API的好工具](https://ithelp.ithome.com.tw/articles/10194897)。

![](https://i.imgur.com/pJXxsi8.png)

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！