# API前後端串接
[![Yes](https://img.youtube.com/vi/BTG5Cm2sUaI/0.jpg)](https://www.youtube.com/watch?v=BTG5Cm2sUaI)


## 今日學習目標
- API 前後端串接 
    - 建立一個鳶尾花朵分類器的網頁

## API URL
採用 Day 26 部署在 Heroku 的 API 來跟網頁前端串接。

![](https://i.imgur.com/8rze0W2.png)

[API 傳送門](https://flask-api-example-with-ml-mode.herokuapp.com/predict)

## 使用 ES6 Fetch API
HTTP Request 在網頁有很多種方式可以實作，像是 ajax、axios、Fetch...等。其中 Fetch 是 ES6 的新語法，意味著最新版瀏覽器可支援的原生函式庫。其優點是不需而外載入其他函式庫，Fetch 主要是透過 Promise 來執行請求資料和接收 HTTP Response 的處理方式。

下面程式參考 [Fetch-MDN-Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) 透過建立 `postData()` 函式，開發者可以重複呼叫做 HTTP Request。其用法直接傳入 API URL 以及需要 POST 的資料即可。

```js
function postData(url, data) {
    // Default options are marked with *
    return fetch(url, {
        body: JSON.stringify(data), // must match 'Content-Type' header
        cache: 'no-cache', // *default, no-cache, reload, force-cache, only-if-cached
        credentials: 'same-origin', // include, same-origin, *omit
        headers: {
            'user-agent': 'Example',
            'content-type': 'application/json'
        },
        method: 'POST', // *GET, POST, PUT, DELETE, etc.
        mode: 'cors', // no-cors, cors, *same-origin
        redirect: 'follow', // manual, *follow, error
        referrer: 'no-referrer', // *client, no-referrer
    })
        .then(response => response.json()) // 輸出成 json
}
```


```js
const url = 'Your API Request URL';
const data = '{ Your data need JSON Object format }';
    
postData(url, data)
.then(data => {
    // response
    const result=data.result ;
})
.catch(error => console.error(error))
```

## Demo
![](https://i.imgur.com/iNaiG0Z.png)

[Demo網頁](https://1010code.github.io/website-API-example)



本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！