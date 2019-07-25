# example0423
# 每日三问——0423
> [github项目](https://github.com/haizlin/fe-interview?utm_source=ZHShareTargetIDMore&utm_medium=social&utm_oi=750848792785354752) 问题解答
# HTML
### iframe框架都有哪些优缺点？
优点：
* 重载时不需要刷新整个页面，只需刷新页面中的一个框架页
* 可以实现跨域，每个iframe的源都可以不相同
* 多页面显示时，对于共同的header、footer、nav等都可以用iframe加载，拆分代码。

缺点：
* 每一个iframe都对应一个页面，也就意味着多余的css，js导入，增加页面请求开销
* 如果iframe内含有滚动条，会影响用户体验
* window.onload事件会在iframe加载完成后才执行，造成页面阻塞
