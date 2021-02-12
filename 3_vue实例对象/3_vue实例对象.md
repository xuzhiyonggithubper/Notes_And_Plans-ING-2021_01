# 3_vue实例对象
## 3_1Vue实例对象概念
Vue程序核心是Vue实例对象，即ViewModel，Vue对象连接视图层（HTML页面）和模型层（数据），ViewModel进行数据双向绑定，View动作触发→DOM Listeners→Model，Model变化→Data Bindings→View更新。
## 3_2示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>3_vue实例对象</title>
</head>
<body>

<!--DOM-->
<div id="app">
<span>span.name={{name}}</span>
<br>
<span>span.age={{age}}</span>
</div>

<!--引入vue-->
<script src="../js/vue.js"></script>

<!--javascript-->
<script>
<!--vue&javascript-->
	var data={
	name:'xu',
	age:20
};
	var vm=new Vue({
	el:'#app',
	data:data
});
	console.log(vm);
</script>
</body>
</html>
```
## 3_3Vue实例对象实例选项
- data
- el
- props
- methods
- computed
## 3_4Vue实例对象中原始数据操作
- 使用vm.$data.name访问原始数据并修改
- Vue实例代理了data对象上所有属性，因此vm.name等价于vm.$data.name