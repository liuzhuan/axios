使用 `XMLHttpRequest` 用来发起 ajax 请求，封装为 Promise 异步风格。

```js
module.exports = function xhrAdapter(config) {
    return new Promise(function(resolve, reject) {
        var requestData = config.data
        
        var request = new XMLHttpRequest()
        request.open(config.method.toUpperCase(), buildURL(/* ... */), true)

        request.onreadystatechange = function handleLoad() {}
        request.send(requestData)
    })
}
```