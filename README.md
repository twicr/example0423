# Interview
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
# CSS
### 简述你对BFC规范的理解
如果一个DOM元素具有BFC，则外部盒子不会影响内部，内部盒子不会影响外部，最简单的应用：当内部盒子设置浮动时，外部盒子不会被撑开，当外部盒子设置BFC时，则外部盒子可以被撑开。

最简单的BFC：设置浮动
# JS
### 统计某一字符或字符串在另一个字符串中出现的次数
* 使用split()方法
```javascript
var num = strParent.split(str).length - 1;
console.log(num);
```
* 使用includes()方法判断
```javascript
function substrCount(str, target) {
	let count = 0;
	while (str.includes(target)) {
		const index = str.indexOf(target);
		count++;
		str = str.substring(index + target.length);
	}
	return count;
}
```
* 使用match()方法遍历
```javascript
function count(str, param) {
	const reg = new RegExp(param, 'g');
	return str.match(reg).length;
}
```
