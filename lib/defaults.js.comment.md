`defaults.js` 定义了诸多默认值。

- `adapter`: 发起 http 请求的适配器
- `transformRequest`: 改变请求的数字
- `transformResponse`: 改变响应数据
- `timeout`: 超时时间
- `xsrfCookieName`: 用来支持[XSRF][xsrf]，用来读取 cookie 名称
- `xsrfHeaderName`: 用来支持[XSRF][xsrf]，当作设置的 header 字段
- `maxContentLength`: 相应体最大容量，超过则报错
- `validateStatus`: 检测响应是否成功

[xsrf](https://en.wikipedia.org/wiki/Cross-site_request_forgery)