# vue3.0-reactiveDemo
vue3.0 响应式原理demo, 用proxy实现响应式数据, 改变数据时自动更新视图。
在线demo: http://gavincat.cn:8081/

博客链接: https://blog.csdn.net/qq_36259513/article/details/103658136

> vue3.0响应式源码 对比 2.0的区别：
- 1. 3.0采用proxy实现代码侦测, 2.x用Object.defineProperty。
- 2. 3.0解决了2.x删除、新增属性无法被侦测的局限，所以3.0不需$del, $set来触发依赖了。
- 3. 3.0将reactive方法暴露出来，用户可自行选择将哪些数据转化成响应式，2.x则是定义在data函数中的所有复杂变量都会自动转为响应式。
- 4. 3.0用weakMap收集依赖，2.x用数组收集依赖，weakMap能及时释放引用，不占内存。
- 5. 3.0这部分代码是面向过程编程，2.x是面向对象编程。
