# 7_v-for渲染
## 7_1渲染数组和对象元素
- v-for
## 7_2计算属性和列表渲染
- ul
- li
## 7_3示例
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>v-for渲染</title>
</head>
<body>

<!--DOM-->
<div id="app">
<h4>商品列表</h4>
	<ul>
		<li v-for="(goods,index) in goodsLists">{{index+1}}---{{goods.name}}---{{goods.price}}</li>
	</ul>
	<ul>
		<li v-for="goods in goodsLists">
			<ul>
				<li v-for="(value,key,index) in goods">{{index}}---{{key}}---{{value}}</li>
			</ul>
	</ul>
<div>
	<ul>
		<li v-for="goods in filterGoodsLists">{{goods.name}}---{{goods.price}}</li>
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
		{name:'apple',price:'9999'},
		{name:'huawei',price:'2012'},
		{name:'oppo',price:'9872'}	
		]
	};
	var vm=new Vue({
	el:'#app',
	data:data,
	computed:{
		filterGoodsLists:function(){
		return this.goodsLists.filter(function(goods){
		return goods.price>3000;
		})
		}
	}
	});
</script>
</body>
</html>
```