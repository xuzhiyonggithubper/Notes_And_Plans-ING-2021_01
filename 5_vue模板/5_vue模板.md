# 5_vue模板
## 5_1直接输出Vue变量
- {{Vue变量}}
- vm.$data.key
## 5_2输出解析后的HTML变量
- v-html
## 5_3在HTML属性中输出变量
- v-bind
## 5_4输出JS表达式
- {{number+1}}
- {{ok?'yes':'no'}}
- {{message.split('').reverse().join('')}}
- **<div v-bind:id="'list-' + id"></div>**
## 5_5示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>5_vue模板</title>
</head>
<body>

<!--DOM-->
<div id="app">
<div>
	str={{str}}
</div>
<div>
	name=vm.$data.user.name<br>
	age={{user.age}}<br>
</div>

<div>
	<ul>
		<li>{{names[0]}}</li>
		<li>{{names[1]}}</li>
		<li>{{names[2]}}</li>
	</ul>
</div>
<div>
	html={{html}}<br>
</div>
<div v-html="html"></div>
<a v-bind:href="link.link">{{link.name}}</a><br>
<a :href="link.link">{{link.name}}</a>
</div>

<!--引入vue-->
<script src="../js/vue.js"></script>

<!--javascript-->
<script>
<!--vue&javascript-->
	var data={
	str:'xu',
	user:{
	name:'xu',
	age:'20'
	},
	names:['Tom','Bob','Robot'],
	html:'<font color=Red>xuzhiyong</font>',
	link:{
		name:'home',
		link:'http://www.baidu.com'	
	}
	};
	var vm=new Vue({
	el:'#app',
	data:data,
	});
	console.log(vm.$data.user.name)
</script>
</body>
</html>
```