`InterceptorManager` 是一个拦截经理。有三个实例方法：

1. `use(fulfilled, rejected)` 增加 Promise 处理函数，返回拦截器的 id（其实就是索引），方便后期移除。
2. `eject(id)` 移除某个拦截器
3. `forEach(fn)` 遍历当前经理名下的所有拦截器。

在 `./Axios.js` 被引用。