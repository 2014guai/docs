## Promise

* 状态：
  * `Pending`（进行中）
  * `fulfilled`（已成功）
  * `rejected`（已失败）
  * ** 状态改变只能是 `pending->fulfilled` 或者 `pending->rejected`，状态一旦改变则不能再变。**
* 链式调用
  * `promise` 每次调用 `.then` 或者 `.catch` 都会返回一个新的 `promise`
  * 不是使用`return this`实现
* `Promise` 构造函数是同步执行的，`promise.then` 中的函数是异步执行的。

```
const promise = new Promise((resolve, reject) => {
  console.log(1)
  resolve()
  console.log(2)
})
promise.then(() => {
  console.log(3)
})
console.log(4)
// 1,2,4,3
```
* `Promise.resolve`

```
var similarProm = new Promise(res => res(5));
// 等价于
var prom = Promise.resolve(5);
```

