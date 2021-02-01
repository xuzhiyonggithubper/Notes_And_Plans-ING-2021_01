# Vue生命周期钩子函数（回调函数）
|钩子函数|说明|
|:---:|:---:|
|beforeCreate|Vue对象创建之前|
|created|Vue对象创建之后|
|beforeMount|Vue对象和文档节点挂载之前|
|mounted|Vue对象和文档节点挂载之后|
|beforeUpdate|视图数据改变之前|
|updated|视图数据改变之后|
|beforeDestory|Vue对象销毁之前|
|destroyed|Vue对象销毁之后|
# 示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Vue生命周期</title>
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
	data:data,
	//生命周期回调函数
	beforeCreate:function(){
	//创建Vue对象之前回调
	console.log('before');
	console.log(this);
	console.log(this.$data);
	console.log(this.$el);
	},
	//创建Vue对象之后回调
	created:function(){
	console.log('created')
	console.log(this);
	console.log(this.$el);
	console.log(this.$data.age);
	},
	//绑定（挂载）view和model之前回调
	beforeMount:function(){
	console.log('beforeMount');
	console.log(this.$el.innerHTML);
	},
	//绑定（挂载）view和model之后回调
	mounted:function(){
	console.log('Mount');
	console.log(this.$el.innerHTML);
	}
});
	console.log('now');
	console.log(vm.$data.name);
</script>
</body>
</html>
```