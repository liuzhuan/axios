`mergeConfig(config1, config2)` 根据一定规则，合并选项参数，在 axios 中大量使用。

1. 如果是 `url`, `method` 等普通字符串，则使用 `config2` 的值
2. 如果是 `headers`, `auth` 等对象选项，则使用 `config2` 和 `config1` 的合并选项
3. 如果是 `baseURL` 等选项，则优先使用 `config2`，否则，使用 `config1` 

工具类 `utils` 提供如下三个工具函数：

* `utils.forEach(obj, fn)` 用于遍历对象或数组，为每个元素执行函数 `fn`
* `utils.isObject(val)` 判断 val 是否对象类型
* `utils.deepMerge(/* obj1, obj2, obj3, ... */)` 深层合并