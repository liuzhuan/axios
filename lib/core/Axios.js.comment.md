`Axios.prototype.request` 是核心的请求函数，其余方法都是它的快捷方式：

```js
utils.forEach(['delete', 'get', 'head', 'options'], function forEachMethodNoData(method) {
    Axios.prototype[method] = function (url, config) {
        return this.request(utils.merge(config || {}, {
            method,
            url,
        }))
    }
})

utils.forEach(['post', 'put', 'patch'], function forEachMethodWithData(method) {
    Axios.prototype[method] = function (url, data, config) {
        return this.request(utils.merge(config || {}, {
            method,
            url,
            data,
        }))
    }
})
```

选项由用户传入的选项和默认选项构成：

```js
var mergeConfig = require('./mergeConfig')
config = mergeConfig(this.defaults, config)
```