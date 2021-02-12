# 2_第1个vue应用程序
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>2_第1个vue应用程序</title>
</head>
<body>

<!--DOM-->
<div id="app">
name={{name}}
</div>

<!--引入vue-->
<script src="../js/vue.js"></script>

<!--javascript-->
<script>
<!--Data-->
	var data={
	name:'vue application'
};
<!--vue&javascript-->
	var vm=new Vue({
	el:'#app',
	data:data
});
</script>
</body>
</html>
```
## 2_1Vue开发工具
- Vue官方文档：https://cn.vuejs.org/v2/guide
- NPM文档：https://www.kancloud.cn/shellway/npm-doc/199982
- Webpack文档：https://doc/webpack-china.org/concepts/
## 2_2Vue开发浏览器
- chrome浏览器
- Vue-devtools插件
## 2_3代码编写工具
- Atom
- Sublime Text
- Visual Studio Code（常用插件如下）
  - JavaScript（ES6） code snippets
  - Vutur
  - VueHelper
- Webstorm