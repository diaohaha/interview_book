## 名词概念


### 生命周期  钩子函数

```
我们把一个对象从生成（new）到被销毁（destory）的过程，称为生命周期。而生命周期函数，就是在某个时刻会自动执行的函数。这就是钩子函数。
常用的有8大声明周期函数.
```

|  函数   | 调用时间  |
|  ----  | ----  |
| beforeCreate  | vue实例初始化之前调用 |
| created  | vue实例初始化之后调用 |
| beforeMount  | 挂载到DOM树之前调用 |
| mounted  | 挂载到DOM树之后调用 |
| beforeUpdate  | 数据更新之前调用 |
| updated  | 数据更新之后调用 |
| beforeDestroy  | vue实例销毁之前调用 |
| destroyed  | vue实例销毁之后调用 |



