# 数组更新检测方法一：Vue静态方法
- Vue.set()
- vm对象.$set()
# 数组更新检测方法二：数组变异方法
- 添加删除元素push()、pop()、shift()、unshift()
- 数组元素排序sort()、reverse()
- 更广义地添加/删除splice()
	- array.splice(删除位置下标，删除元素个数)
	- array.splice(添加位置下标，0，待添加元素)
- slice()获取值
# 示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>数组更新检测</title>
</head>
<body>

<!--DOM-->
<div id="app">
<h4>Test</h4>
<ul>
	<li v-for="(e,index) in goodsLists">{{index+1}}---{{e}}</li>
</ul>
<!--
vm.goodsLists.push('t1');#在数组尾部添加元素
vm.goodsLists.push('t1');#在数组尾部删除元素
vm.goodsLists.unshift('t1');#在数组首部添加元素
vm.goodsLists.shift('t1');#在数组首部删除元素
vm.users.sort(function(a,b){return a.age-b.age});#从小到大排序
vm.users.splice(1,0,{name:'xii',age:99});#添加元素
vm.users.splice(1,1);#删除元素
vm.users.slice(1,2);#删除元素
-->
<div>
	<ul>
		<li v-for="(item,id) in users">{{id+1}}---{{item.name}}---{{item.age}}</li>
	</ul>
</div>
</div>

<!--引入vue-->
<script src="../js/vue.js"></script>

<!--javascript-->
<script>
<!--vue&javascript-->
	var data={
	goodsLists:[
		'm1',
		'm2',
		'm3'	
		],
	users:[
	{name:'xu',age:20},
	{name:'liu',age:30},
	{name:'wang',age:18},
	]
	};

	var vm=new Vue({
	el:'#app',
	data:data,
	});
</script>
</body>
</html>
```